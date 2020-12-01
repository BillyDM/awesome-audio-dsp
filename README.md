# Audio DSP Resources
My curated list of audio digital signal processing resources. New resources may be added in the future. Feel free to open a PR if you wish!

## Textbooks
- [`Designing Software Synthesizer Plug-Ins in C++`] and [`Designing Audio Effect Plugins in C++`] by Will Pirkle
  - Great beginner resource that teaches fundamental DSP concepts with examples.
  - Focuses on teaching concepts, not on writing performant code. His coding sytle is quite ineffecient.

- [`The Scientist and Engineer's Guide to Digital Signal Processing`] by Steven W. Smith, Ph.D.
  - Free online book on DSP in general.

## Mathematics
- [`3Blue1Brown`] - An excellent YouTube channel on complex algebra, linear algebra, calculus, and differential equations.
  - His videos on [`Euler's Formula`] and the [`Fourier Transform`] are particularly excellent.
- This video on the [`Laplace Transform`] by Zach Star.

## Algorithms & Technical Reading
- [`Musicdsp.org`] - A collection of open source DSP algorithms by the community.
- [`Cytomic Technical Papers`] - Excellent real-world useable filters and explanations by Cytomic.
- [`deip.pdf`] - High quality resampling and oversampling.
- [`Freeverb`] - An open-source reverb algorithm.
- [`DAFx`] - An archive of scientific papers and presentations given during an annual DSP research conference.

## Sound Design & Mixing
While this is not *strictly* development related, knowing how plugins are actually used can give valuable insight.
- [`SeamlessR`] - This guy is a great teacher and really knows his stuff.
- [`Au5`] - A beast legend. Need I say more?

## Software Optimization
- [`Intel Intrinsics Guide`] - x86 processor instrinsics
- Follow these rules:
  ![DSP Rules](fast_dsp.png?raw=true)

## Math Tools
- [`Desmos`] - Free online graphing calculator.
- [`Wolfram Alpha`] - A helpful math partner.
- [`Curcuit JS`] - A cool little circuit simulation tool.

## System Tools
- [`MrsWatson`] - Command-line audio plugin host with support for printing to the terminal from your DSP code.
- [`Carla`] - System-wide virtual audio and MIDI patching software, using [`Jack`] as the backend. Available as a standalone application or a VST/LV2 plugin.
- [`Jack`] - Cross-platform audio driver with support for system-wide patching.
- [`Cadence`] - A suite of tools for configuring, monitoring, and controlling system-wide audio in Linux (includes [`Carla`]).
- [`Ardour`] - Open-source DAW with useful plugin analysis tools.
- [`Bertom EQ Curve Analyzer`] - Analyze the frequency and phase response of any plugin.

## Rust Crates
- [`baseplug`] - Create VST plugins in Rust. (GUI and other plugin formats are still a work in progress.)
- [`simdeez`] - Write generic SIMD code across an array of architectures.
- [`FunDSP`] - An audio DSP library with a nifty clean syntax.

## Rust Resources
- [`Learn Rust the Dangerous Way`] - Tips on writing low-level Rust code from a C background.
- [`How-to Optimize Rust Programs on Linux`] - How-to guide on profiling Rust code on Linux.

## Forums
- [`Rust Audio Discord Server`] - A community of passionate Rust audio programmers.
- [`KVR DSP Forum`] - A large community of plugin developers.

[`Designing Software Synthesizer Plug-Ins in C++`]: https://www.amazon.com/Designing-Software-Synthesizer-Plug-Ins-RackAFX/dp/1138787078
[`Designing Audio Effect Plugins in C++`]: https://www.amazon.com/Designing-Audio-Effect-Plugins-C/dp/1138591939
[`The Scientist and Engineer's Guide to Digital Signal Processing`]: http://www.dspguide.com/pdfbook.htm
[`3Blue1Brown`]: https://www.youtube.com/channel/UCYO_jab_esuFRV4b17AJtAw
[`Musicdsp.org`]: https://www.musicdsp.org/en/latest/index.html
[`Intel Intrinsics Guide`]: https://software.intel.com/sites/landingpage/IntrinsicsGuide/#!=undefined
[`simdeez`]: https://crates.io/crates/simdeez
[`FunDSP`]: https://github.com/SamiPerttu/fundsp
[`Learn Rust the Dangerous Way`]: http://cliffle.com/p/dangerust/
[`How-to Optimize Rust Programs on Linux`]: http://www.codeofview.com/fix-rs/2017/01/24/how-to-optimize-rust-programs-on-linux/
[`Cytomic Technical Papers`]: https://cytomic.com/index.php?q=technical-papers
[`Freeverb`]: https://ccrma.stanford.edu/~jos/pasp/Freeverb.html
[`Rust Audio Discord Server`]: https://discord.com/channels/590254806208217089/590657587939115048
[`Desmos`]: https://www.desmos.com/calculator
[`Wolfram Alpha`]: https://www.wolframalpha.com/
[`Curcuit JS`]: https://www.falstad.com/circuit/circuitjs.html
[`Fourier Transform`]: https://www.youtube.com/watch?v=spUNpyF58BY
[`Euler's Formula`]: https://www.youtube.com/watch?v=mvmuCPvRoWQ
[`Laplace Transform`]: https://www.youtube.com/watch?v=n2y7n6jw5d0
[`deip.pdf`]: https://github.com/BillyDM/Audio-DSP-Resources/blob/main/deip.pdf
[`MrsWatson`]: http://teragonaudio.com/MrsWatson.html
[`Jack`]: https://jackaudio.org/
[`Carla`]: https://kx.studio/Applications:Carla
[`Cadence`]: https://kx.studio/Applications:Cadence
[`Ardour`]: https://ardour.org/
[`baseplug`]: https://github.com/wrl/baseplug
[`SeamlessR`]: https://www.youtube.com/playlist?list=PLGYoE903Nir5LfIWap-x8aEV6Q-YkE6c4
[`Au5`]: https://www.youtube.com/playlist?list=PLCP_w7OAVom-d5SMebEPdwrkiNNGCv53N
[`Bertom EQ Curve Analyzer`]: https://www.bertomaudio.com/eqca.html
[`KVR DSP Forum`]: https://www.kvraudio.com/forum/viewforum.php?f=33
[`DAFx`]: http://www.dafx.de/
