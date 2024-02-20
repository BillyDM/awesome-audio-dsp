# Plugin Development Frameworks
A list of software stacks/frameworks used to make audio plugins with/without GUIs, along with their pros and cons.

> #### A common question that gets asked is "How can I use *X* GUI library to make my plugin GUI?
>
> Unfortunately, a big blocker that prevents most of the popular GUI libraries from working in a plugin context is that most are designed with the assumption that they own the event loop. But in a plugin context, it's the host that owns the event loop, not the plugin. So unless the GUI library was designed from the get-go to handle this use case, it's difficult to add it after the fact.
>
> Only the [CLAP] plugin format went out of its way to allow plugins to own their own event loop. Even then, it's still discouraged since it prevents the host from seamlessly integrating with the plugin window (i.e. FL Studio drawing a window border around the plugin window with extra useful controls at the top of the window). Also, you have to be careful about dynamically linking to a GUI library (as described [here](https://github.com/free-audio/clap-plugins)).

## [JUCE](https://github.com/juce-framework/JUCE)
  - Full-stack framework with GUI in C++.
  - Open source with mixed licensing. It's free if you distribute your plugins open-source under the GPLv3 license, but you have to pay for a hefty license if you want to distribute your plugins closed-source.
  - Targets VST2, VST3, AUv2, AUv3, RTAS, AAX, and LV2 plugin formats. Unofficial support for the [CLAP] standard is also in the works [here](https://github.com/free-audio/clap-juce-extensions).
  - Targets Linux, Mac, Windows, iOS, Android, and Raspberry Pi platforms.
  - Well known in the industry, and many commercial plugins are built with it.

### JUCE Resources
  - [Pamplejuce](https://github.com/sudara/pamplejuce) - Handy code template to help get you started.
  - [Cookiejuce](https://github.com/madskjeldgaard/Cookiejuce) - Another good template generator. It's a hard fork of Pamplejuce with a lot of opinionated stuff added/changed.
  - [JIVE](https://github.com/ImJimmi/JIVE) - Framework that makes it easier to create GUIs in JUCE.
  - [Awesome JUCE](https://github.com/sudara/awesome-juce) - A large list of resources for JUCE.

## [NIH-plug](https://github.com/robbert-vdh/nih-plug)
  - Full-stack and modular framework with GUI in Rust.
  - Fully open-source using a permissive license.
  - Targets [CLAP] and VST3 plugin formats.
  - Targets Linux, Mac, and Windows platforms.
  - Has several different options for GUI such as [Vizia](https://github.com/vizia/vizia), [Iced](https://github.com/iced-rs/iced), and [egui](https://github.com/emilk/egui).
  - It's still somewhat experimental and is missing some more specialized features, but it's usable.
  - There is now a [cookiecutter template](https://github.com/robbert-vdh/nih-plug-template) to help get you started faster.

## [DISTRHO Plugin Framework](https://github.com/DISTRHO/DPF)
  - Full-stack framework with GUI in C++.
  - Fully open-source using a permissive license.
  - Targets LADSPA, DSSI, LV2, VST2, VST3, CLAP, and Jack plugin formats.
  - Targets Linux, Mac, and Windows platforms.

## [Dplug](https://github.com/AuburnSounds/Dplug)
  - Full-stack framework with GUI in the D programming language.
  - Fully open-source using a permissive license.
  - The GUI framework has fancy physically-modeled rendering inspired by game engines.
  - Targets VST2, VST3, AUv2, AAX, and LV2 plugin formats.
  - Targets Linux, Mac, Windows, and Raspberry Pi platforms.
  - Used by several commercial plugins.

## [iPlug2](https://github.com/iPlug2/iPlug2)
  - Full-stack framework in C++ with GUI.
  - Fully open-source using a permissive license.
  - Targets VST2, VST3, AUv2, AUv3, AAX and the Web Audio Module (WAM) plugin formats (also support for [CLAP] is in the works).
  - Targets Mac, Windows, iOS, and Web. It does not currently target Linux.

[CLAP]: https://github.com/free-audio/clap
