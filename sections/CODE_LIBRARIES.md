# Code Libraries

A list of useful libraries for audio software.

# Cross-platform System Audio I/O

- [JUCE]
    - C++ only
    - Native duplex audio support
    - Graceful error handling *
    - Linux, Mac, Windows, iOS, and Android
    - GPLv3 license if your application is GPLv3, otherwise requires a paid license
- [RtAudio](https://github.com/thestk/rtaudio)
    - C++, C, Go, Python, and Rust (via [rtaudio-rs](https://github.com/BillyDM/rtaudio-rs))
    - Native duplex audio support
    - Graceful error handling *
    - Linux, Mac, and Windows
    - MIT license
- [PortAudio](https://github.com/PortAudio/portaudio)
    - C, C++, Go, Rust (via [weresocool_portaudio](https://crates.io/crates/weresocool_portaudio)), and Python (via [PyAudio](https://pypi.org/project/PyAudio/))
    - Native duplex audio support
    - Linux, Mac, and Windows
    - MIT license
- [libsoundio](https://github.com/andrewrk/libsoundio)
    - C, C++, and Rust (unsafe bindings via [soundio-sys](https://crates.io/crates/soundio-sys))
    - Graceful error handling *
    - Linux, Mac, and Windows
    - MIT license
- [CPAL](https://crates.io/crates/cpal)
    - Rust only
    - Graceful error handling *
    - Linux, Mac, Windows, iOS, Android, and Emscripten (WebAssembly)
    - Apache 2.0 license

> \* By "graceful error handling", I mean the ability to gracefully deal with any errors encountered while the audio stream is running (i.e. a device was unplugged).

# Cross-platform System MIDI I/O

- [JUCE]
- [RtMidi](https://github.com/thestk/rtmidi)
- [PortMidi](https://github.com/PortMidi/PortMidi)
- [midir](https://crates.io/crates/midir) (Rust only)

# Audio File Decoding/Encoding

- [FFmpeg](https://ffmpeg.org/) (Rust bindings via [ac-ffmpeg](https://crates.io/crates/ac-ffmpeg))
- [Symphonia](https://github.com/pdeljanov/Symphonia)
- [miniaudio](https://github.com/mackron/miniaudio) (Rust bindings via [om-fork-miniaudio](https://crates.io/crates/om-fork-miniaudio))
- [dr_libs](https://github.com/mackron/dr_libs)
- [minimp3](https://github.com/lieff/minimp3)
- [Xiph repositories](https://github.com/xiph) - Contains various open source media codecs and containers such as Opus, FLAC, Vorbis, and OGG

# DSP Libraries

A list of ready-made libraries for DSP.

Please note, while using ready-made libraries can definitely help you achieve faster results as a beginner, I don't actually recommend depending on them in the long term. Not just because it may be considered "cheat-y" by some, but the generic nature of these libraries can make it harder to tweak and optimize. Writing your own DSP code allows you to more easily experiment with and tweak algorithms to add your own special "character" to them. DSP that is purpose-built for a single purpose will generally both sound better and perform better than a generic library that tries to cover all bases.

Also beware that some of these libraries have licenses attached to them, so make sure you are legally allowed to use them in your products.

That being said, it can still be a great resource for learning about various DSP algorithms and how they are implemented in code, so I listed some here.

- [SST Filters](https://github.com/surge-synthesizer/sst-filters), [SST Waveshapers](https://github.com/surge-synthesizer/sst-waveshapers), [SST Oscillators](https://github.com/surge-synthesizer/sst-oscillators-mit), [SST Effects](https://github.com/surge-synthesizer/sst-effects), [SST Basic Blocks](https://github.com/surge-synthesizer/sst-basic-blocks) - Various DSP algorithms used by the [Surge Synthesizer Team](https://surge-synth-team.org/)
- [synfx-dsp](https://github.com/WeirdConstructor/synfx-dsp) - A comprehensive DSP library in Rust, used by the [HexoSynth] synthesizer plugin.
- [HexoDSP](https://github.com/WeirdConstructor/HexoDSP) - A comprehensive modular DSP and audio graph library also used by the [HexoSynth] synthesizer plugin.
- [chowdsp_wdf](https://github.com/Chowdhury-DSP/chowdsp_wdf) - A header only C++ library for implementing real-time Wave Digital Filter (WDF) circuit models.
- [FunDSP](https://github.com/SamiPerttu/fundsp) - A Rust DSP crate with a unique and fun syntax.
- [Moog Ladder Filters](https://github.com/ddiakopoulos/MoogLadders) - Contains different digital implementations of the classic 4-pole, 24 dB/octave analog filter.
- [Meadowlark Audio Filters](https://github.com/MeadowlarkDAW/audio-filters) - An incomplete collection of audio filters that was once planned for use within the internal plugins for my own Meadowlark project. Although because I don't really condone generic DSP libraries, my plugins will probably not actually reference this library. Rather I just keep this repository around as a reference.
- [signalo](https://github.com/signalo/signalo) - A Rust DSP toolbox with focus on embedded environments.
- [juce_dsp](https://docs.juce.com/master/group__juce__dsp.html) - A set of DSP classes that are included with the JUCE library. There is also an introductory [tutorial](https://docs.juce.com/master/tutorial_dsp_introduction.html) on using these libraries (as well as JUCE in general).
- [KFR](https://kfrlib.com/) - A collection of very fast DSP algorithms. Commercial use requires a paid license.
- [Maximilian](https://github.com/micknoise/Maximilian) - A comprehensive collection of DSP algorithms in C++. Also contains Javascript bindings.
- [Q](https://github.com/cycfi/q) - A DSP library that leverages features of modern C++.
- [DaisySP](https://github.com/electro-smith/DaisySP) - A C++ DSP library that provides a comprehensive collection of modular components.
- [SOUL-VA](https://github.com/thezhe/SOUL-VA) - A collection of virtual analog audio effects for the [SOUL](https://github.com/soul-lang/SOUL) programming language.
- [DSP Filters by vinniefalco](https://github.com/vinniefalco/DSPFilters) - A collection of C++ classes for DSP.
- [Bad Circuit Modeling](https://github.com/jatinchowdhury18/Bad-Circuit-Modelling) - Contains analogue models of non-ideal circuits.
- [DSP filters in C++ by dimtass](https://github.com/dimtass/DSP-Cpp-filters) - A collection of DSP biquad filters.

[JUCE]: https://juce.com/
[Hexosynth]: https://github.com/WeirdConstructor/HexoSynth
