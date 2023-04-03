# DSP Libraries
A list of ready-made libraries for DSP.

Please note, while using ready-made libraries can definitely help you achieve faster results as a beginner, I don't actually recommend relying on them. Not just because it may be considered "cheaty" by some, but using generic DSP libraries makes it harder to optimize performance, and it makes it harder to experiment with and tweak algorithms to your liking to add your own custom flair to them. DSP that is purpose-built for a single purpose will generally sound better and perform better than a generic library that tries to cover all bases.

Also beware that some of these libraries have licenses attached to them, so make sure you are legally allowed to use them in your products.

That being said, it can still be a great resource for learning about various DSP algorithms and how they are implemented in code, so I listed some here.

- [`DSP Filters by vinniefalco`](https://github.com/vinniefalco/DSPFilters) - A collection of C++ classes for DSP.
- [`chowdsp_wdf`](https://github.com/Chowdhury-DSP/chowdsp_wdf) - A header only C++ library for implementing real-time Wave Digital Filter (WDF) circuit models.
- [`synfx-dsp`](https://github.com/WeirdConstructor/synfx-dsp) - A comprehensive DSP library in Rust, used by the [`HexoSynth`] synthesizer plugin.
- [`HexoDSP`](https://github.com/WeirdConstructor/HexoDSP) - A comprehensive modular DSP and audio graph library also used by the [`HexoSynth`] synthesizer plugin.
- [`FunDSP`](https://github.com/SamiPerttu/fundsp) - A Rust DSP crate with a unique and fun syntax.
- [`Moog Ladder Filters`](https://github.com/ddiakopoulos/MoogLadders) - Contains different digital implementations of the classic 4-pole, 24 dB/octave analog filter.
- [`Meadowlark Audio Filters`](https://github.com/MeadowlarkDAW/audio-filters) - An incomplete collection of audio filters that was once planned for use within the internal plugins for my own Meadowlark project. Although because I don't really condone generic DSP libraries, my plugins will probably not actually reference this library. Rather I just keep this repository around as a reference.
- [`signalo`](https://github.com/signalo/signalo) - A Rust DSP toolbox with focus on embedded environments.
- [`juce_dsp`](https://docs.juce.com/master/group__juce__dsp.html) - A set of DSP classes that are included with the JUCE library. There is also an introductory [`tutorial`](https://docs.juce.com/master/tutorial_dsp_introduction.html) on using these libraries (as well as JUCE in general).
- [`KFR`](https://kfrlib.com/) - A collection of very fast DSP algorithms. Commercial use requires a paid license.
- [`Maximilian`](https://github.com/micknoise/Maximilian) - A comprehensive collection of DSP algorithms in C++. Also contains Javascript bindings.
- [`Q`](https://github.com/cycfi/q) - A DSP library that leverages features of modern C++.
- [`SOUL-VA`](https://github.com/thezhe/SOUL-VA) - A collection of virtual analog audio effects for the [`SOUL`](https://github.com/soul-lang/SOUL) programming language.
- [`Bad Circuit Modeling`](https://github.com/jatinchowdhury18/Bad-Circuit-Modelling) - Contains analogue models of non-ideal circuits.
- [`DSP filters in C++ by dimtass`](https://github.com/dimtass/DSP-Cpp-filters) - A collection of DSP biquad filters.

[`Hexosynth`]: https://github.com/WeirdConstructor/HexoSynth
