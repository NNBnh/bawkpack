> ## *Bawkpack* is hosted on [*SuperB Bootstrap*](https://github.com/NNBnh/superb-bootstrap), this repository is now a documents only.

<h1 align="center"><i>Bawkpack</i></h1>
<p align="center">Packages list installer that <i>SuperB</i></p>
<p align="center"><img src="https://img.shields.io/github/license/NNBnh/bawkpack?labelColor=073551&color=4EAA25&style=for-the-badge" alt="License: GPL-3.0"> <img src="https://img.shields.io/github/languages/top/NNBnh/bawkpack?logo=gnu-bash&labelColor=073551&color=4EAA25&logoColor=FFFFFF&style=for-the-badge" alt="Shell: 100%"></p>
<p align="center"><img src="https://img.shields.io/github/watchers/NNBnh/bawkpack?labelColor=073551&color=4EAA25&style=flat-square"> <img src="https://img.shields.io/github/stars/NNBnh/bawkpack?labelColor=073551&color=4EAA25&style=flat-square"> <img src="https://img.shields.io/github/forks/NNBnh/bawkpack?labelColor=073551&color=4EAA25&style=flat-square"> <img src="https://img.shields.io/github/issues/NNBnh/bawkpack?labelColor=073551&color=4EAA25&style=flat-square"></p>

## About
**Bawkpack** is a *SuperB* packages list installer ~~using [`awk`](https://www.gnu.org/software/gawk/manual/gawk.html) and~~ written in [`pure sh`](https://github.com/dylanaraps/pure-sh-bible). **Bawkpack** is exactly [**128** lines of `sh`](https://github.com/NNBnh/superb-bootstrap/blob/master/extra/bawkpack#L128) with [**no dependencies**](#dependencies) (if you don't count `sh`).

### Purpose
This project is just a proof of concept. My desire is for a "One for all" package manager, a package manager wrapper that works on any distro that finds and matches an exact package between the package manager.

[Learn more here](https://github.com/NNBnh/dots/wiki/todo#backpack)

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
First set `path/to/packageslist`:

```sh
export BAWKPACK_LIST=path/to/packageslist
```

then `curl` Bawkpack:

```sh
curl -fsSL https://raw.githubusercontent.com/NNBnh/superb-bootstrap/master/extra/bawkpack | sh
```

if you want to use `wget`:

```sh
wget -qO - https://raw.githubusercontent.com/NNBnh/superb-bootstrap/master/extra/bawkpack | sh
```

this will run `bawkpack` with `path/to/packageslist`.

Bawkpack can also be use locally:

```sh
chmod +x bawkpack
./bawkpack path/to/packageslist
```

<br><br><br><br>

---

> <h1 align="center">Made with :heart: by <a href="https://github.com/NNBnh"><i>NNB</i></a></h1>
>
> <p align="center"><a href="https://www.buymeacoffee.com/nnbnh"><img src="https://img.shields.io/badge/buy_me_a_coffee%20-%23F7CA88.svg?logo=buy-me-a-coffee&logoColor=333333&style=for-the-badge" alt="Buy Me a Coffee"></p>
