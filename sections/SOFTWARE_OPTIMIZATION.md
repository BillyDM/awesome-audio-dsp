# Software Optimization
Tips and tools for optimizing audio software.

- [Audio Software Optimization Tips](../content/AUDIO_SOFTWARE_OPTIMIZATION_TIPS.md) - My own list of audio software optimization tips.
- [Real-time audio programming 101](http://www.rossbencina.com/code/real-time-audio-programming-101-time-waits-for-nothing) - Tips on writing real-time code.
- [Compiler Explorer] - Very useful tool that lets you analyze the assembly output of many different languages including Rust, C, and C++.
  - Note, you will generally want to enable compiler optimizations when using this tool to get the actual assembly output in release mode. To do this, enter the following text into the "Compiler options..." field for your given language/compiler:
    - C/C++ (gcc or clang): `-O3`
    - Rust: `-C opt-level=3`
- [Intel Intrinsics Guide](https://software.intel.com/sites/landingpage/IntrinsicsGuide) - x86 processor intrinsics
- [Software Optimization Resources](https://www.agner.org/optimize/) - A popular resource on optimizing for x86 based architectures.
- [Agner Fog's Instruction Tables](https://www.agner.org/optimize/instruction_tables.pdf) - A useful table that lists the latency and throughput performance of various x86 instructions.
- [Auto-Vectorization in LLVM](https://llvm.org/docs/Vectorizers.html) - Tips and tricks on how to structure your code to most effectively take advantage of auto-vectorization.
- [The Rust Performance Book](https://nnethercote.github.io/perf-book/title-page.html) - Tips on optimizing code in Rust.
- [How-to Optimize Rust Programs on Linux](http://www.codeofview.com/fix-rs/2017/01/24/how-to-optimize-rust-programs-on-linux/) - How-to guide on profiling Rust code on Linux.
- [Algorithms for Modern Hardware](https://en.algorithmica.org/hpc/) by Sergey Slotin - Free online book on high performance computing.
  - The [Profiling](https://en.algorithmica.org/hpc/profiling/) chapter is a good guide on how to do effective profiling and benchmarking.
- [Fast-DSP-Approximations](https://github.com/BillyDM/Fast-DSP-Approximations) - My own list of public-domain fast approximations of various expensive calculations.
- [projet μ - denormal](https://mu.krj.st/denormal/) - Important article on how to avoid denormals in your code.
  - [no_denormals](https://crates.io/crates/no_denormals) - A Rust crate for temporarily turning off denormals in your DSP code.
- [Minimizing Rust Binary Size](https://github.com/johnthagen/min-sized-rust) - Tips on how to reduce the size of Rust binaries. This is a very minor optimization, but it can sometimes be useful for shipping release versions of plugins.
  - Note, don't set `opt-level` to "s" or "z" because that will likely make performance much worse (except for maybe when running on an embedded system with little memory).
- [multiversion](https://crates.io/crates/multiversion) - Easy function multiversioning in Rust.

# Profiling Tools

- [llvm-mca](https://www.llvm.org/docs/CommandGuide/llvm-mca.html) - Powerful machine code analyzer. You can also use this inside [Compiler Explorer] by selecting it under "Add tool".
- [VTune](https://www.intel.com/content/www/us/en/docs/vtune-profiler/get-started-guide/2023/overview.html) - Powerful profiler for Intel processors.
- [uProf](https://www.amd.com/en/developer/uprof.html) - Powerful profiler for AMD processors.
- [Valgrind](https://valgrind.org/docs/manual/quick-start.html) - A collection of static analysis and profiling tools.

# Portable SIMD Libraries

- [highway](https://github.com/google/highway) (C++)
- [eve](https://github.com/jfalcou/eve) (C++)
- [MIPP](https://github.com/aff3ct/MIPP) (C++)
- [libsimdcpp](https://github.com/p12tic/libsimdpp) (C++)
- [portable-simd](https://github.com/rust-lang/portable-simd) (Rust, currently requires the nightly compiler)

[Compiler Explorer]: https://godbolt.org/
