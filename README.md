<h1 align="center"><i>Bawkpack</i></h1>
<p align="center">Packages list installer that <i>SuperB</i></p>
<p align="center"><img src="https://img.shields.io/github/license/NNBnh/b.sh?labelColor=073551&color=4EAA25&style=for-the-badge" alt="License: GPL-3.0"> <img src="https://img.shields.io/github/languages/top/NNBnh/b.sh?logo=gnu-bash&labelColor=073551&color=4EAA25&logoColor=FFFFFF&style=for-the-badge" alt="Shell: 100%"> <img src="https://img.shields.io/badge/curl-able-%234EAA25.svg?labelColor=073551&style=for-the-badge&logo=curl&logoColor=FFFFFF" alt="Curlable"> <img src="https://img.shields.io/github/last-commit/NNBnh/b.sh?labelColor=073551&color=4EAA25&style=for-the-badge"></p>
<p align="center"><img src="https://img.shields.io/github/watchers/NNBnh/b.sh?labelColor=073551&color=4EAA25&style=flat-square"> <img src="https://img.shields.io/github/stars/NNBnh/b.sh?labelColor=073551&color=4EAA25&style=flat-square"> <img src="https://img.shields.io/github/forks/NNBnh/b.sh?labelColor=073551&color=4EAA25&style=flat-square"> <img src="https://img.shields.io/github/issues/NNBnh/b.sh?labelColor=073551&color=4EAA25&style=flat-square"></p>

## About
**Bawkpack** is a *SuperB* packages list installer ~~using [`awk`](https://www.gnu.org/software/gawk/manual/gawk.html) and~~ written in [`pure sh`](https://github.com/dylanaraps/pure-sh-bible). **Bawkpack** is exactly [**128** lines of `sh`](bawkpack#L128) with [**no dependencies**](#dependencies) (if you don't count `sh`).

### Purpose

This project is just a proof of concept. My desire is for a "One for all" package manager, a package manager wrapper that works on any distro that finds and matches an exact package between the package manager.

Example:

```sh
bpack install godot
```

|Package manager|What it's actually run|
|-|-|
|[APT](https://wiki.debian.org/Apt)|`apt install godot3`|
|[AUR](https://wiki.archlinux.org/index.php/Arch_User_Repository)|`yay -Sy godot-bin`|
|[XBPS](https://docs.voidlinux.org/xbps/index.html)|`xbps-install --sync godot`|

###### Hope someone make this dream come true

## Contents
- [About](#about)
  - [Purpose](#purpose)
- [Contents](#contents)
- [Setup](#setup)
  - [Dependencies](#dependencies)
    - [Supported Operating System](#supported-operating-system)
    - [To `curl` Bawkpack](#to-curl-bawkpack)
    - [Installation process](#installation-process)
  - [Packages list](#Packages-list)
- [Usage](#usage)

## Setup
### Dependencies
#### Supported package managers
- [APT](https://wiki.debian.org/Apt)
- [Pacman](https://wiki.archlinux.org/index.php/Pacman)
- [XBPS](https://docs.voidlinux.org/xbps/index.html)


- [AUR](https://wiki.archlinux.org/index.php/Arch_User_Repository)
- [Flatpak](https://flatpak.org)
- [Snap](https://snapcraft.io)

#### To `curl` Bawkpack
- `curl` or `wget` to use [`bawkpack`](https://github.com/NNBnh/bawkpack)

#### Installation process
- `sh` to process
- ~~`awk` to read packages file~~ Bawkpack doesn't need `awk` anymore...

### Packages list
Lets take a look at a `packageslist` file example:

```
### Lable (use "#" to comments)
  APT:kakoune                  PAC:kakoune                  XBP:kakoune                # Comments...
  FLA:org.godotengine.Godot    AUR:godot-bin                XBP:godot                  # Comments...
  SNA:blender                                                                          # Use Snapcraft package on every distro
# SNA:retroarch                PAC:retroarch                XBP:retroarch              # Comment out a package
```

## Usage
First `curl` Bawkpack:

```sh
curl -fsSL https://raw.githubusercontent.com/NNBnh/bawkpack/master/bawkpack | sh
```

If you want to use `wget`:

```sh
wget -qO - https://raw.githubusercontent.com/NNBnh/bawkpack/master/bawkpack | sh
```

Bawkpack can also be use locally:

```sh
chmod +x bawkpack
./bawkpack path/to/packageslist
```

> <h1 align="center">Made with ❤️ by <a href="https://github.com/NNBnh"><i>NNB</i></a></h1>
>
> <p align="center"><a href="https://www.buymeacoffee.com/nnbnh"><img src="https://img.shields.io/badge/buy_me_a_coffee%20-%23F7CA88.svg?logo=buy-me-a-coffee&logoColor=333333&style=for-the-badge" alt="Buy Me a Coffee"></p>
