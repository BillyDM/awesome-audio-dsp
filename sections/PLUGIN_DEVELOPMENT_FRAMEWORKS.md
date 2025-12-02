# Plugin Development Frameworks

A list of software stacks/frameworks used to make audio plugins with/without GUIs, along with their pros and cons.

## [DISTRHO Plugin Framework](https://github.com/DISTRHO/DPF)
  - Full-stack framework with GUI in C++.
  - Fully open-source using a permissive license.
  - Targets LADSPA, DSSI, LV2, VST2, VST3, CLAP, and Jack plugin formats.
  - Targets Linux, Mac, and Windows platforms.
  - [cookiecutter-dpf-effect](https://github.com/SpotlightKid/cookiecutter-dpf-effect) - A [cookiecutter] template to help get you started.
  - [DISTRHO Dear Plugins](https://github.com/DISTRHO/dear-plugins) - A collection of plugins demonstrating how to use the Dear ImGui library with the DPF framework. Still a work in progress.

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

## [JUCE](https://github.com/juce-framework/JUCE)
  - Full-stack framework with GUI in C++.
  - Open source with mixed licensing. It's free if you distribute your plugins open-source under the GPLv3 license, but you have to pay for a hefty license if you want to distribute your plugins closed-source.
  - Targets VST2, VST3, AUv2, AUv3, RTAS, AAX, and LV2 plugin formats. Unofficial support for the [CLAP] standard is also in the works [here](https://github.com/free-audio/clap-juce-extensions).
  - Targets Linux, Mac, Windows, iOS, Android, and Raspberry Pi platforms.
  - Well known in the industry, and many commercial plugins are built with it.

### JUCE Resources
  - [Awesome JUCE](https://github.com/sudara/awesome-juce) - A large list of resources for JUCE.
  - [Chowdhury's JUCE template](https://github.com/Chowdhury-DSP/JUCEPluginTemplate) - A good template with some extra useful utilities.
  - [Cookiejuce](https://github.com/madskjeldgaard/Cookiejuce) - Another good template generator. It's a hard fork of Pamplejuce with a lot of opinionated stuff added/changed.
  - [JIVE](https://github.com/ImJimmi/JIVE) - Framework that makes it easier to create GUIs in JUCE.
  - [Pamplejuce](https://github.com/sudara/pamplejuce) - Handy code template to help get you started.

## [NIH-plug](https://github.com/robbert-vdh/nih-plug)
  - Full-stack and modular framework with GUI in Rust.
  - Fully open-source using a permissive license.
  - Targets [CLAP] and VST3 plugin formats.
  - Targets Linux, Mac, and Windows platforms.
  - Has several different options for GUI such as [Vizia], [Iced], [egui], and [Slint]. (Slint requires a paid license if you want to distribute your plugin closed-source.)
    - If you use Iced, there are also audio-specific widgets in the [iced_audio] extension.
    - The `egui` adapter in the nih-plug repository is outdated. Use [this 3rd party egui adapter](https://codeberg.org/BillyDM/egui-baseview) instead.
  - It's still somewhat experimental and is missing some more specialized features, but it's usable.
  - There is now a [cookiecutter template](https://github.com/robbert-vdh/nih-plug-template) to help get you started faster.

# New Experimental Frameworks

There have been a few shiny new plugin development frameworks popping up over the past few years. While these are still experimental and may not have the same level of features and support of the established ones, give them a try if you're interested in shiny new things!

## [Arbor](https://github.com/ArborealAudio/arbor)
  - A "dead-simple" plugin development framework written in the [Zig](https://ziglang.org/) programming language. It also provides a simple C API that makes it easy to provide bindings to other languages.
  - Fully open-source using a permissive license.
  - Currently a work in progress.

## [Coupler](https://github.com/coupler-rs/coupler)
  - An opinionated framework for writing audio plugins in Rust.
  - Fully open-source using a permissive license.
  - Targets [CLAP] and VST3. Audio Unit and AAX support are on the roadmap.
  - Targets Mac, Windows, and Linux.
  - Still early in development and not production-ready yet.

## [CPLUG](https://github.com/Tremus/CPLUG)
  - A simple wrapper for the VST3, Audio Unit v2 & [CLAP] plugin formats.
  - Uses a simple C API that makes it easy to provide bindings to other languages.
  - Only provides the plumbing and doesn't provide a GUI out of the box. You can add your own GUI layer of choice on top. (See the `Bring Your Own OpenGL Context` section below.)
  - Fully open-source using a permissive license (including a public domain license).
  - Very new and experimental. It is missing a few features at the time of this writing.
  - Targets Mac and Windows. It does not currently target Linux, but it is (maybe) on the roadmap.

## [Mostly Harmless](https://github.com/SLM-Audio/mostly-harmless)
  - A minimal audio plugin framework for C++20.
  - Fully open-source using a permissive license.
  - Allows the user to choose their own GUI framework, and includes official support for using [choc](https://github.com/Tracktion/choc)'s WebView to create GUIs.
  - Targets [CLAP], VST3, Audio Unit, and standalone.
  - Targets Mac and Windows. It does not currently support Linux, but it is on the roadmap.

## [Visage]
  - A GPU-accelerated, cross-platform C++ library for native UI and 2D graphics. It merges the structure of a UI framework with the features of a creative graphics libraries. It is made by the developer of the [Vital] synthesizer.
  - Fully open-source using a permissive license.
  - While it is more of a GUI library than a plugin development framework, it natively supports both the [CLAP] plugin API and the [clap-wrapper] library to automatically generate CLAP, VST3, AU, and standalone versions of your plugin for you. For a great example of this setup in action, see the [Spectrum](https://github.com/tadmn/spectrum) plugin.
  - Targets [CLAP], VST3, Audio Unit, and standalone.
  - Targets Linux, Mac, and Windows platforms.

# The DIY Route

Are you hardcore and have a lot of time on your hands? Well then do I have the solution for you!

Jokes aside, this is a legitimate route you can take. Just be prepared for the extra boilerplate work involved, especially if you want to have cross-platform and/or cross-API support. You can get quite far by using one of the GUI libraries listed below. (Though I advise against creating your own GUI library unless you do actually have a lot of time on your hands.) It can also be a fun and valuable experience learning how plugin APIs actually work under the hood.

Here are some resources that can make your life easier:

## Windowing

* [CHOC] (C++) - A random grab-bag of header-only, dependency-free, liberally-licensed C++ classes. It is very handy if you want to use or create a custom GUI library in C++, and it even includes support for [WebView](https://github.com/Tracktion/choc/blob/main/gui/choc_WebView.h).
* [baseview] (Rust) - A low-level windowing system geared towards making audio plugin UIs.

## The CLAP wrapper

A new trend in the audio plugin development world is to just write your plugin against the raw [CLAP] plugin API with whatever GUI library (perhaps using [CHOC] or [baseview] for cross-platform windowing), and then let the [clap-wrapper] library automatically generate VST3, AU, and standalone versions of your plugin for you. For a great example of this setup in action, see the [Spectrum](https://github.com/tadmn/spectrum) plugin.

## Plugin-Compatible GUI Libraries

Here is a list of compatible GUI libraries you can use for your audio plugins.

* [Dear ImGui](https://github.com/ocornut/imgui) - A very popular immediate mode GUI library with an active community. There are bindings to many other languages available.
  * [clap-imgui](https://github.com/schwaaa/clap-imgui) - A minimal example of a CLAP plugin with ImGui.
* [egui] - An ImGui-inspired immediate mode GUI library for Rust.
    - [egui_baseview](https://github.com/BillyDM/egui-baseview) - A shim to run egui on top of [baseview].
* [Iced] - A cross-platform GUI library for Rust focused on simplicity and type-safety.
    - [iced_audio] - Iced widgets for audio applications.
    - [iced_baseview](https://github.com/BillyDM/iced_baseview) - A shim to run Iced on top of [baseview].
* [Nuklear](https://github.com/Immediate-Mode-UI/Nuklear) - Another popular immediate mode GUI library. Written in pure C, and bindings to many other languages are available.
* [Pugl](https://github.com/lv2/pugl) - Minimal GUI layer made specifically for plugins.
* [Qt](https://www.qt.io/) - It's possible to use Qt for CLAP plugins (though I'm not sure about other plugin formats).
  * [Example Clap Plugins](https://github.com/free-audio/clap-plugins/tree/main) - The offical example CLAP plugins use Qt for their GUI.
* [raygui](https://github.com/raysan5/raygui) - Another lightweight immediate mode GUI library written in pure C.
* [rutabaga](https://github.com/wrl/rutabaga) - An experimental OpenGL widget toolkit written in C.
* [robtk](https://github.com/x42/robtk) - A minimal layer for creating GUIs for LV2 plugins.
* [Slint] - Robust and feature-packed declarative GUI library with bindings for Rust and C++. It's free to use for open source projects, but it requires a paid license to use for closed-source projects.
* [Visage] - A a GPU-accelerated, cross-platform C++ library for native UI and 2D graphics. It merges the structure of a UI framework with the features of a creative graphics libraries. Made by the developer of the [Vital]() synthesizer.
* [Vizia] - A declarative GUI library for Rust. Comes with a [baseview] backend built-in.

> #### A common question that gets asked is "How can I use *X* GUI library to make my plugin GUI?
>
> Unfortunately, a big blocker that prevents many of the popular GUI libraries from working in a plugin context is that most are designed with the assumption that they own the event loop. But in a plugin context, it's the host that owns the event loop, not the plugin. So unless the GUI library was designed from the get-go to handle this use case, it's difficult to add it after the fact.
>
> Only the [CLAP] plugin format went out of its way to allow plugins to own their own event loop. Even then, it's still discouraged since it prevents the host from seamlessly integrating with the plugin window (i.e. FL Studio drawing a window border around the plugin window with extra useful controls at the top of the window).

## "I am hardcore and want to make my own GUI solution"

There are plenty of options that allow you to just draw shapes and text to the screen.
 
* [bgfx](https://github.com/bkaradzic/bgfx) - Low-level cross platform graphics library that abstracts over different graphics APIs. Has a sizeable community, and contains bindings to various programming languages.
* [Cairo](https://www.cairographics.org/) - An old but widely used vector graphics library. It is not hardware-accelerated though, so it is quite slow. But on the flip side not being hardware-accelerated removes the headaches involved with graphics drivers.
* [femtovg](https://github.com/femtovg/femtovg) - An OpenGL vector graphics rendering library written in Rust, based on NanoVG.
* [Lyon](https://github.com/nical/lyon) - A tessellation library written in Rust. It simply outputs a list of triangles for the GPU to render.
* [NanoVG](https://github.com/inniyah/nanovg) - Vector graphics rendering library for OpenGL.
* [Skia](https://skia.org/) - Hardware-accelerated 2D vector graphics library. Built by Google to power Chrome and Flutter. It has a relatively large binary size though.
* [Sokol](https://github.com/floooh/sokol) - Low-level cross platform graphics library that abstracts over different graphics APIs. Contains bindings to various programming languages.
* [vg-renderer](https://github.com/jdryg/vg-renderer) - A vector graphics renderer for [bgfx].
* [wgpu](https://wgpu.rs/) - Low-level cross platform graphics library for Rust that abstracts over different graphics APIs. Inspired by WebGPU.
  * [glyphon](https://github.com/grovesNL/glyphon) - An easy way to layout and render text in wgpu using [Cosmic Text](https://github.com/pop-os/cosmic-text/).

[CLAP]: https://github.com/free-audio/clap
[clap-wrapper]: https://github.com/free-audio/clap-wrapper
[Vizia]: https://github.com/vizia/vizia
[Iced]: https://github.com/iced-rs/iced
[iced_audio]: https://github.com/iced-rs/iced_audio
[egui]: https://github.com/emilk/egui
[Slint]: https://slint.dev/
[baseview]: https://github.com/RustAudio/baseview
[bgfx]: https://github.com/bkaradzic/bgfx
[Visage]: https://github.com/VitalAudio/visage
[Vital]: https://github.com/mtytel/vital
[cookiecutter]: https://github.com/audreyr/cookiecutter
[CHOC]: https://github.com/Tracktion/choc
[baseview]: https://github.com/RustAudio/baseview
