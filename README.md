<h1 align="center"><i>Bawkpack</i></h1>
<p align="center">Packages list installer that <i>SuperB</i>
<p align="center"><img src="https://img.shields.io/github/license/NNBnh/b.sh?labelColor=073551&color=4EAA25&style=for-the-badge" alt="License: GPL-3.0"> <img src="https://img.shields.io/github/languages/top/NNBnh/b.sh?logo=gnu-bash&labelColor=073551&color=4EAA25&logoColor=FFFFFF&style=for-the-badge" alt="Shell: 100%"> <img src="https://img.shields.io/badge/curl-able-%234EAA25.svg?labelColor=073551&style=for-the-badge&logo=curl&logoColor=FFFFFF" alt="Curlable"> <img src="https://img.shields.io/github/last-commit/NNBnh/b.sh?labelColor=073551&color=4EAA25&style=for-the-badge">
<p align="center"><img src="https://img.shields.io/github/watchers/NNBnh/b.sh?labelColor=073551&color=4EAA25&style=flat-square"> <img src="https://img.shields.io/github/stars/NNBnh/b.sh?labelColor=073551&color=4EAA25&style=flat-square"> <img src="https://img.shields.io/github/forks/NNBnh/b.sh?labelColor=073551&color=4EAA25&style=flat-square"> <img src="https://img.shields.io/github/issues/NNBnh/b.sh?labelColor=073551&color=4EAA25&style=flat-square">

## About
**Bawkpack** is a *SuperB* packages list installer using [`awk`](https://www.gnu.org/software/gawk/manual/gawk.html) and written in [`pure sh`](https://github.com/dylanaraps/pure-sh-bible).

### Features
- Super **minimum** with exactly [**128** lines of `sh`](bawkpack#L128).
- Super **low** [dependencies](#dependencies)

## Contents
- [About](#about)
  - [Features](#features)
- [Contents](#contents)
- [Setup](#setup)
  - [Dependencies](#dependencies)
    - [Supported Operating System](#supported-operating-system)
    - [To `curl` Bawkpack](#to-curl-bawkpack)
    - [Installation process](#installation-process)
  - [Packages list](#packages-list)
- [Usage](#usage)

## Setup
### Dependencies
#### Supported Operating System
\#TODO

#### To `curl` Bawkpack
- `curl` or `wget` to use [`bawkpack`](https://github.com/NNBnh/bawkpack)

#### Installation process
- `sh` to process
- `awk` to read packages file

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
First export some values:

```sh
export BAWKPACK_FILE=path/to/packageslist
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
./bawkpack path/to/packageslist
```
