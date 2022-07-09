# Low-level Programming Languages
A list of low-level programming languages used to make audio software, along with their pros and cons.

When you want to get serious with audio DSP & audio plugin development, nothing beats writing code in a low-level programming language with manual memory management.
 - Multiplying even just a single gain to a stereo signal will require around 96,000 multiply operations per second on the CPU (2 channels * 48,000 samples per second).
 - Compound that with the fact that complex plugins can have hundreds or thousands of CPU operations applied per-sample, and there are usually many plugin instances loaded at the same time in a single project.
 - On top of that, using an easier higher-level programming language with runtime-safety checks and automatic garbage collection will create problems with latency because allocating/deallocating memory can take an undertermined amount of time (i.e. they are not "realtime safe" languages).

Here I'll list the best languages to use for serious DSP and their pros and cons:
## [`C++`]
- Pros:
  - C++ is the most commonly used programming language in the audio industry, so it is the best bet if you wish to get hired into an audio software company.
  - It has the greatest official support for audio SDKs and APIs with the largest selection of available libraries.
  - Most books and tutorials on audio plugin development teach using C++.
- Cons:
  - Hard to learn and harder to properly master and use safely.
  - It is not "memory safe", meaning it is easy to accidentally create crashes, undefined behavior, and security vulnerabilities with C++. This can be greatly mitigated using an IDE with modern static-analyzing linters and debuggers, and also fuzzing tools like [`AFL`] and [`Honggfuzz`], but that of course means added development time.
  - C++ is bloated with features that have been added over time. You should however learn to use the safer modern features over the old features, even if they are more verbose.
  - Error messages can be hard to decipher. However this has gotten *much* better over the past decade, but it still isn't perfect.
  - Dependency management can be a pain.
  - Uses separate header and source files for the same piece of code. Not a problem for some, but it midly annoys me.
- Resources:
  - [`Learn C++`] - A fantastic free online book that thouroughly teaches C++ and how to use it safely and effectively.

## [`C`]
- Pros:
  - Relatively easy to learn.
  - It has a simple feature set that has pretty much stayed constant for the past several decades.
  - C compilers can be found for almost any processor in existence.
  - Fast compile times.
  - It is the closest thing you can get to writing pure assembly. It is a great way to learn more on how computers actually work.
- Cons:
  - While it is simple to learn, it is hard to properly master and use safely.
  - It is not "memory safe", meaning it is easy to accidentally create crashes, undefined behavior, and security vulnerabilities with C. This can be greatly mitigated using an IDE with modern static-analyzing linters and debuggers, and also fuzzing tools like [`AFL`] and [`Honggfuzz`], but that of course means added development time.
  - Some useful C++ features like inheritence and dynamic dispatch are much harder to do in C.
  - Dependency management can be a pain.
  - The lack of namespaces makes it difficult to manage larger projects.
  - Uses separate header and source files for the same piece of code. Not a problem for some, but it midly annoys me.

## [`Rust`]
- Pros:
  - My personal favorite programming language ;)
  - Rust is modern language that aims to avoid many of the pitfalls of C/C++ development.
  - It is "memory safe", meaning it can ensure that whole slew of common crashes and security bugs cannot happen in the first place.
    - Most high-level languages are also memory safe, but they come at the cost of considerably worse performance since they use things like runtime checks and garbage collection. Rust however uses a clever system of lifetime and borrow restrictions that ensures safety while still allowing compiled code to run just as fast as if it was written in C/C++ (a feature known as "zero-cost abstractions").
  - Relatively easier to learn and master than C++ in my opinion.
  - The nature of using a memory safe language reduces the amount of time you need to spend debugging & testing.
  - It has a built-in dependency and build management system called Cargo that can automatically grab the needed dependencies from the web.
  - It has a built-in system for testing code.
  - Does not require a separate header/source file.
  - It has a welcoming and inclusive community.
- Cons:
  - While it is easier to learn and master than C++ in my opinion, it can still be quite tricky to get used to especially if you are used to other low-level languages.
  - The language is very restrictive on what you are able to do, and thus requires more time up-front figuring out how to structure your code to make the compiler happy (this is of course by design). You are able to use explicit "unsafe" blocks when you need more control, but that of course can be suceptible to the same pitfalls of C/C++ if you're not careful.
  - Slower compile times.
  - The language is still relatively young, so library support such as GUIs and audio plugin development are not even close to the level of support C++ has. (I am however personally working on some of these Rust audio plugin libraries. If you are interested in helping with development, please check out the [`Rust Audio Discord Server`]!)
- Resources:
  - [`Rust Book`] - The fantastic official online book on learning Rust.
  - [`Rust By Practice`] - A great unofficial online book that helps you learn Rust through excersises.
  - [`Learn Rust the Dangerous Way`] - Tips on writing low-level Rust code from a C background.
  - [`The Rust Performance Book`] - Tips on optimizing code in Rust.
  - [`How-to Optimize Rust Programs on Linux`] - How-to guide on profiling Rust code on Linux.
- Some useful crates:
  - [`baseplug`] - Create VST plugins in Rust. (GUI and other plugin formats are still a work in progress.)
  - [`basedrop`] - Memory management tools for interfacing with realtime threads.
  - [`simdeez`] - Write generic SIMD code across an array of architectures.
  - [`FunDSP`] - An audio DSP library with a nifty clean syntax.

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

[`C++`]: https://en.wikipedia.org/wiki/C%2B%2B
[`AFL`]: https://github.com/google/AFL
[`Honggfuzz`]: https://github.com/google/honggfuzz
[`Learn C++`]: https://www.learncpp.com/

[`C`]: https://en.wikipedia.org/wiki/C_(programming_language)

[`Rust`]: https://www.rust-lang.org/
[`Rust Audio Discord Server`]: https://discord.gg/Qs2Zwtf9Gf
[`Rust Book`]: https://doc.rust-lang.org/stable/book/
[`Rust By Practice`]: https://practice.rs/why-exercise.html
[`Learn Rust the Dangerous Way`]: http://cliffle.com/p/dangerust/
[`The Rust Performance Book`]: https://nnethercote.github.io/perf-book/title-page.html
[`How-to Optimize Rust Programs on Linux`]: http://www.codeofview.com/fix-rs/2017/01/24/how-to-optimize-rust-programs-on-linux/
[`baseplug`]: https://github.com/wrl/baseplug
[`basedrop`]: https://github.com/glowcoil/basedrop
[`simdeez`]: https://crates.io/crates/simdeez
[`FunDSP`]: https://github.com/SamiPerttu/fundsp

[`D`]: https://dlang.org/
[`Dplug`]: https://github.com/AuburnSounds/Dplug
