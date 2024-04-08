# Open Source Plugins & Software
A list of open source audio software that you can inspect and learn from, along with the language and framework used to make them.

# Open Source Plugins

## Collections

(Note, individual plugins are not listed in the `Synths`/`Audio FX`/`MIDI FX`/`Meters & Visualizers` sections if they appear in one of these collections.)

- [Airwindows Plugins](https://github.com/airwindows/airwindows/tree/master/plugins) | (C++, gui-less, raw plugin APIs) | - Lots of good quality effects and experiments developed over many years.
  There are a *ton* of plugins here, so here is a list of some community favorites:
  - [density](https://github.com/airwindows/airwindows/tree/master/plugins/LinuxVST/src/Density)
  - [ironoxide](https://github.com/airwindows/airwindows/tree/master/plugins/LinuxVST/src/IronOxide5)
  - [pressure4](https://github.com/airwindows/airwindows/tree/master/plugins/LinuxVST/src/Pressure4)
  - [totape5](https://github.com/airwindows/airwindows/tree/master/plugins/LinuxVST/src/ToTape5)
- [Calf Studio gear](https://github.com/calf-studio-gear/calf) | (C++, custom [GTK] framework) | - A large collection of plugins aimed at a professional audience.
- [Chowdhury DSP](https://github.com/Chowdhury-DSP) | (C++, [JUCE]) | - A collection of high quality effect plugins (as well as a kick drum synthesizer). A lot of these plugins make use of use of cutting-edge neural network inferencing.
- [DISTRHO Plugin Framework](https://github.com/DISTRHO/DPF) | (C++, [DPF]) | - Has a list of plugins that were made using this framework.
- [DISTRHO-Ports](https://github.com/DISTRHO/DISTRHO-Ports) | (C++, [JUCE]) | - A whole bunch of plugins ported to work on Linux/LV2.
- [Dplug] | (D, [Dplug]) | - Contains some example plugins using the framework.
- [EQ10Q](http://eq10q.sourceforge.net/) | (C++, custom [GTK] framework) | - A suite of plugins containing a 10-band parametric equalizer, gate, compressor, bass enhancer, and mid-side encoders.
- [JoepVanlier's JSFX plugins](https://github.com/JoepVanlier/JSFX) | ([JSFX], [Lua]) | - A collection of cool plugins and scripts for Reaper. Some of the GUIs are really stunning.
- [lkjb plugins](https://github.com/lkjbdsp/lkjb-plugins) | (C++, [JUCE]) | - Additional plugins made by the creator of [Luftikus].
- [LSP Plugins](https://github.com/lsp-plugins) | (C++, custom GUI framework) | - A collection of good quality mixing/mastering effects for Linux.
- [Mrugalla Plugins](https://github.com/Mrugalla) | (C++, [JUCE]) | - A collection of modern and unique plugins by Florian Mrugalla.
- [nih-plug](https://github.com/robbert-vdh/nih-plug) | ([Rust], [nih-plug], [egui], [Iced], [Vizia]) | - Contains a collection of plugins written in Rust, including the amazing [Spectral Compressor](https://github.com/robbert-vdh/nih-plug/tree/master/plugins/spectral_compressor) plugin.
- [Shiru Plugins](https://github.com/linuxmao-org/shiru-plugins) | (C++, [DPF]) | - A suite of old video-game sound chips synths and effects.
- [sjaehn](https://github.com/sjaehn?tab=repositories) | (C++, [Pugl]) | - Several cool MIDI based slicing/glitching effects and synthesizers.
- [SocaLabs Plugins](https://github.com/FigBug/SocaLabs) | (C++, [JUCE]) | - A collection of plugins made by SocaLabs.
- [SOUL-VA](https://github.com/thezhe/SOUL-VA) | ([SOUL]) | - A non-trivial virtual analog filter library written in [SOUL](https://github.com/soul-lang/SOUL). Plugin versions are also sold as commercial products.
- [VCV Library database](https://github.com/VCVRack/library) - An official database of [VCV Rack] plugins, containing both commercial and open source plugins.
- [x42-plugins](https://github.com/x42/x42-plugins) | (C, [robtk], [Pugl]) | - A collection of good quality effects and visualizers. Some plugins are also sold as a commercial product.
- [zam-plugins](https://github.com/zamaudio/zam-plugins) | (C++, [DPF]) | - A suite of good quality mixing/mastering plugins.
- [ZL-Audio Plugins](https://github.com/ZL-Audio) | (C++, [JUCE]) | - A collection of good quality plugins including a fancy parametric equalizer, saturator, and compressor.

## Synths

- [ADLplug](https://github.com/jpcima/ADLplug) | (C++, [JUCE]) | - Emulation of FM-synthesizers found in some classic game consoles.
- [Bespoke Synth] | (C++, [JUCE]) | - A very modular synthesizer with support for complex routing, modulation, and sequencing. It can even host VST plugins, blurring the lines between synth and DAW.
- [Cardinal] | (C++, [DPF]) | - An open source modular synthesizer plugin that can host [VCV Rack] plugins.
- [Dexed](https://github.com/asb2m10/dexed) | (C++, [JUCE]) | - Synthesizer closely modelled after the Yamaha DX7.
- [DigiDrie](https://github.com/magnetophon/DigiDrie) | ([Faust], C++, [DPF]) | - A "monster" monophonic synth.
- [Geonkick](https://github.com/Geonkick-Synthesizer/geonkick) | (C++, C, custom GUI framework) | - Advanced drum synthesizer.
- [gRainbow](https://github.com/StrangeLoopsAudio/gRainbow) | (C++, [JUCE]) | - A synthesizer that uses pitch detection to choose candidates for granular synthesis or sampling.
- [Helm](https://github.com/mtytel/helm) | (C++, [JUCE]) | - High-quality modern monophonic synthesizer. The older sibling to Vital. The oscillators are not stereo though.
- [Mika Micro](https://github.com/tesselode/mika-micro) | (C++, [WDL-OL]) | - A nice and simple synthesizer with a clean design.
- [Monique Mono-Synth](https://github.com/surge-synthesizer/monique-monosynth) | (C++, [JUCE]) | - High-quality subtractive monophonic synth. Now open source!
- [Ninjas 2](https://github.com/clearly-broken-software/ninjas2) | (C++, [DPF]) | - Sample slicer and player.
- [OB-Xd](https://github.com/reales/OB-Xd) | (C++, [JUCE]) | - A high quality subtractive analog synth modeled after the Oberheim OB-X.
- [OctaSine](https://github.com/greatest-ape/OctaSine) | ([Rust], [Iced], raw plugins APIs) | - A versatile FM synth written in full-stack Rust.
- [Odin 2](https://github.com/TheWaveWarden/odin2) | (C++, [JUCE]) | - Modern analogue-modeled hybrid synthesizer.
- [sfizz](https://github.com/sfztools/sfizz-ui) | (C++, [Faust], [VSTGUI]) | - A sampler that plays [SFZ](https://sfzformat.com/) files. (SFZ is like SoundFonts but with more features).
- [Spiro](https://github.com/p-o-l-e/spiro.git) | (C++, [JUCE]) | - A semi-modular synthesizer with a beautiful interface.
- [Surge XT](https://github.com/surge-synthesizer/surge) | (C++, [JUCE]) | - Feature-rich hybrid synthesizer that was once sold as a proprietary product. (It has since evolved into its own thing with many new features added.)
- [Synth2](https://github.com/klknn/kdr) | (D, [Dplug]) | - A recreation of the classic Synth1 virtual synth. (Still a work in progress).
- [Vaporizer2](https://github.com/VASTDynamics/Vaporizer2) | (C++, [JUCE]) | - Feature-rich wavetable synthesizer that was once a proprietary product.
- [Vital](https://github.com/mtytel/vital) | (C++, [JUCE]) | - An incredibly powerful and high quality modern synthesizer. Rivals the likes of Xfer Serum and NI Massive.
  - There is also a fully GPLv3-licensed fork called [Vitalium](https://github.com/DISTRHO/DISTRHO-Ports/tree/master/ports-juce6/vitalium) that has all the non-GPL stuff removed.
- [Wavetable](https://github.com/FigBug/Wavetable) | (C++, [JUCE]) | - Sleek wavetable synthesizer with a great clean sound.
- [ZynAddSubFX](https://github.com/zynaddsubfx/zynaddsubfx) | (C++, [DPF]) | - Feature-rich additive synthesizer with a great clean sound. Also sold as a commercial product.

## Audio FX

- [Aether](https://github.com/Dougal-s/Aether) | (C++, [Pugl]) | - Beautiful shimmering reverb based on the `CloudSeed` plugin by Valdemar Erlingsson. I choose this over the original as that uses a Windows-only C# platform for its GUI.
- [AIDA-X](https://github.com/AidaDSP/AIDA-X) | (C++, [DPF]) | - An amp model player that can load AI-trained models of music gear.
- [CloudReverb](https://github.com/xunil-cloud/CloudReverb) | (C++, [DPF]) | - Another reverb plugin based on the `CloudSeed` plugin by Valdemar Erlingsson. I choose this over the original as that uses a Windows-only C# platform for its GUI.
- [Cocoa Delay](https://github.com/tesselode/cocoa-delay) | (C++, [WDL-OL]) | - A nice delay plugin with ducking, saturation, filtering, and pitching features.
- [DelayArchitect](https://github.com/jpcima/DelayArchitect) | (C++, [JUCE]) | - A feature-rich delay designer plugin.
- [Dragonfly Reverb](https://github.com/michaelwillis/dragonfly-reverb) | (C++, [DPF]) | - Algorithmic reverb based on [Freeverb].
- [Flutterbird](https://github.com/tesselode/flutterbird) | (C++, [WDL-OL]) | - Simple multi-lfo than modulates pitch and volume, creating a "fluttering" effect.
- [Fogpad](https://github.com/linuxmao-org/fogpad-port) | (C++, [DPF]) | - Reverb plugin where reflections can be frozen, filtered, pitch-shifted, and mangled.
- [lamb](https://github.com/magnetophon/lamb-rs) | ([Faust], [Rust], [nih-plug], [Vizia]) | - A clean lookahead compressor/limiter.
- [Luftikus] | (C++, [JUCE]) | - Analogue modeled equalizer.
- [MAIM](https://github.com/ArdenButterfield/Maim) | (C++, [JUCE]) | - A unique distortion effect which "circuit bends an MP3 encoder in real time".
- [Misstortion](https://github.com/nimbletools/misstortion1) | (C++, [JUCE]) | - Good quality hard/soft clipper.
- [Molot Lite](https://github.com/magnetophon/molot-lite) | (C++, [iPlug2]) | - A cut-down version of the Molot compressor by Tokyo Dawn Records. It has a lot of color and character.
- [Mverb](https://github.com/DISTRHO/MVerb) | (C++, [DPF]) | - Nice-sounding plate reverb.
- [Room Reverb](https://github.com/cvde/RoomReverb) | (C++, [JUCE]) | - Nice sounding algorithmic reverb based on [Freeverb].
- [Squeezer](https://github.com/mzuther/Squeezer) | (C++, [JUCE]) | - Flexible general-purpose audio compressor with a "touch of citrus".
- [TimeStretch](https://github.com/spluta/TimeStretch) | ([Rust], [SuperCollider], Python, gui-less) | - A refinement of the famous [PaulStretch](http://hypermammut.sourceforge.net/paulstretch) time stretching effect. Includes a PDF explaining the DSP.
- [Valentine](https://github.com/tote-bag-labs/valentine) | (C++, [JUCE]) | - A nice compressor/saturator that is meant to "pump and breath".
- [Wolf Shaper](https://github.com/pdesaulniers/wolf-shaper) | (C++, [DPF]) | - Good quality waveshaper with support for unlimited nodes.

## MIDI FX
- [Helio Workstation](https://github.com/helio-fm/helio-workstation) | (C++, [JUCE]) | - A very modern and feature-rich sequencer.
- [QMidiArp](https://github.com/emuse/qmidiarp) | (C++, [robtk], [Pugl]) | - Advanced arpeggiator, sequencer, and MIDI LFO.
- [Ripchord](https://github.com/trackbout/ripchord) | (C++, [JUCE]) | - A MIDI plugin that can create, perform and remix chord progressions.
  - There is also a [fork](https://github.com/prg318/ripchord) that adds support for Linux.
- [Stochas](https://github.com/surge-synthesizer/stochas) | (C++, [JUCE]) | - An advanced probabilistic polyrythmic sequencer. Made by the same team behind the [Surge XT] synthesizer.

## Meters & Visualizers
- [EasySSP](https://github.com/automatl/audio-dsp-multi-visualize/) | (C++, [JUCE]) | - Real-time spectrum analyzer and stereo analyzer plugin.
- [LUFS Meter](https://github.com/klangfreund/LUFSMeter) | (C++, [JUCE]) | - Real-time loudness meter with support for several international loudness standards.
- [Spectacle](https://github.com/jpcima/spectacle) | (C++, [DPF]) | - Modern real-time spectrum analyzer plugin.
- [Wolf Spectrum](https://github.com/pdesaulniers/wolf-spectrum) | (C++, [DPF]) | - Real-time heat-map spectrum analyzer plugin.

# Open Source Software

## DAWs & Hosts
- [Ardour](https://ardour.org/) - Feature-rich DAW. Focuses more on recorded music production over electronic music production.
- [Audacity](https://github.com/audacity/audacity) - Popular multi-track audio editor. There is also a fully-libre open source fork called [Tenacity](https://github.com/tenacityteam/tenacity).
- [Bass Studio](https://github.com/nidefawl/bass-studio) - A feature-rich DAW that was recently made open source.
- [Bespoke Synth] - A very modular synthesizer with support for complex routing, modulation, and sequencing. It can even host VST plugins, blurring the lines between synth and DAW.
- [Cardinal] - An open source modular synthesizer plugin that can host [VCV Rack] plugins.
- [Carla](https://kx.studio/Applications:Carla) - Cross platform plugin host with support for many plugin formats.
- [LMMS](https://github.com/LMMS/lmms) - Feature-rich DAW focused on electronic music production. Contains many built-in synths and effects.
- [Mixxx](https://github.com/mixxxdj/mixxx) - Popular cross-platform application for performing live DJ mixes.
- [pxtone collab](https://github.com/yuxshao/ptcollab) - A music editor with collaborative editing features.
- [Stargate](https://github.com/stargatedaw/stargate) - A new and lightweight DAW with a powerful routing matrix and a suite of built-in plugins. It also aims to run well on low-spec hardware such as Raspberry Pi's.

## Musical Notation
- [composing.studio](https://github.com/ekzhang/composing.studio) - An experimental open-source web app that allows you to collaborate on editing sheet music.
- [MuseScore](https://musescore.org) - A popular and mature open-source sheet music editor.

## Other
- [Sæmpl](https://github.com/jonasblome/Saempl) - A sample manager that can automatically sort samples by properties like loudness, pitch, and tempo.
- [Ultimate Vocal Remover](https://github.com/Anjok07/ultimatevocalremovergui) - A state-of-the-art program that uses machine learning to separate vocals from a mix.

# More Lists

- [OpenAudio](https://github.com/webprofusion/OpenAudio) - A large list of open source audio plugins, apps, and other projects.

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
[Luftikus]: https://github.com/lkjbdsp/lkjb-plugins/tree/master/Luftikus
[Bespoke Synth]: https://github.com/BespokeSynth/BespokeSynth
[Cardinal]: https://github.com/DISTRHO/Cardinal
[VCV Rack]: https://vcvrack.com/
[Freeverb]: https://ccrma.stanford.edu/~jos/pasp/Freeverb.html
