# Plugin Development Frameworks
A list of software stacks/frameworks used to make audio plugins, along with their pros and cons.

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
      - Currently only targets the VST2 plugin format. CLAP, VST3, AU, LV2, and JACK targets are currently planned.
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

[`Steinberg's VST3 License`]: https://developer.steinberg.help/display/VST/VST+3+Licensing

[`vst-rs`]: https://github.com/RustAudio/vst-rs
[`baseplug`]: https://github.com/wrl/baseplug
[`baseview`]: https://github.com/RustAudio/baseview
[`iced_baseview`]: https://github.com/BillyDM/iced_baseview
[`iced`]: https://github.com/hecrj/iced
[`iced_audio`]: https://github.com/iced-rs/iced_audio
[`iced-baseplug-examples`]: https://github.com/BillyDM/iced-baseplug-examples
[`tuix`]: https://github.com/geom3trik/tuix
[`tuix_audio_synth`]: https://github.com/geom3trik/tuix_audio_synth
[`tuix_baseview_test_vst2`]: https://github.com/geom3trik/tuix_baseview_test_vst2
[`egui`]: https://github.com/emilk/egui
[`egui-baseview`]: https://github.com/BillyDM/egui-baseview
[`egui_baseview_test_vst2`]: https://github.com/DGriffin91/egui_baseview_test_vst2
[`imgui-rs`]: https://github.com/imgui-rs/imgui-rs
[`Dear ImGui`]: https://github.com/ocornut/imgui
[`imgui-baseview`]: https://github.com/BillyDM/imgui-baseview
[`imgui_baseview_test_vst2`]: https://github.com/DGriffin91/imgui_baseview_test_vst2
[`imgui-compressor`]: https://github.com/DGriffin91/compressor-plugin

[`DISTRHO Plugin Framework`]: https://github.com/DISTRHO/DPF

[`Dplug`]: https://github.com/AuburnSounds/Dplug

[`JUCE`]: https://github.com/juce-framework/JUCE

[`Tracktion Engine`]: https://github.com/Tracktion/tracktion_engine/

[`iPlug2`]: https://github.com/iPlug2/iPlug2