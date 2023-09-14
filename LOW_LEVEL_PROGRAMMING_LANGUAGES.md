# Low-level Programming Languages
A list of low-level programming languages used to make audio software, along with their pros and cons.

When you want to get serious with audio DSP & audio plugin development, nothing beats writing code in a low-level programming language with manual memory management.
 - Multiplying even just a single gain to a stereo signal will require around 96,000 multiply operations per second on the CPU (2 channels * 48,000 samples per second).
 - Compound that with the fact that complex plugins can have hundreds or thousands of CPU operations applied per-sample, and there are usually many plugin instances loaded at the same time in a single project.
 - On top of that, using an easier higher-level programming language with runtime-safety checks and automatic garbage collection will create problems with latency because allocating/deallocating memory can take an undetermined amount of time (i.e. they are not "realtime safe" languages).

Here I'll list the best languages to use for serious DSP and their pros and cons:
## [`C++`]
- Pros:
  - C++ is the most commonly used programming language in the audio industry, so it is the best bet if you wish to get hired into an audio software company.
  - It has the greatest official support for audio SDKs and APIs with the largest selection of available libraries.
  - More books and tutorials on audio plugin development teach using C++.
- Cons:
  - Hard to learn and harder to properly master and use safely.
  - It is not "memory safe", meaning it is easy to accidentally create crashes, undefined behavior, and security vulnerabilities with C++. You can and should use the modern C++ features and coding standards to help reduce this risk. And the risks can be further mitigated by using an IDE with modern static-analyzing linters and debuggers, and also fuzzing tools like [`AFL`] and [`Honggfuzz`].
  - C++ is bloated with features that have been added over time. Though you should use the safer modern features over the old features, even if they are more verbose.
  - Error messages can be hard to decipher. While this has gotten *much* better over the past decade, it still isn't as good as other modern languages.
  - Dependency management can be a pain.
  - Uses separate header and source files. Not a problem for some, but it mildly annoys me. (Although C++23 is planning a solution for this.)
- Resources:
  - [`Learn C++`] - A fantastic free online book that thoroughly teaches modern C++ and how to use it safely and effectively.

## [`C`]
- Pros:
  - Relatively easy to learn.
  - It has a simple feature set that has pretty much stayed constant for the past several decades.
  - C compilers can be found for almost any processor in existence.
  - Fast compile times.
  - It is the closest thing you can get to writing pure assembly. It is a great way to learn more on how computers actually work.
- Cons:
  - While it is simple to learn, it is hard to properly master and use safely.
  - It is not "memory safe", meaning it is easy to accidentally create crashes, undefined behavior, and security vulnerabilities with C. This can be mitigated using an IDE with modern static-analyzing linters and debuggers, and also fuzzing tools like [`AFL`] and [`Honggfuzz`].
  - Some useful C++ features like inheritance and dynamic dispatch are much harder to do in C.
  - Dependency management can be a pain.
  - The lack of namespaces can make it more difficult to manage larger projects.
  - Uses separate header and source files. Not a problem for some, but it mildly annoys me.

## [`Rust`]
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
  - There is an active open-source modular audio plugin development framework called [`nih-plug`].
- Cons:
  - It can be tricky to learn, especially if you are used to other low-level languages.
  - The language is more restrictive on what you are allowed to do, and thus requires more time up-front figuring out how to structure your code to make the compiler happy (this is of course by design). You are able to use explicit "unsafe" blocks when you need more control, but that can be susceptible to the same pitfalls of C/C++ if you're not careful.
  - You have to rely more on the compiler to properly optimize your code. While this works the vast majority of the time, it can sometimes fail with complex algorithms in rare cases, requiring you to restructure your code or use unsafe blocks to fix it. Also some features such as SIMD intrinsics require unsafe blocks anyway (although a solution to this is in the works called [`portable-simd`]).
  - Slower compile times.
  - The language is still relatively young, so library support such as GUIs and audio plugin development are not on the same level as C++. (There is however an active community of Rust developers working on some of these libraries. If you are interested in helping, check out the [`Rust Audio Discord Server`]!)
- Resources:
  - [`Rust Book`] - The fantastic official online book on learning Rust.
  - [`How to learn modern Rust`] - An extensive list of resources for learning Rust.
  - [`Rust By Practice`] - A great unofficial online book that helps you learn Rust through exercises.
  - [`Learn Rust the Dangerous Way`] - Tips on writing low-level Rust code from a C background.
  - [`The Rust Performance Book`] - Tips on optimizing code in Rust.
  - [`How-to Optimize Rust Programs on Linux`] - How-to guide on profiling Rust code on Linux.
  - [`Minimizing Rust Binary Size`] - Tips on how to reduce the size of Rust binaries. This is a very minor optimization, but it can sometimes be useful for shipping release versions of plugins.
    - Note, don't set `opt-level` to "s" or "z" because that will likely make performance much worse (except for maybe when running on an embedded system with little memory).

## [`D`]
- Pros:
  - D is a language inspired by C/C++, but with a more streamlined and focused feature set. It also aims to be harder to "mess something up" than C/C++.
  - Has a great open-source audio plugin development library called [`DPlug`].
  - Relatively easier to learn and master than C++ in my opinion.
  - It has an official dependency and build management system called "dub" that can automatically grab the needed dependencies from the web.
  - It has a built-in system for testing code.
  - Does not require a separate header/source file.
  - Fast compile times.
- Cons:
  - While it does aim to be harder to "mess something up" than C/C++, it is still susceptible to the same pitfalls if you're not careful.
  - It uses garbage collection by default (which is not "realtime safe"). It can (and should) be disabled for the DSP portion of your code, but that of course makes it less memory safe and thus requires more care and attention in those areas.
  - Library support is nowhere near the level of support that C/C++ has. (Although luckily [`DPlug`] is a great library for audio plugin development).

> A new language to look out for is [`Carbon`], which aims to be compatible with existing C++ code and libraries while providing modern features, syntax, and safety. It has the potential to be a great language for audio development. Though it's still in the early experimental stages, and it could be a few years until it's ready for use.

[`C++`]: https://en.wikipedia.org/wiki/C%2B%2B
[`AFL`]: https://github.com/google/AFL
[`Honggfuzz`]: https://github.com/google/honggfuzz
[`Learn C++`]: https://www.learncpp.com/

[`C`]: https://en.wikipedia.org/wiki/C_(programming_language)

[`Rust`]: https://www.rust-lang.org/
[`Rust Audio Discord Server`]: https://discord.gg/Qs2Zwtf9Gf
[`nih-plug`]: https://github.com/robbert-vdh/nih-plug
[`portable-simd`]: https://github.com/rust-lang/portable-simd
[`Rust Book`]: https://doc.rust-lang.org/stable/book/
[`How to learn modern Rust`]: https://github.com/joaocarvalhoopen/How_to_learn_modern_Rust
[`Rust By Practice`]: https://practice.rs/why-exercise.html
[`Learn Rust the Dangerous Way`]: http://cliffle.com/p/dangerust/
[`The Rust Performance Book`]: https://nnethercote.github.io/perf-book/title-page.html
[`How-to Optimize Rust Programs on Linux`]: http://www.codeofview.com/fix-rs/2017/01/24/how-to-optimize-rust-programs-on-linux/
[`Minimizing Rust Binary Size`]: https://github.com/johnthagen/min-sized-rust

[`D`]: https://dlang.org/
[`Dplug`]: https://github.com/AuburnSounds/Dplug

[`Carbon`]: https://github.com/carbon-language/carbon-lang