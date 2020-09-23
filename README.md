<h1 align="center"><i>Bawkpack</i></h1>
<p align="center">Packages list installer that <i>SuperB</i>
<p align="center"><img src="https://img.shields.io/github/license/NNBnh/b.sh?labelColor=073551&color=4EAA25&style=for-the-badge" alt="License: GPL-3.0"> <img src="https://img.shields.io/github/languages/top/NNBnh/b.sh?logo=gnu-bash&labelColor=073551&color=4EAA25&logoColor=FFFFFF&style=for-the-badge" alt="Shell: 100%"> <img src="https://img.shields.io/badge/curl-able-%234EAA25.svg?labelColor=073551&style=for-the-badge&logo=curl&logoColor=FFFFFF" alt="Curlable"> <img src="https://img.shields.io/github/last-commit/NNBnh/b.sh?labelColor=073551&color=4EAA25&style=for-the-badge">
<p align="center"><img src="https://img.shields.io/github/watchers/NNBnh/b.sh?labelColor=073551&color=4EAA25&style=flat-square"> <img src="https://img.shields.io/github/stars/NNBnh/b.sh?labelColor=073551&color=4EAA25&style=flat-square"> <img src="https://img.shields.io/github/forks/NNBnh/b.sh?labelColor=073551&color=4EAA25&style=flat-square"> <img src="https://img.shields.io/github/issues/NNBnh/b.sh?labelColor=073551&color=4EAA25&style=flat-square">

## About
**Bawkpack** is a *SuperB* packages list installer using [`awk`](https://www.gnu.org/software/gawk/manual/gawk.html) and written in [`pure sh`](https://github.com/dylanaraps/pure-sh-bible).

### Features
- Super **minimum** with exactly [**64** lines of `sh`](bawkpack#L64).
- Super **low** [dependencies](#dependencies)

## Contents
- [About](#about)
  - [Features](#features)
- [Contents](#contents)
- [Setup](#setup)
  - [Dependencies](#dependencies)
    - [To `curl` Bawkpack](#to-curl-bawkpack)
    - [Installation process](#installation-process)
  - [Packages list](#Packages-list)
- [Usage](#usage)

## Setup
### Dependencies
#### To `curl` Bawkpack
- `curl` or `wget` to use [`bawkpack`](https://github.com/NNBnh/bawkpack)

#### Installation process
- `sh` to process
- `awk` to read packages file

### Packages list

Create a `packageslist` file:

```
### Lable (use '#' to comments)
  APT:kakoune                  PAC:kakoune                  XBP:kakoune                # Comments...
  FLA:org.godotengine.Godot    AUR:godot-bin                XBP:godot                  # Comments...
  SNA:blender                                                                          # Use Snapcraft package on every distro
# SNA:retroarch                PAC:retroarch                XBP:retroarch              # Comment out a package
```

## Usage
First export some values:

```sh
export BAWKPACK_FILE=path/to/packageslist
export BAWKPACK_MAINPM=[Pacman|APT|XBPS] # Choose your main packages manager
```

###### This is unnecessary if you download and use Bawkpack locally.

Then `curl` Bawkpack:

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
./bawkpack path/to/packageslist [Pacman|APT|XBPS]
```
