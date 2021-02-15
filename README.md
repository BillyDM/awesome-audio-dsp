# Awesome Audio DSP
My curated list of audio DSP (digital signal processing) and plugin development resources. New resources may be added in the future. Feel free to open a PR if you wish!

## More Lists
Here I'll link curated lists that others have made.
- [`dsp-learning`] by crsaracco
- [`Awesome Rust Audio`] by kfrncs
- [`Useful Links for DSP and Audio Programming`] from rust.audio

## Free Online Textbooks
- [`The Scientist and Engineer's Guide to Digital Signal Processing`] by Steven W. Smith, Ph.D.
  - A common recommendation from many folks.
  - Focuses on DSP in general, not just audio DSP.

- [`The Art of VA Filter Design`] by Vadim Zavalishin
  - Teaches good techniques for adapting analogue designs into the digital realm.
  - Relatively heavy on mathematics.

- [`Julius Orion Smith III Collection`]
  - A collection of books and resources by Julius Orion Smith III.
  - Relatively heavy on mathematics.

- [`The Theory and Technique of Electronic Music`] by Miller Puckette
  - Focuses more on musical DSP.
  - Relatively heavy on mathematics.

## Paid Textbooks
- [`Designing Software Synthesizer Plug-Ins in C++`] and [`Designing Audio Effect Plugins in C++`] by Will Pirkle
  - One of the most highly recommended resources for entering the world of audio DSP.
  - Great beginner resource that teaches fundamental DSP concepts with examples.
  - The synthesizer one is better than the effect one imo, so go for that if you plan on only buying one.
  - Focuses on teaching concepts, not on writing performant code. His coding sytle is quite ineffecient.
  - There will also be [`newer edition`] in 2021 as well.

- [`A Digital Signal Processing Primer`] by Kenneth Steiglitz
  - Great introduction to the mathematics of DSP.
  - Focuses more and mathematics and does not have many example effects.

- [`DAFX: Digital Audio Effects`] by Udo Zölzer (Editor)
  - Explores good modern advanced effects. It's made by the [`DAFx`] annual scientific research conference.
  - MATLAB is used for its code examples, so stomach that if you can.

- [`Digital Signal Processing: Concepts and Applications`] by Mulgrew, Grant & Thompson
  - Covers the basic principles of DSP in an easy-to-digest way without going into too much mathematics.
  - Focuses more on general DSP rather than audio DSP.
  - Also uses MATLAB for its code examples.

## Mathematics
- [`3Blue1Brown`] - An excellent YouTube channel on complex algebra, linear algebra, calculus, and differential equations.
  - His videos on [`Euler's Formula`] and the [`Fourier Transform`] are particularly excellent.
- [`Paul's Online Math Notes`] - Excellent resources written and used by a professor at Lamar University.
- [`Paul's Cheat Sheets`] - Cheat sheets for many common identities and formulas in algebra, trig, calculus, and laplace transformations. Because who can remeber all this stuff?
- [`katjaas`] - Neat visual explanations of DSP mathematics and techniques.
- This video on the [`Laplace Transform`] by Zach Star.
- [`Khan Academy`] - Free college-level courses.

## Algorithms & Technical Reading
- [`Musicdsp.org`] - A collection of open source DSP algorithms by the community.
- [`Cytomic Technical Papers`] - Excellent real-world useable filters and explanations by Cytomic.
- [`deip.pdf`] - High quality resampling and oversampling.
- [`Freeverb`] - An open-source reverb algorithm.
- [`DAFx`] - An archive of scientific papers and presentations given during an annual DSP research conference.
- [`katjaas`] - Neat visual explanations of DSP mathematics and techniques.
- [`Jatin Chowdhury`] - An active blog that explores cutting-edge DSP techniques.
- [`The Design of the Roland Juno oscillators`] - A beautiful and simple explanation on the oscillators of this classic synth.

## Open Source Plugins & Software
Reading the source code of real-world projects can give valueable insight into different techniques and solutions people have come up with over the years.
### Collections
- [`Airwindows Plugins`] - Many, many good quality effects and experiments developed over many years.
  There are a *ton* of plugins here, so here is a list of community favorites:
  - [`density`]
  - [`pressure4`]
  - [`totape5`]
  - [`ironoxide`]
