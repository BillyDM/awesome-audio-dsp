# Plugin Development Frameworks
A list of software stacks/frameworks used to make audio plugins, along with their pros and cons.

- Please note that you must have a licensing agreement with Steinberg to *distribute* any VST2 and any non-GPLv3 VST3 plugins as per [`Steinberg's VST3 License`]. If you don't already have a VST2 license, you're out of luck since Steinberg doesn't support it anymore (yeah it stinks). Target VST3 instead in that case. Or better yet, target the new [`CLAP`] standard ;).

## [`nih-plug`]
  - Full-stack and modular framework with GUI in [`Rust`].
  - Fully open-source using a permissive license.
  - Targets CLAP and VST3 plugin formats.
  - Targets Linux, Mac, and Windows platforms.
  - Has several different options for GUI such as [`Vizia`], [`Iced`], and [`egui`].
  - Very new and still somewhat a work in progress, but the essential features you need to get started are there.
  - There is now a [`cookiecutter template`] to help get you started faster.

## [`DISTRHO Plugin Framework`]
  - Full-stack framework with GUI in C++.
  - Fully open-source using a permissive license.
  - Targets LADSPA, DSSI, LV2, VST2, and Jack plugin formats.
  - Targets Linux, Mac, and Windows platforms.

## [`Dplug`]
  - Full-stack framework with GUI in te D programming language.
  - Fully open-source using a permissive license.
  - The GUI framework has fancy physically-modeled rendering inspired by game engines.
  - Targets VST2, VST3, AUv2, AAX, and LV2 plugin formats.
  - Targets Linux, Mac, Windows, and Raspberry Pi platforms.
  - Used by several commercial plugins.

## [`JUCE`]
  - Full-stack framework with GUI in C++.
  - Open source, but some of its modules require a hefty commercial license to distribute any non-GPLv3 plugins.
  - Targets VST2, VST3, AUv2, AUv3, RTAS, and AAX plugin formats. Unofficial support for the CLAP standard is also in the works [`here`](https://github.com/free-audio/clap-juce-extensions).
  - Targets Linux, Mac, Windows, iOS, Android, and Raspberry Pi platforms.
  - Well known in the industry, and many commercial plugins are built with it.

## [`Tracktion Engine`]
  - Full-stack framework in C++ with GUI. It is built on top of [`JUCE`].
  - Same licensing as [`JUCE`] since it's built on top of it.
  - Targeted formats and platforms are the same as [`JUCE`].
  - Made and used by the commercial company Tracktion.

## [`iPlug2`]
  - Full-stack framework in C++ with GUI.
  - Fully open-source using a permissive license.
  - Targets VST2, VST3, AUv2, AUv3, AAX and the Web Audio Module (WAM) plugin formats (also support for CLAP is in the works).
  - Targets Mac, Windows, iOS, and Web. It does not target Linux, so I'm personally not a fan of this one.

[`Steinberg's VST3 License`]: https://developer.steinberg.help/display/VST/VST+3+Licensing

[`Rust`]: https://www.rust-lang.org/
[`CLAP`]: https://github.com/free-audio/clap

[`DISTRHO Plugin Framework`]: https://github.com/DISTRHO/DPF
[`Dplug`]: https://github.com/AuburnSounds/Dplug
[`JUCE`]: https://github.com/juce-framework/JUCE
[`Tracktion Engine`]: https://github.com/Tracktion/tracktion_engine/
[`iPlug2`]: https://github.com/iPlug2/iPlug2
[`nih-plug`]: https://github.com/robbert-vdh/nih-plug
[`Vizia`]: https://github.com/vizia/vizia
[`Iced`]: https://github.com/iced-rs/iced
[`egui`]: https://github.com/emilk/egui
[`cookiecutter template`]: https://github.com/robbert-vdh/nih-plug-template
