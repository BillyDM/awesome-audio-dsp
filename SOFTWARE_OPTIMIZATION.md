# Software Optimization
Tips and tools for optimizing audio software.

- [`Real-time audio programming 101`] - Tips on writing real-time code.
- [`Compiler Explorer`] - Very useful tool that lets you analyze the assembly output of many different languages including Rust, C, and C++.
- [`Intel Intrinsics Guide`] - x86 processor instrinsics
- [`Software Optimization Resources`] - A popular resource on optimizing for x86 based architectures.
- [`Agner Fog's Instruction Tables`] - A useful table that lists the latency and throughput performance of various x86 instructions.
- [`Auto-Vectorization in LLVM`] - Tips and tricks on how to structure your code to most effectively take advantage of auto-vectorization.
- [`The Rust Performance Book`] - Tips on optimizing code in Rust.
- [`How-to Optimize Rust Programs on Linux`] - How-to guide on profiling Rust code on Linux.
- [`Fast-DSP-Approximations`] - My own list of public-domain fast approximations of various expensive calculations.

# Portable SIMD Libraries

- [`highway`] (C++)
- [`eve`] (C++)
- [`MIPP`] (C++)
- [`libsimdcpp`] (C++)
- [`portable-simd`] (Rust, currently requires the nighly compiler)

# My 8 Audio Software Optimization Tips

## 1. Avoid using any operations that invoke the operating system in the process thread

OS operations don't have a predictable amount of execution time, meaning the OS can delay the operation for as long as it wants, leading to latency problems and xruns. In other words, these operations are not "realtime safe". These operations include:

