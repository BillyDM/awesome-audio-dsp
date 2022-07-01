# Open Source Plugins & Software
A list of open source audio software that you can inspect and learn from.

## Collections
- [`Airwindows Plugins`] - Many, many good quality effects and experiments developed over many years.
  There are a *ton* of plugins here, so here is a list of community favorites:
  - [`density`]
  - [`pressure4`]
  - [`totape5`]
  - [`ironoxide`]
- [`zam-plugins`] - A suite of good quality mixing/mastering plugins. The limiter, tube amp, and multiband compressor are particularly good.
- [`LSP Plugins`] - Another collection of good quality mixing/mastering effects.
- [`sjaehn`] - Several cool MIDI based slicing/glitching effects and synthesizers.
- [`x42-plugins`] - A collection of good quality effects and visualizers. Some plugins are also sold as a commercial product. The compressor is particularly good.
- [`EQ10Q`] - A suite of plugins containing a 10-band parametric equalizer, gate, compressor, bass enhancer, and mid-side encoders.
- [`Shiru Plugins`] - A suite of old video-game sound chips synths and effects.
- [`DISTRHO-Ports`] - A whole bunch of plugins ported to work on Linux/LV2.
- [`DISTRHO Plugin Framework`] - Has a list of plugins that were made using this framework.
- [`lkjb plugins`] - Additional plugins made by the creator of [`Luftikus`].
- [`SOUL-VA`] - A non-trivial virtual analog filter library written in [`SOUL`]. Plugin versions are also sold as commercial products.

## Synths
- [`Vital`] - An incredibly powerful and high quality modern synthesizer. Rivals that of Xfer Serum and NI Massive.
  - There is also a fully GPLv3-licensed fork called [`Vitalium`] that has all the non-GPL stuff removed.
- [`Helm`] - High-quality modern monophonic synthesizer. The older sibling to Vital. The oscillators are not stereo though.
- [`Surge`] - Feature-rich hybrid synthesizer that was once sold as a commercial product.
- [`Monique Mono-Synth`] - High-quality subtractive monophonic synth. Now open source!
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
- [`OctaSine`] - A versitile FM synth written in full-stack [`Rust`].

## Audio FX
- [`Wolf Shaper`] - Good quality waveshaper with support for unlimited nodes.
- [`Mverb`] - Nice-sounding plate reverb.
- [`Room Reverb`] - Nice sounding algorithmic reverb based on [`Freeverb`].
- [`Dragonfly Reverb`] - Algorithmic reverb based on [`Freeverb`].
- [`CloudReverb`] - Beautiful shimmering reverb based on the `CloudSeed` plugin by Valdemar Erlingsson. I choose this over the original as that uses a Windows-only C# platform for its GUI.
  - There is also a port of this plugin with a GUI called [`Aether`].
- [`Luftikus`] - Good quality analogue modeled equalizer.
- [`Fogpad`] - Reverb plugin where reflections can be frozen, filtered, pitch-shifted, and mangled.
- [`Misstortion`] - Good quality hard/soft clipper.
- [`Cocoa Delay`] - A nice delay plugin with ducking, saturation, filtering, and pitching features.
- [`Flutterbird`] - Simple multi-lfo than modulates pitch and volume, creating a "fluttering" effect.
- [`DelayArchitect`] - A feature-rich delay designer plugin.
- [`TimeStretch`] - A refinement of the famous [`PaulStretch`] time stretching effect. Includes a PDF explaining the DSP.

## MIDI FX
- [`Helio Workstation`] - A very modern and feature-rich sequencer.
- [`QMidiArp`] - Advanced arpeggiator, sequencer, and MIDI LFO.
- [`Stochas`] - An advanced probabilistic polyrythmic sequencer. Made by the same team behind the [`Surge`] synthesizer.

## Meters & Visualizers
- [`Spectacle`] - Modern real-time spectrum analyzer plugin.
- [`Wolf Spectrum`] - Real-time heat-map spectrum analyzer plugin.
- [`EasySSP`] - Real-time spectrum analyzer and stereo analyzer plugin.
- [`LUFS Meter`] - Real-time loudness meter with support for several international loudness standards.

## DAWs & Hosts
- [`Meadowlark`] - Definitely biased here since this is my main project that I work on full-time. It's still in its very early stages, but check it out if you're interested in contributing! :)
- [`Ardour`] - Feature-rich DAW. Focuses more on recorded music production over electronic music production.
- [`LMMS`] - Feature-rich DAW focused on electronic music production. Contains many built-in synths and effects.
- [`Audacity`] - Popular multi-track audio editor. There is also a fully-libre open source fork called [`Tenacity`].
- [`Carla`] - Cross platform plugin host with support for many plugin formats.
- [`Bespoke Synth`] - A very modular synthesizer with support for complex routing, modulation, and sequencing. It can even host VST plugins, blurring the lines between synth and DAW.
- [`termdaw`] - A neat little DAW experiment that uses a terminal as its interface instead of a GUI.

## Musical Notation
- [`MuseScore`] - A popular and mature open-source sheet music editor.
- [`composing.studio`] - An experimental open-source web app that allows you to collaborate on editing sheet music.