- [`LSP Plugins`] - A collection of high quality mixing effects.
- [`sjaehn`] - Several cool MIDI based slicing/glitching effects and synthesizers.
- [`x42-plugins`] - A collection of good quality effects and visualizers. Some plugins are also sold as a commercial product.
- [`EQ10Q`] - A suite of plugins containing a 10-band parametric equalizer, gate, compressor, bass enhancer, and mid-side encoders.
- [`DISTRHO Plugin Framework`] - A bunch more open-source plugins are listed here.
- [`lkjb plugins`] - Additional plugins made by the creator of [`Luftikus`].
### Synths
- [`Helm`] - High-quality modern synthesizer with a flexible modulation system. The oscillators are not stereo though.
- [`Surge`] - Feature-rich hybrid synthesizer that was once sold as a commercial product.
- [`Dexed`] - Synthesizer closely modelled after the Yamaha DX7.
- [`ZynAddSubFX`] - Feature-rich additive synthesizer with a great clean sound. Also sold as a commercial product.
- [`Odin 2`] - Modern analogue-modeled hybrid synthesizer.
- [`Geonkick`] - Advanced drum synthesizer.
- [`ADLplug`] - Emulation of FM-synthesizers found in some classic game consoles.
- [`Ninjas 2`] - Sample slicer and player.
### Audio FX
- [`Wolf Shaper`] - Good quality waveshaper with support for unlimited nodes.
- [`Mverb`] - Nice-sounding plate reverb.
- [`Dragonfly Reverb`] - Algorithmic reverb based on [`Freeverb`].
- [`CloudReverb`] - Beautiful shimmering reverb based on the `CloudSeed` plugin by Valdemar Erlingsson. I choose this over the original as that uses a Windows-only C# platform for its GUI.
- [`Luftikus`] - Good quality analogue modeled equalizer.
- [`Fogpad`] - Reverb plugin where reflections can be frozen, filtered, pitch-shifted, and mangled.
- [`Misstortion`] - Good quality hard/soft clipper.
### MIDI FX
- [`Helio Workstation`] - A very modern and feature-rich sequencer.
- [`QMidiArp`] - Advanced arpeggiator, sequencer, and MIDI LFO.
### Meters & Visualizers
- [`Spectacle`] - Modern real-time spectrum analyzer plugin.
- [`Wolf Spectrum`] - Real-time heat-map spectrum analyzer plugin.
- [`EasySSP`] - Real-time spectrum analyzer and stereo analyzer plugin.
- [`LUFS Meter`] - Real-time loudness meter with support for several international loudness standards.
### DAWs & Hosts
- [`Ardour`] - Feature-rich DAW. Focuses more on recorded music production over electronic music production.
- [`LMMS`] - Feature-rich DAW focused on electronic music production. Contains many built-in synths and effects.
- [`Audacity`] - Popular multi-track audio editor.
- [`Carla`] - Cross platform plugin host with support for many plugin formats.

## Sound Design, Arrangement, & Mixing
While this is not *strictly* development related, knowing how plugins are actually used can give valuable insight.
- [`Mixing Secrets for the Small Studio`] - A great beginner resource on mixing fundamentals.
- [`SeamlessR`] - This guy is a fantastic teacher and really knows his stuff.
- [`How to Hear Compression`] - A brilliant video that teaches how to "hear" compressors from an artistic point of view, rather than a technical one.
- [`Au5`] - A beast legend. Need I say more?
- [`Virtual Riot`] - Another beast legend.
- [`Zircon`] - An underrated artist, and I'm personally a huge fan of his more organic, jazzy breakbeat style. Great if you're tired of loud and obnoxious "dubstep" sound design and production.
- [`Nosia`] - He and another cutting edge sound designer have a tutorial series on their Patreon.
- [`Mr. Bill`] - This guy has a lot of good tutorials on his channel.
- [`Nigel Good`] - This guy makes sounds that are *so* clean.
- [`Frequent`] - Good sound design & arrangment tutorials.
- [`Crow`] - Good tutorials on sound design and mixing.