- Mutexes, locks, and try-locks
  - Instead, use lock-free methods for sharing data between threads such as atomics or by using realtime-safe ring buffers like [`SPSCQueue`](https://github.com/rigtorp/SPSCQueue) in C++ or [`rtrb`](https://github.com/mgeier/rtrb) in Rust.
- Allocating and deallocating memory on the heap (i.e. `malloc` and `free` in C)
  - This also means avoid using data structures that use these operations under-the-hood such as `std::vector` in C++ and `std::Vec` in Rust. If you can, use constant-sized buffers that are allocated on the stack (i.e. arrays in C++ and Rust).
  - If you need these dynamically-sized data structures in the process thread, make sure they are pre-allocated with sufficient size during plugin initialization, and then freed when the plugin is dropped. While processing, don't use any methods on the vector that change its allocated capacity.
  - You can also allocate buffers on the GUI/main thread and then send a pointer to that buffer to the process thread via a realtime-safe message channel. Just make sure that the buffer is also freed on the GUI/main thread and not on the process thread.
- Reading/writing a file
  - If you need to stream data (for example a plugin that records to a file), then run that stream in a separate thread and pass data to/from the process thread via a realtime-safe ring buffer.
- Printing to the terminal
  - While this is fine to do while developing and debugging a plugin, just make sure that you disable terminal printing operations in the process thread before shipping the plugin or when measuring its performance.

## 2. Avoid excessive division and modulo operations

The division and modulo operations on both floating point and integer numbers are significantly more expensive than the addition, subtraction, and multiplication operations. If the same divisor is being used over and over again (it's especially common to divide by the sample rate), consider taking the reciprocal of the divisor once and then mutliplying by the reciprocal.

Note this does not apply if the divisor is a constant. Compilers will automatically convert those to multliplying by the reciprocal.

Even then, a lot of times compilers will automatically take the reciprocal of a divisor before a loop. But if you want to rely on this, you can use tools like [`Compiler Explorer`] to verify the assembly.

## 3. Prefer to use block-based processing instead of per-sample processing

In other words, prefer to use loops that process a chunk (aka block) of samples in each loop iteration instead of loops that process just a single sample in each loop iteration. The reasons why tie into the points 4, 5, and 6.

## 4. Cache misses are expensive on modern CPUs

Modern CPUs rely heavily on cached memory for their performance. If an operation causes the CPU to fetch data that is not readily available in its low-level cache, it has to wait around to pull that data from either high-level cache or from RAM.

One way to avoid cache misses is to make sure your buffers aren't too large, so that the CPU can fit all of the working buffers into its low-level cache. The optimal block size will usually be somewhere around 32 to 1024 samples. But of course experiment to see what performs best for your code.

## 5. Avoid excessive calls to medium/large-sized functions

Calling a function has a small amount of overhead, and this overhead can add up if called thousands or millions of times a second. Large function calls also makes it harder for a CPU to optimally cache its working memory.

By using block-based processing, you can reduce the number of function calls by only calling the function once per block of samples instead of calling it once per sample.

And note that I said "medium/large-sized functions". Modern compilers are really good at inlining small functions. But if you're still unsure whether or not a function is being inlined properly by the compiler, you can use tools like [`Compiler Explorer`] to verify the assembly. If it's not being inlined properly, you can use the `__forceinline` or `inline __attribute__((always_inline))` keywords in C++ or the `#[inline(always)]` keyword in Rust to try to force the compiler to inline it. Even then, always measure the performance to see if inlining the function actually improves performance, because a lot of times it can actually make the performance worse (it also can make the size of the compiled binary much larger).

## 6. Avoid excessive if and switch statements

Branching logic has a small amount of overhead, and this overhead can add up if called thousands or millions of times a second. Branching logic also makes it harder for a CPU to optimally cache its working memory.

This includes hidden if statements such as `asserts` or bounds-checking the index into an array.

By using block-based processing, you can reduce the number of branches by only invoking them once per block of samples instead of invoking them once per sample.

You can also try having multiple loops, one for each case. But of course the downside to that approach is duplicated code.

Also note that sometimes compilers can optimize branching inside loops by automatically splitting it into multiple loops. But if you rely on this, use tools like [`Compiler Explorer`] to verify the assembly.

Even then, modern CPUs tend to make heavy use of speculative execution to mitigate the overhead from branching. Always measure the performance to see if optimizing the branching logic actually makes a meaningful improvement.

## 7. Use SIMD intrinsics

SIMD intrinsics are special features built into CPUs that allow it to pack multiple numbers into a single "vector" object (not to be confused with `std::vector` in C++ or `std::Vec` in Rust) and then apply an operation to every number in that vector at the same time. It's kind of like multithreaded processing, but in a super fast single-threaded kind of way.

One big downside to using SIMD intrinsics is that these methods can differ between CPU architectures such as x86 and ARM, and they can even differ between different vendors and generations of CPUs. So this can create a lot of platform-specific code. If you don't want to mess with platform-specific code, there are some libraries that attempt to abstract over these intrinsics in a portable, cross-platform way including [`highway`], [`eve`], [`MIPP`], and [`libsimdcpp`] in C++ and [`portable-simd`] in Rust (currently requires nightly Rust).

For a list of SIMD intrinsics in x86 processors, look at the [`Intel Intrinsics Guide`].

Also note that modern compilers have a feature called "autovectorization" where they can automatically create SIMD code for the given target CPU. However, this process can be unreliable for all but the simplist algorithms. But if you want to rely on this, you can use [`Compiler Explorer`] to verify the assembly, and you can follow [`Auto-Vectorization in LLVM`] for some tips.

One more thing to mention is that you should prefer to use single-precision floating point numbers instead of double-precision floating point numbers, because you can pack twice as many single-precision floats into an SIMD vector. While there is some debate on whether using double-precision actually makes a difference to sound quality (and there are specific algorithms that do require the extra precision), the general consensus is that the noise introduced from single-precision quantization errors is negligible, and other factors such as the quality of antialiasing algorithms have a far greater impact on sound quality. *However*, if your algorithm doesn't allow you to pack in more than two or four numbers into a vector anyway, then there's no harm in using double-precision if you want to.

## 8. Don't assume that a change made your code faster, measure it!

This final point is probably the most important one. All the previous points (except for point 1) are just guidelines, they aren't hard and set rules. Perhaps you find that block-based processing performs worse for your algorithm, or maybe you find that forcing a function to be inlined performs worse, or maybe you find that SIMD intrinsics perform worse than before, or maybe you find that the trig functions built into the standard library perform better than a "fast approximation" you found online.

Point is, it's important to learn how to measure the performance of your code. You can use both benchmarking tools and profiling tools.

If performance is a key feature of your product, treat it like one. Set up tests and actions on your GitHub repo (or whatever continous integration system you use) to catch whenever a future change to your code or a future update to a compiler causes worse performance.

[`Fast-DSP-Approximations`]: https://github.com/BillyDM/Fast-DSP-Approximations
[`Intel Intrinsics Guide`]: https://software.intel.com/sites/landingpage/IntrinsicsGuide
[`Compiler Explorer`]: https://rust.godbolt.org/
[`Software Optimization Resources`]: https://www.agner.org/optimize/
[`Agner Fog's Instruction Tables`]: https://www.agner.org/optimize/instruction_tables.pdf
[`Real-time audio programming 101`]: http://www.rossbencina.com/code/real-time-audio-programming-101-time-waits-for-nothing
[`Auto-Vectorization in LLVM`]: https://llvm.org/docs/Vectorizers.html
[`The Rust Performance Book`]: https://nnethercote.github.io/perf-book/title-page.html
[`How-to Optimize Rust Programs on Linux`]: http://www.codeofview.com/fix-rs/2017/01/24/how-to-optimize-rust-programs-on-linux/
[`highway`]: https://github.com/google/highway
[`eve`]: https://github.com/jfalcou/eve
[`MIPP`]: https://github.com/aff3ct/MIPP
[`libsimdcpp`]: https://github.com/p12tic/libsimdpp
[`portable-simd`]: https://github.com/rust-lang/portable-simd
