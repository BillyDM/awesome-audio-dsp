# Plugin APIs
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
  - Special note - Steinberg is making it difficult to legally create bindings to the VST3 SDK so it can be used with other programming languages (the SDK is in C++). As a Rust developer myself, this has been a big pain in the backside. There have been proposed lawsuits that aim to prevent companies from doing this, but who knows what the future will hold? (By now you can probably see why a lot of the audio industry has an issue with Steinberg).
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
  - Distribution - You can distribute open source and close sourced versions of your plugins (and host LV2 plugins) freely without restriction.
  - SDK source: [`LV2 SDK`]
  - [`sjaehn's LV2 Tutorial`] - A nice tutorial on developing LV2 plugins.

### LADSPA
LADSPA is the precursor to LV2.
  - Why?: It is dead simple to work with.
  - Why Not?: Lack of support in most major commercial DAWs. Also, LADSPA only supports GUI-less plugins.
  - License: [`LGPLv2.1`]/[`LGPLv3`]
  - Platforms: Same as LV2 above
  - Support: Same as LV2 above
  - Distribution: Same as LV2 above
  - SDK source: [`LADSPA Header File`]

### CLAP
  - Why?: A brand new fully open-source plugin standard with no licensing restrictions. It was started by an employee of the Bitwig DAW and has since gotten development support from several key players in the audio industry. It is built from the ground up by people with real-world experience developing audio software, and such it is designed to fit the needs of actual developers as much as possible. It is written in a stable header-only C API, making it easy to create bindings to it in any programming language.
  - Why Not?: The standard is very young (or at-least the latest incarnation of it is young). So young that no DAW actually supports it yet aside from maybe some unrealeased development builds. Also, the spec is still a work in progress and is subject to change before the final release. The reason I am talking about it here is because I am hopeful this will become the plugin standard of the future. It's an exciting time to be an audio developer! Please join the discussions in the issues tab of the [`CLAP SDK`] repository if you are interested!
  - Why not just improve LV2? The developers of CLAP have had many issues with the core design decisions of LV2 (which I won't get into here), and the maintainers of LV2 were not open to changing it. These flawed design decisions are in my opinion a big reason why LV2 has not had any real adoption outside of Linux and open-source DAWs.
  - License: [`MIT`]
  - Platforms: Linux, Mac, Windows (and possibly Android and iOS at some point?)
  - Support: Not supported by any DAW yet aside from maybe some unreleased development builds.
  - Distribution - You can distribute open source and close sourced versions of your plugins (and host CLAP plugins) freely without restriction.
  - SDK source: [`CLAP SDK`] (also includes links to examples)

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
  - [`VCV Rack Plugin Tutorial`] - The official tutorial on making VCV Rack plugins.

[`Vestige Header File`]: https://github.com/x42/lv2vst/blob/master/include/vestige.h

[`VST3 License Agreement`]: https://developer.steinberg.help/pages/viewpage.action?pageId=9797944
[`VST3 SDK`]: https://github.com/steinbergmedia/vst3sdk
[`Rust`]: https://www.rust-lang.org/

[`AU SDK`]: https://github.com/apple/AudioUnitSDK

[`LV2 SDK`]: https://gitlab.com/lv2/lv2
[`sjaehn's LV2 Tutorial`]: https://github.com/sjaehn/lv2tutorial

[`LADSPA Header File`]: https://www.ladspa.org/ladspa_sdk/ladspa.h.txt

[`CLAP SDK`]: https://github.com/free-audio/clap

[`WAP SDK`]: https://github.com/micbuffa/WebAudioPlugins

[`VCV Rack`]: https://vcvrack.com/
[`VCV Rack Licensing`]: https://vcvrack.com/manual/PluginLicensing
[`VCV Rack Plugin SDK`]: https://vcvrack.com/downloads/
[`VCV Rack Plugin Tutorial`]: https://vcvrack.com/manual/PluginDevelopmentTutorial

[`GPLv2`]: https://opensource.org/licenses/gpl-2.0.php
[`GPLv3`]: https://choosealicense.com/licenses/gpl-3.0/
[`MIT`]: https://choosealicense.com/licenses/mit/
[`Apache 2.0`]: https://choosealicense.com/licenses/apache-2.0/
[`LGPLv2.1`]: https://opensource.org/licenses/lgpl-2.1.php
[`LGPLv3`]: https://choosealicense.com/licenses/lgpl-3.0/