## Software Optimization
- [`Fast-DSP-Approximations`] - My own list of public-domain fast approximations of various expensive calculations.
- [`Intel Intrinsics Guide`] - x86 processor instrinsics
- [`Real-time audio programming 101`] - Tips on writing real-time code.
- [`The Rust Performance Book`] - Tips on optimizing code in Rust.
- Follow these rules:
  ![DSP Rules](fast_dsp.png?raw=true)

## Math Tools
- [`Desmos`] - Free online graphing calculator.
- [`Wolfram Alpha`] - A helpful math partner.
- [`Symbolab`] - Another helpful math partner.
- [`Octave`] - An open-source alternative to MATLAB.
- [`Curcuit JS`] - A cool little circuit simulation tool.

## System Tools
- [`MrsWatson`] - Command-line audio plugin host with support for printing to the terminal from your DSP code.
- [`Carla`] - System-wide virtual audio and MIDI patching software, using [`Jack`] as the backend. Available as a standalone application or a VST/LV2 plugin.
- [`Jack`] - Cross-platform audio driver with support for system-wide patching.
- [`Cadence`] - A suite of tools for configuring, monitoring, and controlling system-wide audio in Linux (includes [`Carla`]).
- [`Ardour`] - Open-source DAW with useful plugin analysis tools.
- [`Bertom EQ Curve Analyzer`] - Analyze the frequency and phase response of any plugin.
- [`pluginval`] - Cross-platform open-source plugin validation tool made by the company Tracktion.

## Plugin Development Frameworks
- Rust Community Framework
  - Full-stack modular framework in Rust (currently a WIP and not production ready yet). I'm personally biased towards this as one of the main contributors.
  - [`baseplug`] - Provides an abstraction-layer over the different plugin formats, and simplifies parameter management.
    - Does not contain a GUI framework, but other frameworks can be attached to provide the GUI.
    - Currently only targets the VST2 plugin format. VST3, AU, LV2, and JACK targets are currently planned.
    - Targets Mac, Windows, and Linux platforms.
  - [`baseview`] - Provides windowing and input events for plugins / standalone applications.
    - Targets Mac, Windows, and Linux.
  - [`iced_baseview`] - Provides the [`iced`] GUI framework on top of [`baseview`].
    - Targets Mac, Windows, and Linux.
  - [`iced_audio`] - An extension to the [`iced`] GUI framework that provides audio-specific widgets like knobs and sliders.
  - [`iced-baseplug-examples`] - Example plugins built using the [`baseplug`], [`iced_baseview`], and [`iced_audio`] modules.
  - [`goldenrod`] - A personal raster-based GUI framework built on top of [`baseview`]. Currently very WIP and experimental.
    - Targets Mac, Windows, and Linux.
- [`DISTRHO Plugin Framework`]
  - Full-stack framework with GUI in C++. Fully open-source.
  - Targets LADSPA, DSSI, LV2, VST2, and Jack plugin formats.
  - Targets Mac, Windows, and Linux platforms.
