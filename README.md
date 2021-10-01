# Awesome Audio DSP
My curated list of audio DSP (digital signal processing) and plugin development resources. New resources may be added in the future. Feel free to open a PR if you wish!

## Free Online Textbooks
- [`The Scientist and Engineer's Guide to Digital Signal Processing`] by Steven W. Smith, Ph.D.
  - A common recommendation from many folks.
  - Focuses on DSP in general, not just audio DSP.

- [`Julius Orion Smith III Collection`]
  - A great collection of books and resources by Julius Orion Smith III.
  - Very comprehensive, and covers many topics on the mathematics and applications of audio DSP. Good for getting a solid foundation.
  - Contains code examples in C and MatLab (although [`GNU Octave`] can be used as well).
  - Relatively heavy on mathematics.

- [`The Art of VA Filter Design`] by Vadim Zavalishin
  - Teaches good techniques for adapting analogue designs into the digital realm.
  - Relatively heavy on mathematics.

- [`The Theory and Technique of Electronic Music`] by Miller Puckette
  - Focuses more on musical DSP.
  - Teaches core concepts of many common audio effects and synthesizers.
  - Relatively heavy on mathematics.

## Paid Textbooks
- [`Designing Software Synthesizer Plug-Ins in C++`] and [`Designing Audio Effect Plugins in C++`] by Will Pirkle
  - One of the most highly recommended resources for entering the world of audio DSP.
  - Great beginner resource that teaches fundamental DSP concepts without going into too much mathematics.
  - The synthesizer one is better than the effect one imo, so go for that if you plan on only buying one.
  - Focuses on teaching concepts, not on writing performant code. His coding sytle is quite ineffecient.
  - There will also be [`newer edition`] in 2021 as well.

- [`A Digital Signal Processing Primer`] by Kenneth Steiglitz
  - Great introduction to the mathematics of DSP.
  - Focuses more on mathematics and does not have many example effects.

- [`DAFX: Digital Audio Effects`] by Udo Zölzer (Editor)
  - Explores good modern advanced effects. It's made by the [`DAFx`] annual scientific research conference.
  - MATLAB is used for its code examples, but [`GNU Octave`] could probably be used as well.

- [`Digital Signal Processing: Concepts and Applications`] by Mulgrew, Grant & Thompson
  - Covers the basic principles of DSP in an easy-to-digest way without going into too much mathematics.
  - Focuses more on general DSP rather than audio DSP.
  - Uses MATLAB for its code examples, but [`GNU Octave`] could probably be used as well.

## DSP Playgrounds
These can be a great start for learning and experimenting with DSP for those with little or no programming experience.

### Codeless
- [`Reaktor 6`] by Native Instruments
  - A popular modular environment for creating DSP without code.
  - Has a sizeable community.
  - Full version is expensive at $200 USD at the time of this writing. Free version is limited in functionality.
  - Mac and Windows only. Although some have had success running it in Linux using Wine.
- [`Alpha Forever`]
  - A Reaktor-like environment for creating DSP without code.
  - Commercial software that is $80 USD at the time of this writing. Although the free demo lets you use all the features, just without the ability to save.
  - Windows only.
- [`The Grid`] by Bitwig Studio
  - A built-in Reaktor-like plugin environment tightly integrated with the highly modular Bitwig Studio DAW.
  - Highly intuitive to use.
  - Requires Bitwig Studio, which is a whopping $400 USD at the time of this writing. However, the demo version lets you use all the features, just without the ability to save.
  - Sound quality is not the greatest.
  - Runs on Linux, Mac, and Windows.
- [`VCV Rack`]
  - A fully modular software environment that simulates the analogue Eurorack environment.
  - Popular with a sizeable community.
  - Arguably more "plugin"-like than actual DSP, but concepts still translate to DSP skills.
  - Free and open source.
  - Runs on Linux, Mac, and Windows.

### Easy Code
- [`CSound`]
  - A custom scripting language that is easy to learn and use.
  - Well-known and long standing in the industry.
  - Free and open-source.
- [`py-modular`]
  - A modular and experimental programming environment with basic DSP routines.
  - Uses the very popular [`Python`] programming language, which is a great those who are learning to code.
  - Relatively new and experimental project.
  - Free and open-source.
