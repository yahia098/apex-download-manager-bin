# Apex Download Manager (Arch Linux)

An unofficial Arch Linux package for [Apex Download Manager](https://github.com/ThembaTman0/apex-download-manager).

This repository packages the official upstream Debian build for Arch Linux. It does not compile, patch, or modify the application. It simply extracts the upstream `.deb` and packages its contents for installation through pacman.

## Installation

### Requirements

- Arch Linux or an Arch-based distribution
- x86_64 architecture
- `base-devel`
- `git`

### Install

```bash
sudo pacman -S --needed base-devel git

git clone https://github.com/yahia098/apex-download-manager-bin.git
cd apex-download-manager-bin

makepkg -si
```

`makepkg` handles the package dependencies and installs the resulting package.

After installation, Apex can be launched from your desktop's application menu.

## Dependencies

**Runtime dependencies**

- `gtk3`
- `webkit2gtk-4.1`
- `libayatana-appindicator`

**Build dependency**

- `dpkg` — used to extract the upstream Debian package. It is not required to run Apex.

**Optional features**

- `yt-dlp` — video downloading.
- `ffmpeg` — merging video and audio streams.

## Updating

When an updated PKGBUILD is published:

```bash
cd apex-download-manager-bin
git pull
makepkg -si
```

Package updates are maintained through this repository and pacman.

## Uninstallation

```bash
sudo pacman -Rns apex-download-manager-bin
```

## Packaging

The PKGBUILD:

1. Downloads the official upstream Debian package.
2. Verifies the downloaded file using SHA-256.
3. Extracts the Debian package using `dpkg-deb`.
4. Produces a native Arch Linux package.

No source compilation or additional application modifications are performed.

## Upstream

- [Apex Download Manager](https://github.com/ThembaTman0/apex-download-manager)
- [Official Website](https://apexdownloadmanager.com/)

This is an unofficial community-maintained Arch Linux packaging repository and is not affiliated with the upstream developer.

## License

Apex Download Manager is distributed under the GNU General Public License v3 or later (GPL-3.0-or-later). See the upstream repository for the license text.