- [`Dplug`]
  - Full-stack framework with GUI in te D programming language (if you're into that sort-of thing).
  - The GUI framework has fancy physically-modeled rendering inspired by game engines.
  - Targets VST2, VST3, AUv2, AAX, and LV2 plugin formats.
  - Targets Mac, Windows, Linux, and Raspberry Pi platforms.
  - Used by several commercial plugins.
- [`JUCE`]
  - Full-stack framework with GUI in C++. Open source, but some of its modules require a hefty commercial license to use.
  - Targets VST2, VST3, AUv2, AUv3, RTAS, and AAX plugin formats.
  - Targets Mac, Windows, Linux, iOS, Android, and Raspberry Pi platforms.
  - Well known, and many commercial plugins are built with it.
- [`Tracktion Engine`]
  - Full-stack framework in C++ with GUI. It is built on top of [`JUCE`].
  - Targeted formats and platforms are the same as [`JUCE`].
  - Made and used by the commercial company Tracktion.
- [`iPlug2`]
  - Full-stack framework in C++ with GUI. Fully open-source.
  - Targets VST2, VST3, AUv2, AUv3, AAX and the Web Audio Module (WAM) plugin formats.
  - Targets Mac, Windows, iOS, and Web. It does not target Linux, so I'm personally not a fan of this one.

## Rust Crates
- [`baseplug`] - Create VST plugins in Rust. (GUI and other plugin formats are still a work in progress.)
- [`simdeez`] - Write generic SIMD code across an array of architectures.
- [`FunDSP`] - An audio DSP library with a nifty clean syntax.

## Rust Resources
- [`Learn Rust the Dangerous Way`] - Tips on writing low-level Rust code from a C background.
- [`How-to Optimize Rust Programs on Linux`] - How-to guide on profiling Rust code on Linux.
- [`The Rust Performance Book`] - Tips on optimizing code in Rust.

## Forums
- [`Rust Audio Discord Server`] - A community of passionate Rust audio programmers.
- [`The Audio Programmer Discord Server`] - Another Discord community for audio programmers using any programming languages, not just Rust.
- [`Rust Community Discord Server`] - Not strictly DSP related, but the people there can help you with any Rust questions.
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
[`Rust Audio Discord Server`]: https://discord.gg/Qs2Zwtf9Gf
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
[`newer edition`]: https://www.amazon.com/Designing-Software-Synthesizer-Plug-Ins-Audio/dp/0367510480
[`DAFX: Digital Audio Effects`]: https://www.amazon.com/DAFX-Digital-Effects-Udo-Z%C3%B6lzer/dp/0470665998
[`The Theory and Technique of Electronic Music`]: http://msp.ucsd.edu/techniques.htm
[`Julius Orion Smith III Collection`]: https://ccrma.stanford.edu/~jos/
[`A Digital Signal Processing Primer`]: https://www.amazon.com/Digital-Signal-Processing-Primer-Applications/dp/0486845834
[`Helm`]: https://github.com/mtytel/helm
[`Surge`]: https://github.com/surge-synthesizer/surge
[`Dexed`]: https://github.com/asb2m10/dexed
[`ZynAddSubFX`]: https://github.com/zynaddsubfx/zynaddsubfx
[`Wolf Shaper`]: https://github.com/pdesaulniers/wolf-shaper
[`Mverb`]: https://github.com/DISTRHO/MVerb
[`Dragonfly Reverb`]: https://github.com/michaelwillis/dragonfly-reverb
[`CloudReverb`]: https://github.com/xunil-cloud/CloudReverb
[`Odin 2`]: https://github.com/TheWaveWarden/odin2
[`Spectacle`]: https://github.com/jpcima/spectacle
[`ADLplug`]: https://github.com/jpcima/ADLplug
[`LMMS`]: https://github.com/LMMS/lmms
[`Audacity`]: https://github.com/audacity/audacity
[`Wolf Spectrum`]: https://github.com/pdesaulniers/wolf-spectrum
[`Misstortion`]: https://github.com/nimbletools/misstortion1
[`DISTRHO Plugin Framework`]: https://github.com/DISTRHO/DPF
[`JUCE`]: https://github.com/juce-framework/JUCE
[`DISTRHO Mini-Series`]: https://github.com/DISTRHO/Mini-Series
[`NDC Plugs`]: https://github.com/DISTRHO/ndc-Plugs
[`Fogpad`]: https://github.com/linuxmao-org/fogpad-port
[`Ninjas 2`]: https://github.com/clearly-broken-software/ninjas2
[`Stone Phaser`]: https://github.com/jpcima/stone-phaser
[`YK Chorus`]: https://github.com/SpotlightKid/ykchorus
[`EQ10Q`]: http://eq10q.sourceforge.net/
[`EasySSP`]: https://github.com/automatl/audio-dsp-multi-visualize/
[`LUFS meter`]: https://github.com/klangfreund/LUFSMeter
[`Luftikus`]: https://github.com/lkjbdsp/lkjb-plugins/tree/master/Luftikus
[`lkjb plugins`]: https://github.com/lkjbdsp/lkjb-plugins
[`The Audio Programmer Discord Server`]: https://discord.com/channels/382895736356077570/490473503422808064
[`pluginval`]: https://github.com/Tracktion/pluginval
[`Tracktion Engine`]: https://github.com/Tracktion/tracktion_engine/
[`Dplug`]: https://github.com/AuburnSounds/Dplug
[`iPlug2`]: https://github.com/iPlug2/iPlug2
[`iced_baseview`]: https://github.com/BillyDM/iced_baseview
[`iced`]: https://github.com/hecrj/iced
[`baseview`]: https://github.com/RustAudio/baseview
[`iced_audio`]: https://github.com/BillyDM/iced_audio
[`iced-baseplug-examples`]: https://github.com/BillyDM/iced-baseplug-examples
[`goldenrod`]: https://github.com/BillyDM/goldenrod
[`QMidiArp`]: https://github.com/emuse/qmidiarp
[`Rust Community Discord Server`]: https://discord.com/channels/273534239310479360/273534239310479360
[`Virtual Riot`]: https://www.youtube.com/c/OfficialVirtualRiot/featured
[`Zircon`]: https://www.youtube.com/playlist?list=PLD8FC11AD5EB41006
[`Mr. Bill`]: https://www.youtube.com/playlist?list=PLDxTQYPyq4JTRvdmYDiykyOdoEjjyuQgI
[`Nigel Good`]: https://www.youtube.com/channel/UCnqL5z-OAN-QHT4aRFtpvWA
[`Frequent`]: https://www.youtube.com/channel/UCVMbWJCB-79KbDZ51eakZgQ
[`Crow`]: https://www.youtube.com/c/CrowOfficial/videos
[`Nosia`]: https://www.youtube.com/watch?v=PzM37xuFFxY
[`Symbolab`]: https://www.symbolab.com/
[`Octave`]: https://octave-online.net/
[`Airwindows Plugins`]: https://github.com/airwindows/airwindows/tree/master/plugins
[`Geonkick`]: https://github.com/iurie-sw/geonkick
[`Real-time audio programming 101`]: http://www.rossbencina.com/code/real-time-audio-programming-101-time-waits-for-nothing
[`The Art of VA Filter Design`]: https://www.native-instruments.com/fileadmin/ni_media/downloads/pdf/VAFilterDesign_2.1.0.pdf
[`Khan Academy`]: https://www.khanacademy.org/math
[`Paul's Online Math Notes`]: https://tutorial.math.lamar.edu/
[`Paul's Cheat Sheets`]: https://tutorial.math.lamar.edu/Extras/CheatSheets_Tables.aspx
[`katjaas`]: http://www.katjaas.nl/home/home.html
[`dsp-learning`]: https://github.com/crsaracco/dsp-learning
[`Awesome Rust Audio`]: https://github.com/kfrncs/awesome-rust-audio
[`Useful Links for DSP and Audio Programming`]: https://rust.audio/articles/useful-resources/
[`x42-plugins`]: https://github.com/x42/x42-plugins
[`Jatin Chowdhury`]: https://jatinchowdhury18.medium.com/
[`The Rust Performance Book`]: https://nnethercote.github.io/perf-book/title-page.html
[`Helio Workstation`]: https://github.com/helio-fm/helio-workstation
[`sjaehn`]: https://github.com/sjaehn?tab=repositories
[`density`]: https://github.com/airwindows/airwindows/tree/master/plugins/LinuxVST/src/Density
[`pressure4`]: https://github.com/airwindows/airwindows/tree/master/plugins/LinuxVST/src/Pressure4
[`totape5`]: https://github.com/airwindows/airwindows/tree/master/plugins/LinuxVST/src/ToTape5
[`ironoxide`]: https://github.com/airwindows/airwindows/tree/master/plugins/LinuxVST/src/IronOxide5
[`Mixing Secrets for the Small Studio`]: https://www.amazon.com/Mixing-Secrets-Small-Studio-Presents/dp/0240815807
[`The Design of the Roland Juno oscillators`]: https://blog.thea.codes/the-design-of-the-juno-dco/
[`Fast-DSP-Approximations`]: https://github.com/BillyDM/Fast-DSP-Approximations
[`LSP Plugins`]: https://github.com/sadko4u/lsp-plugins
[`How to Hear Compression`]: https://youtu.be/K0XGXz6SHco
[`Digital Signal Processing: Concepts and Applications`]: https://www.amazon.com/Digital-Signal-Processing-Concepts-Applications-ebook/dp/B015OLJ5JG/