- [`FunDSP`]
  - A neat project for learning and prototyping DSP.
  - Uses the [`Rust`] programming language, so it is not for those who are beginners to coding. However, the library itself does not require advance Rust skills.
  - Relatively new and experimental project.
  - Free and open-source.

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
- [`Cytomic Technical Papers`] - Excellent real-world useable filters and explanations by Cytomic. Use these as a better alternative to Biquad filters that behave much better while being modulated.
- [`deip.pdf`] - High quality resampling and oversampling.
- [`Freeverb`] - An open-source reverb algorithm.
- [`DAFx`] - An archive of scientific papers and presentations given during an annual DSP research conference.
- [`katjaas`] - Neat visual explanations of DSP mathematics and techniques.
- [`Jatin Chowdhury`] - An active blog that explores cutting-edge DSP techniques.
- [`The Design of the Roland Juno oscillators`] - A beautiful and simple explanation on the oscillators of this classic synth.
- [`TimeStretch PDF`] - A PDF explaining the DSP of [`TimeStretch`], a refinement of the famous [`PaulStretch`] time stretching effect.

## Machine Learning
Machine learning has been gaining traction in the audio industry lately. I don't know much about the topic myself, but I'll link some potentially useful resources here if you're interested.
- [`3Blue1Brown - Neural Networks`] - An excellent short series of YouTube videos explaining the basics of how machine learning actually works.
- [`SmartCore`] - An advanced and comprehensive machine learning library written in the [`Rust`] programming language.

## Open Source Plugins & Software
Reading the source code of real-world projects can give valueable insight into different techniques and solutions people have come up with over the years.
### Collections
- [`Airwindows Plugins`] - Many, many good quality effects and experiments developed over many years.
  There are a *ton* of plugins here, so here is a list of community favorites:
  - [`density`]
  - [`pressure4`]
  - [`totape5`]
  - [`ironoxide`]
