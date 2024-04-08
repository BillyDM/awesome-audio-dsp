# DSP Playgrounds

A list of software tools that are useful for quickly and easily prototyping DSP. These can be a great start for learning and experimenting with DSP for those with little or no programming experience.

## Codeless

- [Alpha Forever](https://www.afmodular.com/)
  - A Reaktor-like environment for creating DSP without code.
  - Commercial software that is $80 USD at the time of this writing. Although the free demo lets you use all the features, just without the ability to save.
  - Windows only.
- [Reaktor 6](https://www.native-instruments.com/en/products/komplete/synths/reaktor-6/) by Native Instruments
  - A popular modular environment for creating DSP without code.
  - Has a sizeable community.
  - Full version is expensive at $200 USD at the time of this writing. Free version is limited in functionality.
  - Mac and Windows only. Although some have had success running it in Linux using Wine.
- [The Grid](https://www.bitwig.com/the-grid/) by Bitwig Studio
  - A built-in Reaktor-like plugin environment tightly integrated with the highly modular Bitwig Studio DAW.
  - Highly intuitive to use.
  - Requires Bitwig Studio, which is a whopping $400 USD at the time of this writing. However, the demo version lets you use all the features, just without the ability to save.
  - Sound quality is not the greatest.
  - Runs on Linux, Mac, and Windows.
- [VCV Rack](https://vcvrack.com/)
  - A fully modular software environment that simulates the analogue Eurorack environment.
  - Popular with a sizeable community.
  - Arguably more "plugin"-like than actual DSP, but concepts still translate to DSP skills.
  - Free and open source.
  - Runs on Linux, Mac, and Windows.

## Easy Code

- [Cmajor](https://github.com/SoundStacks/cmajor)
  - A JIT (just in time) compiled language specifically designed for DSP. It aims to have performance similar to C/C++.
  - Easier to learn than C/C++. However it is very similar to C, so it can be a bit harder for those who are beginners to coding.
  - Relatively new and experimental project.
  - Free and open-source.
- [CSound](https://csound.com/)
  - A custom scripting language that is easy to learn and use.
  - Well-known and long standing in the industry.
  - Free and open-source.
- [Faust](https://faust.grame.fr/)
  - A powerful functional programming language.
  - Can be transpiled into many different languages such as C++, C, Rust, and WebAssembly.
  - Free and open-source.
  - [nih-faust-jit](https://github.com/YPares/nih-faust-jit) - A plugin that hot-reloads Faust dsp files and JIT-compiles them.
- [FunDSP](https://github.com/SamiPerttu/fundsp)
  - A neat project for learning and prototyping DSP.
  - Uses the Rust programming language, so it is not for those who are beginners to coding. However, the library itself does not require advance Rust skills.
  - Relatively new and experimental project.
  - Free and open-source.
- [Maximilian.js](https://mimicproject.com/guides/maximJS)
  - Javascript bindings to the Maximilian DSP library.
  - Javascript can be great for those who are just learning to code, and it can be ran inside a web browser.
  - Free and open source.
- [py-modular](http://py-modular.readthedocs.io/)
  - A modular and experimental programming environment with basic DSP routines.
  - Uses the very popular Python programming language, which is a great those who are learning to code.
  - Relatively new and experimental project.
  - Free and open-source.
- [SuperCollider]
  - A platform for audio synthesis and algorithmic composition.
  - Free and open-source.
- [Tidal Cycles](https://tidalcycles.org/)
  - A platform for audio synthesis and algorithmic composition, built on top of [SuperCollider].
  - Free and open-source.

## Visual Code

- [Max](https://cycling74.com/products/max/)
  - Another popular visual programming language.
  - Originally developed in the 1980s at IRCAM by Miller Puckette.
  - Proprietary.
- [Pure Data](http://puredata.info/)
  - Another popular visual programming language.
  - Also developed by Miller Puckette in the 1990s as an open-source project.
  - Early on, some parts were ported to Max which became Max/MSP.
  - Free and open source under BSD-3-Clause.
  - [plugdata](https://github.com/plugdata-team/plugdata) - A wrapper plugin with a much nicer looking GUI.
  - [HVCC](https://github.com/Wasted-Audio/hvcc) - A tool to convert Pure Data graphs to C/C++ code.

[SuperCollider]: https://supercollider.github.io/