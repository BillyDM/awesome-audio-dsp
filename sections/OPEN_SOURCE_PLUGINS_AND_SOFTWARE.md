# Open Source Plugins & Software

A list of open source audio software that you can inspect and learn from, along with the language and framework used to make them.

# Open Source Plugins

## Collections

(Note, I'm avoiding listing individual plugins in the `Synths`/`Audio FX`/`MIDI FX`/`Meters & Visualizers` sections if they appear in one of these collections. A few exceptions are made for plugins that are particuarly notable.)

- [AnClark's Plugin Ports](https://github.com/AnClark) | (C++, [DPF]) | - A collection of various synths and plugins ported to [DPF].
- [Airwindows Plugins](https://github.com/airwindows/airwindows/tree/master/plugins) | (C++, gui-less, raw plugin APIs) | - Lots of good quality effects and experiments developed over many years.
  - There are a *ton* of plugins here, so here is a list of some community favorites:
    - [density](https://github.com/airwindows/airwindows/tree/master/plugins/LinuxVST/src/Density)
    - [ironoxide](https://github.com/airwindows/airwindows/tree/master/plugins/LinuxVST/src/IronOxide5)
    - [pressure4](https://github.com/airwindows/airwindows/tree/master/plugins/LinuxVST/src/Pressure4)
    - [totape5](https://github.com/airwindows/airwindows/tree/master/plugins/LinuxVST/src/ToTape5)
  - [airwin2rack](https://github.com/baconpaul/airwin2rack) | (C++, [JUCE], [VCV Rack]) | - All of the Airwindows plugins consolidated into a single plugin with GUI. Can also be used as a static libray for inclusion into other projects.
- [ardura's plugins](https://github.com/ardura) | ([Rust], [nih-plug], [egui]) | - A collection of neat synths and effects with nice-looking GUIs. Written in Rust, nih-plug, and egui.
- [Black Box Audio plugins](https://github.com/blackboxaudio) | (C++, [Rust], [JUCE]) | - Contains some neat plugins from this new audio company including a phase distortion synthesizer and a fancy ring modulation effect.
- [brummer10's plugins](https://github.com/brummer10?tab=repositories) | (C++, [libxputty], raw plugin APIs, [JUCE]) | - A large collection of mostly guitar-focused effects. [guitarix](https://github.com/brummer10/guitarix) is one of the more popular ones.
- [Calf Studio gear](https://github.com/calf-studio-gear/calf) | (C++, custom [GTK] framework) | - A large collection of plugins aimed at a professional audience.
- [Chowdhury DSP](https://github.com/Chowdhury-DSP) | (C++, [JUCE]) | - A collection of high quality effect plugins (as well as a kick drum synthesizer). A lot of these plugins make use of use of cutting-edge neural network inferencing.
- [Cool Panda Plugins](https://www.coolxpandaxplugins.com/) | (C++, [JUCE]) | - A collection of creative effects.
- [Destroy FX](https://github.com/sophiapoirier/destroyfx) | (C++, custom GUI framework based on [VSTGUI], raw plugin APIs) | - A collection of effects that "destroy your sound".
- [DISTRHO Dear Plugins](https://github.com/DISTRHO/dear-plugins) | (C++, [DPF], [Dear ImGui]) | - A collection of plugins demonstrating how to use the Dear ImGui library with the DPF framework. Still a work in progress.
- [DISTRHO Plugin Framework](https://github.com/DISTRHO/DPF) | (C++, [DPF]) | - Has a list of plugins that were made using this framework.
- [DISTRHO-Ports](https://github.com/DISTRHO/DISTRHO-Ports) | (C++, [JUCE]) | - A whole bunch of plugins ported to work on Linux/LV2.
- [Dplug] | (D, [Dplug]) | - Contains some example plugins using the framework.
- [EQ10Q](http://eq10q.sourceforge.net/) | (C++, custom [GTK] framework) | - A suite of plugins containing a 10-band parametric equalizer, gate, compressor, bass enhancer, and mid-side encoders.
- [FX-Mechanics Plugins](https://github.com/odoare?tab=repositories) | (C, C++, [JUCE]) | - A neat collection of plugins including a waveguide synthesizer and a binaural convolutional reverb.
- [Glafo's plugins](https://github.com/glafiro) | (C++, [JUCE]) | - A collection of good quality plugins with fancy UIs.
- [GuitarML](https://github.com/GuitarML) | (C++, [JUCE]) | - A collection of electric guitar effects that use neural network models to emulate real-world hardware.
- [Igorski's Plugins](https://github.com/igorski?tab=repositories) | (C++, [JUCE]) | - Contains some neat synths and effects.
- [JoepVanlier's JSFX plugins](https://github.com/JoepVanlier/JSFX) | ([JSFX], [Lua]) | - A collection of cool plugins and scripts for Reaper. Some of the GUIs are really stunning.
- [lkjb plugins](https://github.com/lkjbdsp/lkjb-plugins) | (C++, [JUCE]) | - Additional plugins made by the creator of [Luftikus].
- [LSP Plugins](https://github.com/lsp-plugins) | (C++, custom GUI framework) | - A collection of good quality mixing/mastering effects for Linux.
- [Madadog's plugins](https://github.com/Madadog) | ([Rust], [nih-plug], [Iced]) | - Contains some synthesizer plugins written in [Rust].
- [Maeror's VST3 plugins](https://github.com/Maerorr/maerors-vst3-plugins) | ([Rust], [nih-plug], [Vizia]) | - A collection of simple effects written in Rust, nih-plug, and Vizia.
- [Mrugalla Plugins](https://github.com/Mrugalla) | (C++, [JUCE]) | - A collection of modern and unique plugins by Florian Mrugalla.
- [Mutable Instruments' Eurorack Modules](https://github.com/pichenettes/eurorack/tree/master) | (C++, custom embedded framework) | - The source code for a large collection of popular, high quality [Eurorack] modules.
- [nih-plug](https://github.com/robbert-vdh/nih-plug) | ([Rust], [nih-plug], [egui], [Iced], [Vizia]) | - Contains a collection of plugins written in Rust, including the amazing [Spectral Compressor](https://github.com/robbert-vdh/nih-plug/tree/master/plugins/spectral_compressor) plugin.
- [PodcastPlugins](https://github.com/trummerschlunk/PodcastPlugins) | (C++, [DPF]) | - A collection of easy-to-use plugins for speach enhancement. Currently under development at the time of this writing.
- [Shiru Plugins](https://github.com/linuxmao-org/shiru-plugins) | (C++, [DPF]) | - A suite of old video-game sound chips synths and effects.
- [sjaehn](https://github.com/sjaehn?tab=repositories) | (C++, [Pugl]) | - Several cool MIDI based slicing/glitching effects and synthesizers.
- [SocaLabs Plugins](https://github.com/FigBug/SocaLabs) | (C++, [JUCE]) | - A collection of plugins made by SocaLabs.
- [SOUL-VA](https://github.com/thezhe/SOUL-VA) | ([SOUL]) | - A non-trivial virtual analog filter library written in [SOUL](https://github.com/soul-lang/SOUL). Plugin versions are also sold as commercial products.
- [SpotlightKid's plugins](https://github.com/SpotlightKid) | (C++, [Faust], [DPF]) | - Contains some great plugins like reverbs and a high quality chorus effect.
- [TiagoLr's plugins](https://github.com/tiagolr?tab=repositories) | (C++, [JUCE]) | - Contains some nice plugins including a physically modeled synth, a fancy delay modulator, and a fancy gate plugin.
- [VCV Library database](https://github.com/VCVRack/library) - An official database of [VCV Rack] plugins, containing both commercial and open source plugins.
- [x42-plugins](https://github.com/x42/x42-plugins) | (C, [robtk], [Pugl]) | - A collection of good quality effects and visualizers. Some plugins are also sold as a commercial product.
- [zam-plugins](https://github.com/zamaudio/zam-plugins) | (C++, [DPF]) | - A suite of good quality mixing/mastering plugins.
- [ZL-Audio Plugins](https://github.com/ZL-Audio) | (C++, [JUCE]) | - A collection of good quality plugins including a fancy parametric equalizer, saturator, and compressor.

## Synths

- [ADLplug](https://github.com/jpcima/ADLplug) | (C++, [JUCE]) | - Emulation of FM-synthesizers found in some classic game consoles.
- [Audible Planets](https://github.com/gregrecco67/AudiblePlanets) - | (C++, [JUCE]) | - An expressive, quasi-Ptolemaic semi-modular synthesizer.
- [Bespoke Synth] | (C++, [JUCE]) | - A very modular synthesizer with support for complex routing, modulation, and sequencing. It can even host VST plugins, blurring the lines between synth and DAW.
- [Cardinal] | (C++, [DPF]) | - An open source modular synthesizer plugin that can host [VCV Rack] plugins.
- [Dexed](https://github.com/asb2m10/dexed) | (C++, [JUCE]) | - Synthesizer closely modelled after the Yamaha DX7.
- [DigiDrie](https://github.com/magnetophon/DigiDrie) | ([Faust], C++, [DPF]) | - A "monster" monophonic synth.
- [Fabla 2](https://github.com/openAVproductions/openAV-Fabla2) | (C++, custom GUI framework) | - A multi-sampler plugin with a drum pad layout.
- [Firefly Synth](https://github.com/sjoerdvankreel/firefly-synth) | (C++, [JUCE]) | - A feature-rich semi-modular software synthesizer and fx plugin.
  - It is the bigger brother to the discontinued [InfernalSynth](https://github.com/sjoerdvankreel/infernal-synth) plugin.
- [Geonkick](https://github.com/Geonkick-Synthesizer/geonkick) | (C++, C, custom GUI framework) | - Advanced drum synthesizer.
- [gRainbow](https://github.com/StrangeLoopsAudio/gRainbow) | (C++, [JUCE]) | - A synthesizer that uses pitch detection to choose candidates for granular synthesis or sampling.
- [Havregryn](https://github.com/vsandstrom/Havregryn) | (Rust, [nih-plug], [Vizia]) | - A granular delay and texture synthesizer.
- [Helm](https://github.com/mtytel/helm) | (C++, [JUCE]) | - High-quality modern monophonic synthesizer. The older sibling to Vital. The oscillators are not stereo though.
- [jc303](https://github.com/midilab/jc303) | (C++, [JUCE]) | - A nice Roland TB-303 clone.
- [Mika Micro](https://github.com/tesselode/mika-micro) | (C++, [WDL-OL]) | - A nice and simple synthesizer with a clean design.
- [Monique Mono-Synth](https://github.com/surge-synthesizer/monique-monosynth) | (C++, [JUCE]) | - High-quality subtractive monophonic synth. Now open source!
- [Ninjas 2](https://github.com/clearly-broken-software/ninjas2) | (C++, [DPF]) | - Sample slicer and player.
- [OB-Xd](https://github.com/reales/OB-Xd) | (C++, [JUCE]) | - A high quality subtractive analog synth modeled after the Oberheim OB-X.
- [OctaSine](https://github.com/greatest-ape/OctaSine) | ([Rust], [Iced], raw plugins APIs) | - A versatile FM synth written in full-stack Rust.
- [Odin 2](https://github.com/TheWaveWarden/odin2) | (C++, [JUCE]) | - Modern analogue-modeled hybrid synthesizer.
- [OpenB3](https://github.com/michele-perrone/OpenB3) | (C++, [JUCE]) | - A nice sounding tonewheel organ and rotary speaker emulator. The younger sibling to [setBfree](https://github.com/pantherb/setBfree).
- [OS-251](https://github.com/utokusa/OS-251) | (C++, [JUCE]) | - A nice sounding lo-fi synthesizer.
- [Resonarium](https://github.com/gabrielsoule/resonarium) | (C++, [JUCE]) | - An MPE-compatible expressive physical modeling synthesizer. (Still in development at the time of this writing).
- [sfizz](https://github.com/sfztools/sfizz-ui) | (C++, [Faust], [VSTGUI]) | - A sampler that plays [SFZ](https://sfzformat.com/) files. (SFZ is like SoundFonts but with more features).
- [Spiro](https://github.com/p-o-l-e/spiro.git) | (C++, [JUCE]) | - A semi-modular synthesizer with a beautiful interface.
- [Surge XT](https://github.com/surge-synthesizer/surge) | (C++, [JUCE]) | - Feature-rich hybrid synthesizer that was once sold as a proprietary product. (It has since evolved into its own thing with many new features added.)
- [Synth2](https://github.com/klknn/kdr) | (D, [Dplug]) | - A recreation of the classic Synth1 virtual synth. (Still a work in progress).
- [Terrain](https://github.com/aaronaanderson/Terrain) | (C++, [JUCE]) | - A unique wave terrain synthesizer plugin.
- [Tunefish](https://github.com/paynebc/tunefish?tab=readme-ov-file) | (C++, [JUCE]) | - A neat little additive synthesizer.
- [Vaporizer2](https://github.com/VASTDynamics/Vaporizer2) | (C++, [JUCE]) | - Feature-rich wavetable synthesizer that was once a proprietary product.
- [Vital] | (C++, [JUCE]) | - An incredibly powerful and high quality modern synthesizer. Rivals the likes of Xfer Serum and NI Massive.
  - There is also a fully GPLv3-licensed fork called [Vitalium] that has all the non-GPL stuff removed.
- [Wavetable](https://github.com/FigBug/Wavetable) | (C++, [JUCE]) | - Sleek wavetable synthesizer with a great clean sound.
- [ZynAddSubFX](https://github.com/zynaddsubfx/zynaddsubfx) | (C++, [DPF]) | - Feature-rich additive synthesizer with a great clean sound. Also sold as a commercial product.

## Audio FX

- [Aether](https://github.com/Dougal-s/Aether) | (C++, [Pugl]) | - Beautiful shimmering reverb based on the `CloudSeed` plugin by Valdemar Erlingsson. I choose this over the original as that uses a Windows-only C# platform for its GUI.
- [AIDA-X](https://github.com/AidaDSP/AIDA-X) | (C++, [DPF]) | - An amp model player that can load AI-trained models of music gear.
- [BinAural](https://github.com/twoz/binaural-vst) | (C++, [JUCE]) | - A mono-to-stereo plugin that positions sound in a 3D space using Head-Related Transfer Functions.
- [Castello Reverb](https://github.com/lucianoiam/castello) | (C++, [DPF], [dpfwebui]) | - A small reverb plugin with a webview-based UI.
- [Caverb](https://github.com/toasty-ghost/ASE_KM_Caverb) | (C++, [VSTGUI]) | - An algorithmic room reverb plugin with a sleek GUI. It also contains technical information on how the DSP works.
- [CHOMP](https://github.com/yaboypax/PaxMBClip) | (C++, [JUCE]) | - A high quality multiband clipper plugin.
- [CloudReverb](https://github.com/xunil-cloud/CloudReverb) | (C++, [DPF]) | - Another reverb plugin based on the `CloudSeed` plugin by Valdemar Erlingsson. I choose this over the original as that uses a Windows-only C# platform for its GUI.
- [Cocoa Delay](https://github.com/tesselode/cocoa-delay) | (C++, [WDL-OL]) | - A nice delay plugin with ducking, saturation, filtering, and pitching features.
- [CTAG Dynamic Range Compressor](https://github.com/p-hlp/CTAGDRC) | (C++, [JUCE]) | - A simple general-purpose compressor plugin.
- [DelayArchitect](https://github.com/jpcima/DelayArchitect) | (C++, [JUCE]) | - A feature-rich delay designer plugin.
- [Delay Intervals](https://github.com/Matth-ewe-f/audio-plugin-delay-intervals) | (C++, [JUCE]) | - An audio plugin that can create fully customizable delay patterns.
- [Dragonfly Reverb](https://github.com/michaelwillis/dragonfly-reverb) | (C++, [DPF]) | - Algorithmic reverb based on [Freeverb].
- [Dust Saturator](https://github.com/Everither/dust-saturator) | ([Rust], [nih-plug], [Vizia]) | - A distortion plugin with a unique distortion algorithm.
- [Fire](https://github.com/jerryuhoo/Fire) | (C++, [JUCE]) | - A multiband waveshaper with a great looking UI.
- [Flutterbird](https://github.com/tesselode/flutterbird) | (C++, [WDL-OL]) | - Simple multi-lfo than modulates pitch and volume, creating a "fluttering" effect.
- [Free Clip](https://gitlab.com/JHVenn/Free-Clip) | (C++, [JUCE]) | - A nice sounding waveshaper plugin.
- [Frequalizer](https://github.com/ffAudio/Frequalizer) | (C++, [JUCE]) | - An equalizer plugin using JUCE's new dsp module.
- [Fogpad](https://github.com/linuxmao-org/fogpad-port) | (C++, [DPF]) | - Reverb plugin where reflections can be frozen, filtered, pitch-shifted, and mangled.
- [Glorious](https://github.com/TitanChariotsBB/Glorious) | (C++, [JUCE]) | - A chorus plugin modeled after the famous chorus circuit from the Roland Juno series of synths.
- [lamb](https://github.com/magnetophon/lamb-rs) | ([Faust], [Rust], [nih-plug], [Vizia]) | - A clean lookahead compressor/limiter.
- [Audio Sampler](https://github.com/arunas-cesonis/live-sampler) | ([Rust], [nih-plug], [Vizia]) | - A live audio sampler plugin written in [Rust].
- [Luftikus] | (C++, [JUCE]) | - Analogue modeled equalizer.
- [MAIM](https://github.com/ArdenButterfield/Maim) | (C++, [JUCE]) | - A unique distortion effect which "circuit bends an MP3 encoder in real time".
- [Misstortion](https://github.com/nimbletools/misstortion1) | (C++, [JUCE]) | - Good quality hard/soft clipper.
- [Molot Lite](https://github.com/magnetophon/molot-lite) | (C++, [iPlug2]) | - A cut-down version of the Molot compressor by Tokyo Dawn Records. It has a lot of color and character.
- [Mverb](https://github.com/DISTRHO/MVerb) | (C++, [DPF]) | - Nice-sounding plate reverb.
- [PeakEater](https://github.com/vvvar/PeakEater) | (C++, [JUCE]) | - A nice waveshaping plugin with a sleek UI.
- [Reach](https://github.com/Sinuslabs/Reach) | (C++, [Faust], [JUCE]) | - Extraterrestrial reverb with a unique sound. It is also sold as a commercial product.
- [Reverse Camel](https://github.com/soerenbnoergaard/reverse-camel) | (C++, [DPF]) | - A black-box reverse engineered version of the famous Camel Crusher plugin. It also contains a Jupyter notebook explaining how it works.
- [Room Reverb](https://github.com/cvde/RoomReverb) | (C++, [JUCE]) | - Nice sounding algorithmic reverb based on [Freeverb].
- [sand_stretch](https://github.com/s4n7r0/sand_stretch) | (C++, [JUCE]) | - A remake of the dblue Stretch plugin.
- [Space Chili](https://github.com/glafiro/space-chili) | (C++, [JUCE]) | - A delay and chorus plugin with a sleek interface.
- [Squeezer](https://github.com/mzuther/Squeezer) | (C++, [JUCE]) | - Flexible general-purpose audio compressor with a "touch of citrus".
- [TimeStretch](https://github.com/spluta/TimeStretch) | ([Rust], [SuperCollider], Python, gui-less) | - A refinement of the famous [PaulStretch](http://hypermammut.sourceforge.net/paulstretch) time stretching effect. Includes a PDF explaining the DSP.
- [Transfer](https://github.com/MeijisIrlnd/Transfer) | (C++, [JUCE]) | - A waveshaper plugin which JIT-compiles any nonlinear function inputted by the user.
- [Utility Clone](https://github.com/m1m0zzz/utility-clone) | (C++, [JUCE]) | - A remake of the Utility plugin in Ableton.
- [utilities](https://github.com/butchwarns/utilities) | (C++, [JUCE]) | - A plugin that contains a bunch of simple but useful utilities.
- [Valentine](https://github.com/tote-bag-labs/valentine) | (C++, [JUCE]) | - A nice compressor/saturator that is meant to "pump and breath".
- [VitaliumVerb](https://github.com/BillyDM/vitalium-verb) | ([Rust], [nih-plug], [Vizia]) | - A Rust port of the reverb module from the [Vital]/[Vitalium] synthesizer, with some added improvements and optimizations.
- [Wolf Shaper](https://github.com/pdesaulniers/wolf-shaper) | (C++, [DPF]) | - Good quality waveshaper with support for unlimited nodes.

## MIDI FX

- [Helio Workstation](https://github.com/helio-fm/helio-workstation) | (C++, [JUCE]) | - A very modern and feature-rich sequencer.
- [QMidiArp](https://github.com/emuse/qmidiarp) | (C++, [robtk], [Pugl]) | - Advanced arpeggiator, sequencer, and MIDI LFO.
- [Ripchord](https://github.com/trackbout/ripchord) | (C++, [JUCE]) | - A MIDI plugin that can create, perform and remix chord progressions.
  - There is also a [fork](https://github.com/prg318/ripchord) that adds support for Linux.
- [ShowMIDI](https://github.com/gbevin/ShowMIDI) | (C++, [JUCE]) | - A tool to effortlessly visualize MIDI activity.
- [Stochas](https://github.com/surge-synthesizer/stochas) | (C++, [JUCE]) | - An advanced probabilistic polyrythmic sequencer. Made by the same team behind the [Surge XT] synthesizer.

## Meters & Visualizers

- [cqt-analyzer](https://github.com/jmerkt/cqt-analyzer) | (C++, [JUCE]) | - A spectral analyzer that offers logarithmic equally spaced resolution across all octaves.
- [EasySSP](https://github.com/automatl/audio-dsp-multi-visualize/) | (C++, [JUCE]) | - Real-time spectrum analyzer and stereo analyzer plugin.
- [K-Meter](https://github.com/mzuther/K-Meter) | (C++, [JUCE]) | - A feature-rich loudness meter.
- [LUFS Meter](https://github.com/klangfreund/LUFSMeter) | (C++, [JUCE]) | - Real-time loudness meter with support for several international loudness standards.
- [MultiMeter](https://github.com/RealAlexZ/MultiMeter) | (C++, [JUCE]) | - A swiss-army-knife metering plugin with a sleek UI.
- [Spectacle](https://github.com/jpcima/spectacle) | (C++, [DPF]) | - Modern real-time spectrum analyzer plugin.
- [Spectrum](https://github.com/tadmn/spectrum) | (C++, [Visage]) | - A high quality and high performance spectrum analyzer plugin.
- [Wolf Spectrum](https://github.com/pdesaulniers/wolf-spectrum) | (C++, [DPF]) | - Real-time heat-map spectrum analyzer plugin.

# Open Source Software

## DAWs & Hosts

- [Ardour](https://ardour.org/) - Feature-rich DAW. Focuses more on recorded music production over electronic music production.
- [Audacity](https://github.com/audacity/audacity) - Popular multi-track audio editor. There is also a fully-libre open source fork called [Tenacity](https://github.com/tenacityteam/tenacity).
- [Bass Studio](https://github.com/nidefawl/bass-studio) - A feature-rich DAW that was recently made open source.
- [Bespoke Synth] - A very modular synthesizer with support for complex routing, modulation, and sequencing. It can even host VST plugins, blurring the lines between synth and DAW.
- [Cardinal] - An open source modular synthesizer plugin that can host [VCV Rack] plugins.
- [Carla](https://kx.studio/Applications:Carla) - Cross platform plugin host with support for many plugin formats.
- [Furnace](https://github.com/tildearrow/furnace) - A modern, feature-rich chiptune tracker. 
- [Hydrogen](https://github.com/hydrogen-music/hydrogen) - An advanced drum sequencer for Linux, MacOS, and Windows.
- [Jackdaw](https://github.com/chvolow24/jackdaw) - A stripped-down, keyboard-focused digital audio workstation.
- [LGML](https://github.com/OrganicOrchestra/LGML) - A flexible & nodal audio host for live performances.
- [LMMS](https://github.com/LMMS/lmms) - Feature-rich DAW focused on electronic music production. Contains many built-in synths and effects.
- [Mixxx](https://github.com/mixxxdj/mixxx) - Popular cross-platform application for performing live DJ mixes.
- [pxtone collab](https://github.com/yuxshao/ptcollab) - A music editor with collaborative editing features.
- [Stargate](https://github.com/stargatedaw/stargate) - A new and lightweight DAW with a powerful routing matrix and a suite of built-in plugins. It also aims to run well on low-spec hardware such as Raspberry Pi's.

## Musical Notation

- [composing.studio](https://github.com/ekzhang/composing.studio) - An experimental open-source web app that allows you to collaborate on editing sheet music.
- [MuseScore](https://musescore.org) - A popular and mature open-source sheet music editor.

## Other

- [MasVisGtk](https://github.com/itprojects/MasVisGtk) - An audio loudness analysis tool that can be used to detect mastering defects.
- [melonix](https://github.com/mika314/melonix) - A pitch correction application written using ImGui and OpenGL 3. Currently a work in progress at the time of this writing.
- [Sæmpl](https://github.com/jonasblome/Saempl) - A sample manager that can automatically sort samples by properties like loudness, pitch, and tempo.
- [Ultimate Vocal Remover](https://github.com/Anjok07/ultimatevocalremovergui) - A state-of-the-art program that uses machine learning to separate vocals from a mix.

# More Lists

- [Awesome Linux Clap List](https://github.com/RustoMCSpit/awesome-linux-clap-list) - A list of FOSS clap plugins that work for Linux
- [HyMPS](https://www.forart.it/HyMPS) - A large list of open source software and libraries for audio/video content production.
- [OpenAudio](https://github.com/webprofusion/OpenAudio) - A large list of open source audio plugins, apps, and other projects.
- [SpotlightKid's list](https://github.com/stars/SpotlightKid/lists/audio-midi-applications) - A large, actively updated list of open source audio plugins and apps.
- [StudioRack](https://studiorack.github.io/studiorack-site/) - An app for browsing and downloading from a large catalogue of open source plugins and multisample instruments.

[JUCE]: https://juce.com/
[DPF]: https://github.com/DISTRHO/DPF
[GTK]: https://www.gtk.org/
[Dplug]: https://github.com/AuburnSounds/Dplug
[JSFX]: https://www.reaper.fm/sdk/js/js.php
[Lua]: https://www.lua.org/
[nih-plug]: https://github.com/robbert-vdh/nih-plug
[Rust]: https://www.rust-lang.org/
[egui]: https://github.com/emilk/egui
[Iced]: https://github.com/iced-rs/iced
[Vizia]: https://github.com/vizia/vizia
[Pugl]: https://github.com/lv2/pugl
[SOUL]: https://github.com/soul-lang/SOUL
[Faust]: https://faust.grame.fr/
[WDL-OL]: https://github.com/olilarkin/wdl-ol
[VSTGUI]: https://github.com/steinbergmedia/vstgui/
[iPlug2]: https://github.com/iPlug2/iPlug2
[SuperCollider]: https://supercollider.github.io/
[robtk]: https://github.com/x42/robtk
[Dear ImGui]: https://github.com/ocornut/imgui
[libxputty]: https://github.com/brummer10/libxputty
[Luftikus]: https://github.com/lkjbdsp/lkjb-plugins/tree/master/Luftikus
[Bespoke Synth]: https://github.com/BespokeSynth/BespokeSynth
[Cardinal]: https://github.com/DISTRHO/Cardinal
[VCV Rack]: https://vcvrack.com/
[Freeverb]: https://ccrma.stanford.edu/~jos/pasp/Freeverb.html
[Eurorack]: https://en.wikipedia.org/wiki/Eurorack
[Visage]: https://github.com/VitalAudio/visage
[Vital]: https://github.com/mtytel/vital
[dpfwebui]: https://github.com/lucianoiam/dpfwebui
[Vitalium]: https://github.com/DISTRHO/DISTRHO-Ports/tree/master/ports-juce6.0/vitalium