- [`zam-plugins`] - A suite of high quality mixing/mastering plugins. The limiter, tube amp, and multiband compressor are particularly excellent.
- [`LSP Plugins`] - Another collection of high quality mixing/mastering effects.
- [`sjaehn`] - Several cool MIDI based slicing/glitching effects and synthesizers.
- [`x42-plugins`] - A collection of high quality effects and visualizers. Some plugins are also sold as a commercial product. The compressor is particularly excellent.
- [`EQ10Q`] - A suite of plugins containing a 10-band parametric equalizer, gate, compressor, bass enhancer, and mid-side encoders.
- [`Shiru Plugins`] - A suite of old video-game sound chips synths and effects.
- [`DISTRHO Plugin Framework`] - A bunch more open-source plugins are listed here.
- [`lkjb plugins`] - Additional plugins made by the creator of [`Luftikus`].
### Synths
- [`Vital`] - An incredibly powerful and high quality modern synthesizer. Rivals that of Xfer Serum and NI Massive.
- [`Helm`] - High-quality modern monophonic synthesizer. The older sibling to Vital. The oscillators are not stereo though.
- [`Surge`] - Feature-rich hybrid synthesizer that was once sold as a commercial product.
- [`Dexed`] - Synthesizer closely modelled after the Yamaha DX7.
- [`ZynAddSubFX`] - Feature-rich additive synthesizer with a great clean sound. Also sold as a commercial product.
- [`Odin 2`] - Modern analogue-modeled hybrid synthesizer.
- [`Geonkick`] - Advanced drum synthesizer.
- [`ADLplug`] - Emulation of FM-synthesizers found in some classic game consoles.
- [`Ninjas 2`] - Sample slicer and player.
- [`Mika Micro`] - A nice and simple synthesizer with a clean design.
- [`Synth2`] - A recreation of the classic Synth1 virtual synth. (Still a work in progress).
- [`Sfizz`] - A sampler that plays [`SFZ`] files. (SFZ is like SoundFonts but with more features).
- [`Bespoke Synth`] - A very modular synthesizer with support for complex routing, modulation, and sequencing. It can even host VST plugins, blurring the lines between synth and DAW.
### Audio FX
- [`Wolf Shaper`] - Good quality waveshaper with support for unlimited nodes.
- [`Mverb`] - Nice-sounding plate reverb.
- [`Dragonfly Reverb`] - Algorithmic reverb based on [`Freeverb`].
- [`CloudReverb`] - Beautiful shimmering reverb based on the `CloudSeed` plugin by Valdemar Erlingsson. I choose this over the original as that uses a Windows-only C# platform for its GUI.
- [`Luftikus`] - Good quality analogue modeled equalizer.
- [`Fogpad`] - Reverb plugin where reflections can be frozen, filtered, pitch-shifted, and mangled.
- [`Misstortion`] - Good quality hard/soft clipper.
- [`Cocoa Delay`] - A nice delay plugin with ducking, saturation, filtering, and pitching features.
- [`Flutterbird`] - Simple multi-lfo than modulates pitch and volume, creating a "fluttering" effect.
- [`DelayArchitect`] - A feature-rich delay designer plugin.
- [`TimeStretch`] - A refinement of the famous [`PaulStretch`] time stretching effect. Includes a PDF explaining the DSP.
### MIDI FX
- [`Helio Workstation`] - A very modern and feature-rich sequencer.
- [`QMidiArp`] - Advanced arpeggiator, sequencer, and MIDI LFO.
- [`Stochas`] - An advanced probabilistic polyrythmic sequencer. Made by the same team behind the [`Surge`] synthesizer.
### Meters & Visualizers
- [`Spectacle`] - Modern real-time spectrum analyzer plugin.
- [`Wolf Spectrum`] - Real-time heat-map spectrum analyzer plugin.
- [`EasySSP`] - Real-time spectrum analyzer and stereo analyzer plugin.
- [`LUFS Meter`] - Real-time loudness meter with support for several international loudness standards.
### DAWs & Hosts
- [`Meadowlark`] - Definitely biased here since this is my main project that I work on full-time. It's still in its very early stages, but check it out if you're interested in contributing! :)
- [`Ardour`] - Feature-rich DAW. Focuses more on recorded music production over electronic music production.
- [`LMMS`] - Feature-rich DAW focused on electronic music production. Contains many built-in synths and effects.
- [`Audacity`] - Popular multi-track audio editor. There is also a fully-libre open source fork called [`Tenacity`].
- [`Carla`] - Cross platform plugin host with support for many plugin formats.
- [`Bespoke Synth`] - A very modular synthesizer with support for complex routing, modulation, and sequencing. It can even host VST plugins, blurring the lines between synth and DAW.
- [`termdaw`] - A neat little DAW experiment that uses a terminal as its interface instead of a GUI.
### Musical Notation
- [`MuseScore`] - A popular and mature open-source sheet music editor.
- [`composing.studio`] - An experimental open-source web app that allows you to collaborate on editing sheet music.

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
- [`Compiler Explorer`] - Very useful tool that lets you analyze the assembly output of many different languages including Rust, C, and C++.
- [`Software Optimization Resources`] - A popular resource on optimizing for x86 based architectures.
- [`Agner Fog's Instruction Tables`] - A useful table that lists the latency and throughput performance of various x86 instructions.
- [`Real-time audio programming 101`] - Tips on writing real-time code.
- [`The Rust Performance Book`] - Tips on optimizing code in Rust.
- Follow these rules:
  ![DSP Rules](fast_dsp.png?raw=true)

## Math Tools
- [`Desmos`] - Free online graphing calculator.
- [`Wolfram Alpha`] - A helpful math partner.
- [`Symbolab`] - Another helpful math partner.
- [`GNU Octave`] - An open-source alternative to MATLAB. There is also an [`online version of GNU Octave`] available.
  - [`Signal package`] - Signal processing tools for [`GNU Octave`], including filtering, windowing and display functions.
- [`Curcuit JS`] - A cool little circuit simulation tool.
- [`Russell`] - A collection of tools that assist in the development of scientific computations (and by extension audio DSP). It includes numerical methods and solvers for differential equations, tools for statistical analysis, and other linear algebra tools. It is written in the [`Rust`] programming lanugage. 

## System Tools
- [`MrsWatson`] - Command-line audio plugin host with support for printing to the terminal from your DSP code.
- [`Carla`] - System-wide virtual audio and MIDI patching software, using [`Jack`] as the backend. Available as a standalone application or a VST/LV2 plugin.
- [`Jack`] - Cross-platform audio driver with support for system-wide patching.
- [`Cadence`] - A suite of tools for configuring, monitoring, and controlling system-wide audio in Linux (includes [`Carla`]).
- [`Ardour`] - Open-source DAW with useful plugin analysis tools.
- [`Bertom EQ Curve Analyzer`] - Analyze the frequency and phase response of any plugin.
- [`pluginval`] - Cross-platform open-source plugin validation tool made by the company Tracktion.

