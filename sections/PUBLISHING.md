# Publishing

Resources related to the publishing and distrubution of audio plugins.

## Continuous Integration (CI)

### GitHub Action examples

* [Chowdhury-DSP JUCE Template](https://github.com/Chowdhury-DSP/JUCEPluginTemplate/blob/main/.github/workflows/cmake.yml)
* [NIH-plug](https://github.com/robbert-vdh/nih-plug/blob/master/.github/workflows/build.yml) (outdated)
* [Pamplejuce](https://github.com/sudara/pamplejuce/blob/main/.github/workflows/build_and_test.yml)
* [SurgeXT](https://github.com/surge-synthesizer/surge/blob/main/.github/workflows/build-release.yml)

## Compiling for Linux

A common problem with distributing plugins for Linux is that plugins compiled with newer versions of libraries (including [libc](https://www.gnu.org/software/libc/)) will not run on hosts/distributions which use older versions of those libraries. (This problem can also occur when running plugins in a DAW bundled as a [flatpak](https://flatpak.org/)). A common solution is to target an older version of Linux, commonly Ubuntu 22.04 (Jammy Jeyllyfish).

If you use CI to build your plugins, then simply set the target to Ubuntu 22.04. But if you want to build the plugins on your own machine, there are a few options:

* [Distrobox](https://distrobox.it/)
* [Docker](https://www.docker.com/products/docker-desktop/)
* [Nix Flakes](https://nixos.wiki/wiki/flakes)
* [podman](https://podman.io/)
* [Toolbx](https://docs.fedoraproject.org/en-US/atomic-desktops/toolbox/) - An easy-to-use container-based development tool built on top of podman. Create an Ubuntu 22.04 container with `toolbox create --distro ubuntu-22.04`.

## Bundling

* [cargo-nice-plug](https://codeberg.org/RustAudio/nice-plug/src/branch/main/crates/cargo-nice-plug) - A cargo command to bundle audio plugins in the Rust programming language. While it's made for the [nice-plug](https://codeberg.org/RustAudio/nice-plug) development framework, it can also be used on its own to bundle Rust plugins made with other frameworks such as [clack-plugin](https://github.com/prokopyl/clack).

## Cross Compilation

* [cross-rs](https://github.com/cross-rs/cross) - An easy-to-use tool to cross-compile and even cross-test Rust projects. Only supports GNU targets (so no MacOS or Windows with the MSVC toolchain, but Windows with the GNU toolchain is supported).
