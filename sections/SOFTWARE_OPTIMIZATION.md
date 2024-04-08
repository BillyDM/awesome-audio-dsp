# Software Optimization

Tips and tools for optimizing audio software.

- [Agner Fog's Instruction Tables](https://www.agner.org/optimize/instruction_tables.pdf) - A useful table that lists the latency and throughput performance of various x86 instructions.
- [Algorithms for Modern Hardware](https://en.algorithmica.org/hpc/) by Sergey Slotin - Free online book on high performance computing.
  - The [Profiling](https://en.algorithmica.org/hpc/profiling/) chapter is a good guide on how to do effective profiling and benchmarking.
- [Audio Software Optimization Tips](../content/AUDIO_SOFTWARE_OPTIMIZATION_TIPS.md) - My own list of audio software optimization tips.
- [Auto-Vectorization in LLVM](https://llvm.org/docs/Vectorizers.html) - Tips and tricks on how to structure your code to most effectively take advantage of auto-vectorization.
- [Compiler Explorer] - Very useful tool that lets you analyze the assembly output of many different languages including Rust, C, and C++.
  - Note, you will generally want to enable compiler optimizations when using this tool to get the assembly output for release mode. To do this, enter the following text into the "Compiler options..." field for your given language/compiler:
    - C/C++ (gcc or clang): `-O3`
    - C/C++ (msvc): `/O2`
    - Rust: `-C opt-level=3`
  - Sometimes the compiler optimizes so much that it removes the function you want to analyze entirely (i.e. dead code elimination). To fix this, use the following function attributes for your given language/compiler:
    - C/C++ (gcc): `__attribute__((optimize("O0")))`
        - *Place this on a function that calls the function you want to analyze, not the function itself. For example:*
        - ```c
          int __attribute__((optimize("O0"))) main() {
            foo_my_function_to_analyze();
            return 0;
          }
          ```
    - C/C++ (clang): `__attribute__ ((optnone))`
        - *Place this on a function that calls the function you want to analyze, not the function itself. For example:*
        - ```c
          int __attribute__ ((optnone)) main() {
            foo_my_function_to_analyze();
            return 0;
          }
          ```
    - C/C++ (msvc): `#pragma optimize( "", off )` / `#pragma optimize( "", on )`
      - *Place these around a function that calls the function you want to analyze, not the function itself. For example:*
      - ```c
        #pragma optimize( "", off )
        int main() {
          foo_my_function_to_analyze();
          return 0;
        }
        #pragma optimize( "", on )
        ```
    - Rust: `#[no_mangle]` or `#[inline(never)]`
      - ```rust
        #[no_mangle]
        pub fn foo_my_function_to_analyze() {
          // ...
        }
        ```
- [Fast-DSP-Approximations](https://github.com/BillyDM/Fast-DSP-Approximations) - My own list of public-domain fast approximations of various expensive calculations.
- [How-to Optimize Rust Programs on Linux](http://www.codeofview.com/fix-rs/2017/01/24/how-to-optimize-rust-programs-on-linux/) - How-to guide on profiling Rust code on Linux.
- [Intel Intrinsics Guide](https://software.intel.com/sites/landingpage/IntrinsicsGuide) - x86 processor intrinsics
- [Minimizing Rust Binary Size](https://github.com/johnthagen/min-sized-rust) - Tips on how to reduce the size of Rust binaries. This is a very minor optimization, but it can sometimes be useful for shipping release versions of plugins.
  - Note, don't set `opt-level` to "s" or "z" because that will likely make performance much worse (except for maybe when running on an embedded system with little memory).
- [multiversion](https://crates.io/crates/multiversion) - Easy function multiversioning in Rust.
- [Performance Ninja Class](https://github.com/dendibakh/perf-ninja) - A free and open source online course on how to find and fix low-level performance issues.
- [projet μ - denormal](https://mu.krj.st/denormal/) - Important article on how to avoid denormals in your code.
  - [no_denormals](https://crates.io/crates/no_denormals) - A Rust crate for temporarily turning off denormals in your DSP code.
- [Real-time audio programming 101](http://www.rossbencina.com/code/real-time-audio-programming-101-time-waits-for-nothing) - Tips on writing real-time code.
- [Software Optimization Resources](https://www.agner.org/optimize/) - A popular resource on optimizing for x86 based architectures.
- [The Rust Performance Book](https://nnethercote.github.io/perf-book/title-page.html) - Tips on optimizing code in Rust.

# Profiling Tools

- [llvm-mca](https://www.llvm.org/docs/CommandGuide/llvm-mca.html) - Powerful machine code analyzer. You can also use this inside [Compiler Explorer] by selecting it under "Add tool".
- [uProf](https://www.amd.com/en/developer/uprof.html) - Powerful profiler for AMD processors.
- [Valgrind](https://valgrind.org/docs/manual/quick-start.html) - A collection of static analysis and profiling tools.
- [VTune](https://www.intel.com/content/www/us/en/docs/vtune-profiler/get-started-guide/2023/overview.html) - Powerful profiler for Intel processors.

# Portable SIMD Libraries

- [eve](https://github.com/jfalcou/eve) (C++)
- [highway](https://github.com/google/highway) (C++)
- [libsimdcpp](https://github.com/p12tic/libsimdpp) (C++)
- [MIPP](https://github.com/aff3ct/MIPP) (C++)
- [portable-simd](https://github.com/rust-lang/portable-simd) (Rust, currently requires the nightly compiler)

[Compiler Explorer]: https://godbolt.org/
