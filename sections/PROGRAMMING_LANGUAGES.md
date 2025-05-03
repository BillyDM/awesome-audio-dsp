# Programming Languages

A list of programming languages used to make audio software, along with their pros and cons.

# Low-level Languages

When you want to get serious with audio DSP & audio plugin development, nothing beats writing code in a low-level programming language with manual memory management.
 - Multiplying even just a single gain to a stereo signal will require around 96,000 multiply operations per second on the CPU (2 channels * 48,000 samples per second).
 - Complex plugins can have hundreds or thousands of CPU operations applied per-sample, and there are usually many plugin instances loaded at the same time in a single project.
 - Using an easier higher-level programming language with runtime-safety checks and automatic garbage collection are not [realtime safe](http://www.rossbencina.com/code/real-time-audio-programming-101-time-waits-for-nothing) because allocating/deallocating memory can take an undetermined amount of time.

## [C](https://en.wikipedia.org/wiki/C_(programming_language))
- Pros:
  - Relatively easy to learn.
  - It has a simple feature set that has pretty much stayed constant for the past several decades.
  - C compilers can be found for almost any processor in existence.
  - Fast compile times.
  - It is the closest thing you can get to writing pure assembly. It is a great way to learn more on how computers actually work.
- Cons:
  - While it is simple to learn, it is hard to properly master and use safely.
  - It is not "memory safe", meaning it is easy to accidentally create crashes, undefined behavior, and security vulnerabilities with C. This can be mitigated using an IDE with modern static-analyzing linters and debuggers, and also fuzzing tools like [AFL] and [Honggfuzz].
  - Some useful C++ features like inheritance and dynamic dispatch are much harder to do in C.
  - Dependency management can be a pain.
  - The lack of namespaces can make it more difficult to manage larger projects.
  - Uses separate header and source files. Not a problem for some, but it mildly annoys me.

## [C++](https://en.wikipedia.org/wiki/C%2B%2B)
- Pros:
  - C++ is the most commonly used programming language in the audio industry, so it is the best bet if you wish to get hired into an audio software company.
  - It has the greatest official support for audio SDKs and APIs with the largest selection of available libraries.
  - More books and tutorials on audio plugin development teach using C++.
- Cons:
  - Hard to learn and harder to properly master and use safely.
  - It is not "memory safe", meaning it is easy to accidentally create crashes, undefined behavior, and security vulnerabilities with C++. You can and should use the modern C++ features and coding standards to help reduce this risk. And the risks can be further mitigated by using an IDE with modern static-analyzing linters and debuggers, and also fuzzing tools like [AFL] and [Honggfuzz].
  - C++ is bloated with features that have been added over time. Though you should use the safer modern features over the old features, even if they are more verbose.
  - Error messages can be hard to decipher. While this has gotten *much* better over the past decade, it still isn't as good as other modern languages.
  - Dependency management can be a pain.
  - Uses separate header and source files. Not a problem for some, but it mildly annoys me. (Although C++23 is planning a solution for this.)
- Resources:
  - [Learn C++](https://www.learncpp.com/) - A fantastic free online book that thoroughly teaches modern C++ and how to use it safely and effectively.
  - [CHOC](https://github.com/Tracktion/choc) - A random grab-bag of header-only, dependency-free, liberally-licensed C++ classes.

## [D](https://dlang.org/)
- Pros:
  - D is a language inspired by C/C++, but with a more streamlined and focused feature set. It also aims to be harder to "mess something up" than C/C++.
  - Has a great open-source audio plugin development library called [DPlug].
  - Relatively easier to learn and master than C++ in my opinion.
  - It has an official dependency and build management system called "dub" that can automatically grab the needed dependencies from the web.
  - It has a built-in system for testing code.
  - Does not require a separate header/source file.
  - Fast compile times.
- Cons:
  - While it does aim to be harder to "mess something up" than C/C++, it is still susceptible to the same pitfalls if you're not careful.
  - It uses garbage collection by default (which is not "realtime safe"). It can (and should) be disabled for the DSP portion of your code, but that of course makes it less memory safe and thus requires more care and attention in those areas.
  - Library support is nowhere near the level of support that C/C++ has. (Although luckily [DPlug] is a great library for audio plugin development).

## [Rust](https://www.rust-lang.org/)
- Pros:
  - Rust is modern language that aims to avoid many of the pitfalls of C/C++ development.
  - It is "memory safe", meaning it can ensure that memory safety related crashes and security bugs cannot happen in the first place.
    - Most high-level languages are also memory safe, but they come at the cost of considerably worse performance since they use things like runtime checks and garbage collection. Rust however uses a clever system of lifetime checks and borrow restrictions that ensures safety while still allowing compiled code to run just as fast as if it was written in C/C++.
  - Easier to master than C++ in my opinion.
  - The nature of using a memory safe language reduces the amount of time you need to spend debugging & testing.
  - It has a built-in dependency and build management system called Cargo that can automatically grab the needed dependencies from the web.
  - It has a built-in system for testing code.
  - Does not use a separate header/source file (yay).
  - It has a welcoming and inclusive community.
  - There is an active open-source modular audio plugin development framework called [NIH-plug].
- Cons:
  - It can be tricky to learn, especially if you are used to other low-level languages.
  - The language is more restrictive on what you are allowed to do, and thus requires more time up-front figuring out how to structure your code to make the compiler happy (this is of course by design). You are able to use explicit "unsafe" blocks when you need more control, but that can be susceptible to the same pitfalls of C/C++ if you're not careful.
  - If you want to use safe Rust for DSP, you need to rely a lot more on the compiler to properly optimize your code. While this works most of the time, it can sometimes fail in more complex scenarios, requiring you to either restructure your code or use unsafe blocks to fix it. Also some features such as SIMD intrinsics require unsafe blocks anyway (although a solution to this is in the works called [portable-simd](https://github.com/rust-lang/portable-simd), and there are other 3rd-party SIMD crates you can try).
  - Slower compile times.
  - The language is still comparatively young, so library support such as GUIs and audio plugin development are not on the same level as C++. (There is however an active community of Rust developers working on some of these libraries. If you are interested in helping, check out the [Rust Audio Discord Server]!)
- Resources:
  - [How to learn modern Rust](https://github.com/joaocarvalhoopen/How_to_learn_modern_Rust) - An extensive list of resources for learning Rust.
  - [How-to Optimize Rust Programs on Linux](http://www.codeofview.com/fix-rs/2017/01/24/how-to-optimize-rust-programs-on-linux/) - How-to guide on profiling Rust code on Linux.
  - [Learn Rust the Dangerous Way](http://cliffle.com/p/dangerust/) - An article exploring the benefits of Rust for readers with a C background. I really love this article.
  - [Lib.rs](https://lib.rs/) - An unofficial, lightweight, opinionated, and curated alternative to crates.io.
  - [Minimizing Rust Binary Size](https://github.com/johnthagen/min-sized-rust) - Tips on how to reduce the size of Rust binaries. This is a very minor optimization, but it can sometimes be useful for shipping release versions of plugins.
    - Note, don't set `opt-level` to "s" or "z" because that will likely make performance much worse (except for maybe when running on an embedded system with little memory).
  - [Rust Audio Discord Server] - A Discord server for Rust audio programmers.
  - [Rust Book](https://doc.rust-lang.org/stable/book/) - The fantastic official online book on learning Rust.
  - [Rust By Practice](https://practice.rs/why-exercise.html) - A great unofficial online book that helps you learn Rust through exercises.
  - [The Rust Performance Book](https://nnethercote.github.io/perf-book/title-page.html) - Tips on optimizing code in Rust.

> I often get asked about beginner-friendly DSP learning resources which focus on the [Rust](https://www.rust-lang.org/) programming language. Unfortunately there isn't really anything out there. I would suggest learning DSP in another language first and then translating that knowledge to Rust later. The choice of language doesn't really matter that much for learning DSP, the main difference comes when it's time to create full applications/plugins *around* your DSP code.

# Domain Specific Languages

These languages are specifically designed to write DSP code. These can be a great alternative if you're not into writing low-level code.

- [Cmajor](https://github.com/SoundStacks/cmajor)
  - A JIT (just in time) compiled language which aims to have similar performance to C/C++.
  - Easier to learn than C/C++. However it is very similar to C, so it can be a bit harder for those who are beginners to coding.
  - Relatively new and experimental project.
  - Free and open-source.
- [CSound](https://csound.com/)
  - Easy to learn and use.
  - Well-known and long standing in the industry.
  - Free and open-source.
- [Faust](https://faust.grame.fr/)
  - A powerful functional programming language.
  - Can be transpiled into many different languages such as C++, C, Rust, and WebAssembly.
  - Free and open-source.
  - [Faust IDE](https://github.com/grame-cncm/faustide) - An online IDE than can edit, compile, and run Faust code in the browser.
  - [nih-faust-jit](https://github.com/YPares/nih-faust-jit) - A plugin that hot-reloads Faust DSP files and JIT-compiles them.
  - [rust-faust](https://github.com/Frando/rust-faust) - A library that provides easy integration between Faust and Rust. (Still a work in progress at the time of this writing.)
- [FunDSP](https://github.com/SamiPerttu/fundsp)
  - Not exactly it's own programming language, but more of a Rust library with a special (and fun) syntax.
  - While it's built on top of Rust, the library itself does not require advance Rust knowledge to use.
  - Relatively new and experimental project.
  - Free and open-source.
- [Max](https://cycling74.com/products/max/)
  - Another popular visual programming environment.
  - Proprietary.
- [Pure Data](http://puredata.info/)
  - A popular visual programming environment.
  - Free and open source.
  - [plugdata](https://github.com/plugdata-team/plugdata) - A wrapper plugin with a much nicer looking GUI.
  - [HVCC](https://github.com/Wasted-Audio/hvcc) - A tool to convert Pure Data graphs to C/C++ code.

# Languages To Look Out For

The following are newer programming languages that have the potential to be great for audio development. Keep in mind that these languages are still quite young and have a very small ecosystem compared to more well-established languages. They may not be ready yet for production.

- [Carbon](https://github.com/carbon-language/carbon-lang)
  - Aims to be compatible with existing C++ code and libraries while providing modern features, syntax, and safety.
  - Still in the early experimental stages, and it could be a few years until it's ready for use.
- [Nim](https://nim-lang.org/)
  - A modern language that combines successful concepts from mature languages like Python, Ada and Modula.
  - Compiles to native assembly and has customizable memory management.
- [Odin](https://odin-lang.org/)
  - Aims to be a modern alternative to C.
  - Not a memory-safe language, so extra precautions are needed when using it with safety checks disabled.
- [Zig](https://ziglang.org/)
  - A simple but powerful language that aims to be a modern successor to C.
  - Has no hidden control flows or allocations, and even has a built-in cross-platform SIMD library. This makes it a great fit for writing low-level realtime DSP code IMO.
  - Not a memory-safe language, so extra precautions are needed when using it with safety checks disabled.
  - There is an audio plugin framework in the works called [arbor](https://github.com/ArborealAudio/arbor).

[AFL]: https://github.com/google/AFL
[Honggfuzz]: https://github.com/google/honggfuzz
[NIH-plug]: https://github.com/robbert-vdh/nih-plug
[Rust Audio Discord Server]: https://discord.gg/Qs2Zwtf9Gf
[Dplug]: https://github.com/AuburnSounds/Dplug
