<div align="center">
  <img src="https://raw.githubusercontent.com/bottlesdevs/Bottles/main/data/icons/hicolor/scalable/apps/com.usebottles.bottles.svg" width="64">
  <h1 align="center">Bottles</h1>
  <p align="center">Run Windows Software on Linux</p>
</div>

<br/>

<div align="center">
  <a href="https://flathub.org/apps/com.usebottles.bottles">
    <img alt="Flathub" src="https://img.shields.io/flathub/downloads/com.usebottles.bottles" />
  </a>
  <a href="https://hosted.weblate.org/engage/bottles">
    <img src="https://hosted.weblate.org/widgets/bottles/-/bottles/svg-badge.svg" />
  </a>
  <a href="https://www.codefactor.io/repository/github/bottlesdevs/bottles/overview/main">
    <img src="https://www.codefactor.io/repository/github/bottlesdevs/bottles/badge/main" />
  </a>
  <a href="https://github.com/bottlesdevs/Bottles/blob/main/LICENSE">
    <img src="https://img.shields.io/badge/License-GPL--3.0-blue.svg">
  </a>
  <br>
  <a href="https://github.com/bottlesdevs/Bottles/actions">
    <img src="https://github.com/bottlesdevs/Bottles/workflows/Build%20release%20packages/badge.svg">
  </a>
  <a href="https://stopthemingmy.app" title="Please do not theme this app">
    <img src="https://stopthemingmy.app/badge.svg">
  </a>

  <hr />

  <a href="https://docs.usebottles.com">Documentation</a> ·
  <a href="https://forum.usebottles.com">Forums</a> · 
  <a href="https://discord.gg/wF4JAdYrTR">Discord</a> · 
  <a href="https://usebottles.com/funding">Funding</a>
</div>

<br/>

![Bottles Dark](docs/screenshot-dark.png#gh-dark-mode-only)![Bottles Light](docs/screenshot-light.png#gh-light-mode-only)

## Installation

<a href='https://flathub.org/apps/com.usebottles.bottles'><img width='240' alt='Download on Flathub' src='https://flathub.org/assets/badges/flathub-badge-en.png'/></a>

## Contributing

Refer to the [Contributing](CONTRIBUTING.md) page.

## Building

⚠️ Be sure to backup all your data before testing experimental builds of Bottles!

There are two methods to build Bottles. The first and longer method is using `org.flatpak.Builder`, and the second but shorter method is building directly.

### org.flatpak.Builder

1. Install [`org.flatpak.Builder`](https://github.com/flathub/org.flatpak.Builder) from Flathub
1. Clone `https://github.com/bottlesdevs/Bottles.git` (or your fork)
1. Run `flatpak run org.flatpak.Builder --install --install-deps-from=flathub --default-branch=master --force-clean build-dir com.usebottles.bottles.yml` in the terminal from the root of the repository (use `--user` if necessary)
1. Run `flatpak run com.usebottles.bottles//master` to launch it

### Meson

Since Bottles is primarily and officially distributed as a Flatpak, we only provide instructions to directly build it inside a Flatpak environment:

1. Download and install the latest build of Bottles: [bottles-x86_64.zip](https://nightly.link/bottlesdevs/Bottles/workflows/build_flatpak/main/bottles-x86_64.zip). Unzip it, and run `flatpak install bottles.flatpak` (use `--user` if necessary)
2. Run `flatpak run -d --filesystem=$PWD --command=bash com.usebottles.bottles//master` from the root of the repository, followed by `./utils/install.sh`. This will build Bottles and install it under the `build/` directory.
3. Run `./build/bin/bottles` to launch Bottles

This build does not follow Gnome and will be removing libadwaita and re-enabling GTK theming. If the oG devs have an issue well its GPL-v3 so suck it.