## Plugin APIs
There are quite a few audio plugin API standards which allow your plugin be compatible with certain DAWs and hosts. I'll list the most relevant ones today and their advantages/disadvantages.
### VST2 (aka VST, version 2)
  - Why?: It is the most well-known and mature format, supported by almost every DAW.
  - Why Not?: Unless you already have a signed license agreement from Steinberg, you're not even allowed to distribute your VST2 plugins or create a host for VST2 plugins (yeah it stinks).
  - License: Proprietary
  - Platforms: Linux, Mac, Windows
  - Support: Supported by pretty much every commercial DAW (with notable exception of Apple's DAW Logic) and by most open source DAWs.
  - Distribution: Must have a signed license agreement to distribute any VST2 plugin. If you don't already have a VST2 license, you're out of luck since Steinberg doesn't support it anymore (yeah it stinks).
  - SDK source: (Not available anymore).
### Vestige (Reversed engineered VST2)
  - Why?: If you still *really* want to distribute or host VST2 plugins without a signed license agreement, this is another option.
  - Why Not?: Gray legal area.
  - License: *Technically* [`GPLv2`]/[`GPLv3`], but again this is a gray legal area. It is technically legal since the author claims it to be cleanly and legally reverse engineered without reference to the official VST2 SDK. However, I don't believe this has been tested in court, so I wouldn't rely on it.
  - Platforms: Same as VST2 above.
  - Support: Same as VST2 above.
  - Distribution: You can only distribute your plugins or host as open source under either the [`GPLv2`] or [`GPLv3`] license. Though again, this is a gray legal area so I would be weary.
  - SDK source: [`Vestige Header File`]
### VST3 (aka VST version 3)
  - Why?: This plugin standard is widely used and has excellent support in most modern commercial DAWs.
  - Why Not?: Requires a signed license agreement with Steinberg in order to distribute commercial (closed source) VST3 plugins (or to host VST3 plugins in a closed source host). Also, Steinberg makes it hard to bind this C++ library to use with other languages (like [`Rust`]).
  - License: Proprietary / [`GPLv3`]
  - Platforms: Linux, Mac, Windows
  - Support: Supported by most modern commercial DAWs (with notable exception of Apple's DAW Logic) and a few open source DAWs.
  - Distribution - If you are distributing your plugin with the [`GPLv3`] open source license (or host VST3 plugins with your own [`GPLv3`] host), then you do not need to have a signed license agreement with Steinberg. However, if you want to distribute your plugin closed source (for commercial purposes) or create a closed-source host, then you need to get a signed [`VST3 License Agreement`].
    - Also note that Steinberg has a history of changing their license agreements for however they see fit (like they did when they stopped giving out VST2 licenses). If you want to ever distribute plugins commerically, I would advise to get a license agreement as soon as possible before Steinberg changes their mind.
  - Special note - Steinberg is making it difficult to legally create bindings to the VST3 SDK so it can be used with other programming languages (the SDK is in C++). As a Rust developer myself, this has been a big pain in the backside. There have been proposed lawsuits that aim to prevent companies from doing this, but who knows what the future will hold? (By now you can probably see why a lot of the audio industry does not like Steinberg).
  - SDK download: [`VST3 SDK`]
### AUv2/AUv3 (aka AU or Audio Units, version 2 and 3)
  - License: [`Apache 2.0`]
  - Platforms: Mac, iOS
  - Support: Main support is for Apple's own DAW Logic, but a few other DAWs that run on Mac support it as well. AU is the only plugin standard supported by Logic.
  - Distribution - You can distribute open source and close sourced versions of your plugins (and host AU plugins) freely without restriction.
  - SDK source: [`AU SDK`]
### AAX
This is a proprietary plugin standard for use exclusively with Avid's DAW Pro Tools.
  - Why?: Pro Tools is pretty standard in the professional/corporate recording/mixing/mastering industry. Pro Tools only supports AAX plugins.
  - Why Not?: No other DAW supports it. Also, it requires a signed license agreement with Avid, and also requires joining Avid's developer program.
  - License: Proprietary
  - Platforms: Mac, Windows
  - Support: Only Pro Tools
  - Distribution: Requires a signed license agreement with Avid, and also requires joining Avid's developer program.
  - SDK source: (must register to download)
 ### LV2
 LV2 is a libre open source plugin standard created for use within the Linux ecosystem.
  - Why?: Even though support on Mac and Windows is rare, Linux has by far the best development ecosystem in my opinion. There is also a growing community of music producers using Linux.
  - Why Not?: Lack of support in most major commercial DAWs.
  - License: [`MIT`]
  - Platforms: Linux, Mac, Windows (Although support for Mac and Windows is rare.)
  - Support: Supported by most open-source DAWs, but hardly any commercial DAWs support it (maybe even none of them do).
  - Distribution -  You can distribute open source and close sourced versions of your plugins (and host LV2 plugins) freely without restriction.
  - SDK source: [`LV2 SDK`]
### LADSPA
LADSPA is the precursor to LV2.
  - Why?: It is dead simple to work with.
  - Why Not?: Lack of support in most major commercial DAWs. Also, LADSPA only supports GUI-less plugins.
  - License: [`LGPLv2.1`]/[`LGPLv3`]
  - Platforms: Same as LV2 above
  - Support: Same as LV2 above
  - Distribution: Same as LV2 above
  - SDK source: [`LADSPA Header File`]
### WAP (Web Audio Plugins)
An open source audio plugin standard for use with web browsers using WebAudio.
  - Why?: If you want create plugins using web technologies if that is something you are already familiar with.
  - Why Not?: Only works in a web browser, so all native DAWs don't support it.
  - License: [`MIT`]
  - Platforms: Web
  - Support: Only web-browser based DAWs
  - Distribution: You can distribute open source and close sourced versions of your plugins (and host WAP plugins) freely without restriction.
  - SDK source: [`WAP SDK`]
### VCV Rack Plugin
The audio plugin standard for use with the open source [`VCV Rack`] virtual synthesizer.
  - Why?: If you want to create plugins for [`VCV Rack`].
  - License: [`GPLv3`]
  - Distribution: You can distribute freely if your plugin is [`GPLv3`] or a multitude of other accepted open source licenses. You are allowed to sell closed-source versions if you get special permission from the author via email. See [`VCV Rack Licensing`] for more details.
  - SDK source: [`VCV Rack Plugin SDK`]

## Plugin Development Frameworks
- Please note that you must have a licensing agreement with Steinberg to *distribute* any VST2 and any non-GPLv3 VST3 plugins as per [`Steinberg's VST3 License`]. If you don't already have a VST2 license, you're out of luck since Steinberg doesn't support it anymore (yeah it stinks). Target VST3 instead in that case.
### RustAudio Framework
  - Full-stack and modular framework in Rust (currently a WIP and not fully-production ready yet for anything but VST2 plugins). I'm personally biased towards this as one of its creators.
  - Fully open-source under the permissive MIT or Apache2 license.
  - Plugin FFI bindings
    - [`vst-rs`] - Provides nice bindings to the VST2 api.
      - Does not contain a GUI framework, but other frameworks can be attached to provide the GUI.
      - Targets Mac, Windows, and Linux platforms.
    - [`baseplug`] - Provides an abstraction-layer over several different plugin formats, and simplifies parameter management.
      - Does not contain a GUI framework, but other frameworks can be attached to provide the GUI.
      - Currently only targets the VST2 plugin format. VST3, AU, LV2, and JACK targets are currently planned.
      - Targets Mac, Windows, and Linux platforms.
  - [`baseview`] - Provides windowing and input events for plugins / standalone applications.
    - Targets Mac, Windows, and Linux.
  - GUI frameworks
    - Iced
      - [`iced_baseview`] - Provides the [`iced`] GUI framework on top of [`baseview`].
        - Targets Mac, Windows, and Linux.
      - [`iced_audio`] - An extension to the [`iced`] GUI framework that provides audio-specific widgets like knobs and sliders.
      - [`iced-baseplug-examples`] - Example of full-stack plugins built using the [`baseplug`], [`iced_baseview`], and [`iced_audio`] modules.
    - Tuix
      - [`tuix`] - Experimental/WIP GUI library with an official [`baseview`] backend.
      - [`tuix_audio_synth`] - Example of how to build audio widgets using [`tuix`].
      - [`tuix_baseview_test_vst2`] - Example of a full-stack plugin built using the [`vst-rs`] and [`tuix`] modules.
    - Egui
      - [`egui-baseview`] - Provides the [`egui`] GUI framework on top of [`baseview`].
      - [`egui_baseview_test_vst2`] - Example of a full-stack plugin built using the [`vst-rs`] and [`egui-baseview`] modules.
    - Imgui
      - [`imgui-rs`] - Rust bindings to the popular [`Dear ImGui`] C framework.
      - [`imgui-baseview`] - Provides the [`imgui-rs`] GUI framework on top of [`baseview`].
      - [`imgui_baseview_test_vst2`] - Example of a full-stack plugin built using the [`vst-rs`] and [`imgui-baseview`] modules.
      - [`imgui-compressor`] - An experimental/WIP compressor plugin built using the [`vst-rs`] and [`imgui-baseview`] modules.
### [`DISTRHO Plugin Framework`]
  - Full-stack framework with GUI in C++.
  - Fully open-source using a permissive license.
  - Targets LADSPA, DSSI, LV2, VST2, and Jack plugin formats.
  - Targets Mac, Windows, and Linux platforms.
### [`Dplug`]
  - Full-stack framework with GUI in te D programming language.
  - Fully open-source using a permissive license.
  - The GUI framework has fancy physically-modeled rendering inspired by game engines.
  - Targets VST2, VST3, AUv2, AAX, and LV2 plugin formats.
  - Targets Mac, Windows, Linux, and Raspberry Pi platforms.
  - Used by several commercial plugins.
### [`JUCE`]
  - Full-stack framework with GUI in C++.
  - Open source, but some of its modules require a hefty commercial license to distribute any non-GPLv3 plugins.
  - Targets VST2, VST3, AUv2, AUv3, RTAS, and AAX plugin formats.
  - Targets Mac, Windows, Linux, iOS, Android, and Raspberry Pi platforms.
  - Well known in the industry, and many commercial plugins are built with it.
### [`Tracktion Engine`]
  - Full-stack framework in C++ with GUI. It is built on top of [`JUCE`].
  - Same licensing as [`JUCE`] since it's built on top of it.
  - Targeted formats and platforms are the same as [`JUCE`].
  - Made and used by the commercial company Tracktion.
### [`iPlug2`]
  - Full-stack framework in C++ with GUI.
  - Fully open-source using a permissive license.
  - Targets VST2, VST3, AUv2, AUv3, AAX and the Web Audio Module (WAM) plugin formats.
  - Targets Mac, Windows, iOS, and Web. It does not target Linux, so I'm personally not a fan of this one.

## Rust Crates
- [`baseplug`] - Create VST plugins in Rust. (GUI and other plugin formats are still a work in progress.)
- [`basedrop`] - Memory management tools for interfacing with realtime threads.
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

## More Lists
Here I'll link curated lists that others have made.
- [`dsp-learning`] by crsaracco
- [`Awesome Rust Audio`] by kfrncs
- [`Useful Links for DSP and Audio Programming`] from rust.audio

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
[`iced_audio`]: https://github.com/iced-rs/iced_audio
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
[`GNU Octave`]: https://www.gnu.org/software/octave/index
[`online version of GNU Octave`]: https://octave-online.net/
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
[`Vital`]: https://github.com/mtytel/vital
[`Shiru Plugins`]: https://github.com/linuxmao-org/shiru-plugins
[`vst-rs`]: https://github.com/RustAudio/vst-rs
[`tuix`]: https://github.com/geom3trik/tuix
[`tuix_audio_synth`]: https://github.com/geom3trik/tuix_audio_synth
[`tuix_baseview_test_vst2`]: https://github.com/geom3trik/tuix_baseview_test_vst2
[`egui`]: https://github.com/emilk/egui
[`egui-baseview`]: https://github.com/BillyDM/egui-baseview
[`egui_baseview_test_vst2`]: https://github.com/DGriffin91/egui_baseview_test_vst2
[`Dear ImGui`]: https://github.com/ocornut/imgui
[`imgui-rs`]: https://github.com/imgui-rs/imgui-rs
[`imgui-baseview`]: https://github.com/BillyDM/imgui-baseview
[`imgui_baseview_test_vst2`]: https://github.com/DGriffin91/imgui_baseview_test_vst2
[`imgui-compressor`]: https://github.com/DGriffin91/compressor-plugin
[`Steinberg's VST3 License`]: https://developer.steinberg.help/display/VST/VST+3+Licensing
[`Mika Micro`]: https://github.com/tesselode/mika-micro
[`Cocoa Delay`]: https://github.com/tesselode/cocoa-delay
[`Flutterbird`]: https://github.com/tesselode/flutterbird
[`Agner Fog's Instruction Tables`]: https://www.agner.org/optimize/instruction_tables.pdf
[`Software Optimization Resources`]: https://www.agner.org/optimize/
[`Synth2`]: https://github.com/klknn/synth2
[`Stochas`]: https://github.com/surge-synthesizer/stochas
[`Signal package`]: https://octave.sourceforge.io/signal/index.html
[`Rust`]: https://www.rust-lang.org/
[`Reaktor 6`]: https://www.native-instruments.com/en/products/komplete/synths/reaktor-6/
[`Alpha Forever`]: https://www.afmodular.com/
[`CSound`]: https://csound.com/
[`py-modular`]: http://py-modular.readthedocs.io/
[`Python`]: https://www.python.org/
[`VCV Rack`]: https://vcvrack.com/
[`The Grid`]: https://www.bitwig.com/the-grid/
[`zam-plugins`]: https://github.com/zamaudio/zam-plugins
[`TimeStretch`]: https://github.com/spluta/TimeStretch
[`TimeStretch PDF`]: https://github.com/spluta/TimeStretch/blob/main/NessStretchICMC_Final.pdf
[`PaulStretch`]: http://hypermammut.sourceforge.net/paulstretch/
[`termdaw`]: https://github.com/ocdy1001/termdaw
[`Sfizz`]: https://github.com/sfztools/sfizz
[`SFZ`]: https://sfzformat.com/
[`DelayArchitect`]: https://github.com/jpcima/DelayArchitect
[`Tenacity`]: https://github.com/tenacityteam/tenacity
[`Meadowlark`]: https://github.com/MeadowlarkDAW/Meadowlark
[`Compiler Explorer`]: https://rust.godbolt.org/
[`basedrop`]: https://github.com/glowcoil/basedrop
[`Bespoke Synth`]: https://github.com/BespokeSynth/BespokeSynth
[`Russell`]: https://github.com/cpmech/russell
[`SmartCore`]: https://smartcorelib.org/
[`3Blue1Brown - Neural Networks`]: https://youtube.com/playlist?list=PLZHQObOWTQDNU6R1_67000Dx_ZCJB-3pi
[`MuseScore`]: https://musescore.org
[`composing.studio`]: https://github.com/ekzhang/composing.studio
[`GPLv2`]: https://opensource.org/licenses/gpl-2.0.php
[`GPLv3`]: https://choosealicense.com/licenses/gpl-3.0/
[`MIT`]: https://choosealicense.com/licenses/mit/
[`Apache 2.0`]: https://choosealicense.com/licenses/apache-2.0/
[`Vestige Header File`]: https://github.com/x42/lv2vst/blob/master/include/vestige.h
[`VST3 SDK`]: https://github.com/steinbergmedia/vst3sdk
[`AU SDK`]: https://github.com/apple/AudioUnitSDK
[`LV2 SDK`]: https://gitlab.com/lv2/lv2
[`LADSPA Header File`]: https://www.ladspa.org/ladspa_sdk/ladspa.h.txt
[`LGPLv2.1`]: https://opensource.org/licenses/lgpl-2.1.php
[`LGPLv3`]: https://choosealicense.com/licenses/lgpl-3.0/
[`WAP SDK`]: https://github.com/micbuffa/WebAudioPlugins
[`VCV Rack Plugin SDK`]: https://vcvrack.com/downloads/
[`VCV Rack Licensing`]: https://vcvrack.com/manual/PluginLicensing
[`VCV Rack Plugin Tutorial`]: https://vcvrack.com/manual/PluginDevelopmentTutorial
[`sjaehn's LV2 Tutorial`]: https://github.com/sjaehn/lv2tutorial
[`VST3 License Agreement`]: https://developer.steinberg.help/pages/viewpage.action?pageId=9797944