[`Airwindows Plugins`]: https://github.com/airwindows/airwindows/tree/master/plugins
[`density`]: https://github.com/airwindows/airwindows/tree/master/plugins/LinuxVST/src/Density
[`pressure4`]: https://github.com/airwindows/airwindows/tree/master/plugins/LinuxVST/src/Pressure4
[`totape5`]: https://github.com/airwindows/airwindows/tree/master/plugins/LinuxVST/src/ToTape5
[`ironoxide`]: https://github.com/airwindows/airwindows/tree/master/plugins/LinuxVST/src/IronOxide5
[`zam-plugins`]: https://github.com/zamaudio/zam-plugins
[`LSP Plugins`]: https://github.com/sadko4u/lsp-plugins
[`sjaehn`]: https://github.com/sjaehn?tab=repositories
[`x42-plugins`]: https://github.com/x42/x42-plugins
[`EQ10Q`]: http://eq10q.sourceforge.net/
[`Shiru Plugins`]: https://github.com/linuxmao-org/shiru-plugins
[`DISTRHO-Ports`]: https://github.com/DISTRHO/DISTRHO-Ports
[`DISTRHO Plugin Framework`]: https://github.com/DISTRHO/DPF
[`lkjb plugins`]: https://github.com/lkjbdsp/lkjb-plugins
[`SOUL-VA`]: https://github.com/thezhe/SOUL-VA
[`SOUL`]: https://github.com/soul-lang/SOUL

[`Vital`]: https://github.com/mtytel/vital
[`Vitalium`]: https://github.com/DISTRHO/DISTRHO-Ports/tree/master/ports-juce6/vitalium
[`Helm`]: https://github.com/mtytel/helm
[`Surge`]: https://github.com/surge-synthesizer/surge
[`Monique Mono-Synth`]: https://github.com/surge-synthesizer/monique-monosynth
[`Dexed`]: https://github.com/asb2m10/dexed
[`ZynAddSubFX`]: https://github.com/zynaddsubfx/zynaddsubfx
[`Odin 2`]: https://github.com/TheWaveWarden/odin2
[`Geonkick`]: https://github.com/iurie-sw/geonkick
[`ADLplug`]: https://github.com/jpcima/ADLplug
[`Ninjas 2`]: https://github.com/clearly-broken-software/ninjas2
[`Mika Micro`]: https://github.com/tesselode/mika-micro
[`Synth2`]: https://github.com/klknn/synth2
[`Sfizz`]: https://github.com/sfztools/sfizz
[`SFZ`]: https://sfzformat.com/
[`Bespoke Synth`]: https://github.com/BespokeSynth/BespokeSynth
[`OctaSine`]: https://github.com/greatest-ape/OctaSine

[`Wolf Shaper`]: https://github.com/pdesaulniers/wolf-shaper
[`Mverb`]: https://github.com/DISTRHO/MVerb
[`Room Reverb`]: https://github.com/cvde/RoomReverb
[`Dragonfly Reverb`]: https://github.com/michaelwillis/dragonfly-reverb
[`Freeverb`]: https://ccrma.stanford.edu/~jos/pasp/Freeverb.html
[`CloudReverb`]: https://github.com/xunil-cloud/CloudReverb
[`Aether`]: https://github.com/Dougal-s/Aether
[`Luftikus`]: https://github.com/lkjbdsp/lkjb-plugins/tree/master/Luftikus
[`Fogpad`]: https://github.com/linuxmao-org/fogpad-port
[`Misstortion`]: https://github.com/nimbletools/misstortion1
[`Cocoa Delay`]: https://github.com/tesselode/cocoa-delay
[`Flutterbird`]: https://github.com/tesselode/flutterbird
[`DelayArchitect`]: https://github.com/jpcima/DelayArchitect
[`TimeStretch`]: https://github.com/spluta/TimeStretch
[`PaulStretch`]: http://hypermammut.sourceforge.net/paulstretch

[`Helio Workstation`]: https://github.com/helio-fm/helio-workstation
[`QMidiArp`]: https://github.com/emuse/qmidiarp
[`Stochas`]: https://github.com/surge-synthesizer/stochas

[`Spectacle`]: https://github.com/jpcima/spectacle
[`Wolf Spectrum`]: https://github.com/pdesaulniers/wolf-spectrum
[`EasySSP`]: https://github.com/automatl/audio-dsp-multi-visualize/
[`LUFS meter`]: https://github.com/klangfreund/LUFSMeter

[`Meadowlark`]: https://github.com/MeadowlarkDAW/Meadowlark
[`Ardour`]: https://ardour.org/
[`LMMS`]: https://github.com/LMMS/lmms
[`Audacity`]: https://github.com/audacity/audacity
[`Tenacity`]: https://github.com/tenacityteam/tenacity
[`Carla`]: https://kx.studio/Applications:Carla
[`termdaw`]: https://github.com/ocdy1001/termdaw

[`MuseScore`]: https://musescore.org
[`composing.studio`]: https://github.com/ekzhang/composing.studio

[`Rust`]: https://www.rust-lang.org/
