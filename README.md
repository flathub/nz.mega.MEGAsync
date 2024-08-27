# nz.mega.MEGAsync
MEGAsync Desktop App packaged as flatpak.

## Installation

### Method 1: Install via FlatHub (recommended)

```
flatpak remote-add --if-not-exists flathub https://dl.flathub.org/repo/flathub.flatpakrepo
flatpak install nz.mega.MEGAsync
```

### Method 2: Install using this repository

```
git clone https://github.com/flathub/nz.mega.MEGAsync.git
cd nz.mega.MEGAsync
flatpak-builder --install --user build nz.mega.MEGAsync.yml
```

## Launch the desktop app

```
flatpak run nz.mega.MEGAsync
```

## Uninstall

```
flatpak uninstall nz.mega.MEGAsync
```

## Local flatpak testing

```
git clone https://github.com/flathub/nz.mega.MEGAsync.git
cd nz.mega.MEGAsync
mkdir binary-cache
```

Then edit nz.mega.MEGAsync.yml and uncomment the binary-cache module source at the end of the manifest.

If you already have a vcpkg binary cache, you may copy it to binary-cache folder.

If this is an initial build, run the following command:

```
flatpak-builder --install --user --keep-build-dirs build nz.mega.MEGAsync.yml
```

Once a successful build was done, copy the folder `.flatpak-builder/build/MEGAsync/binary-cache` and paste it in the directory where nz.mega.MEGAsync.yml is. The next build will be faster because the vcpkg dependencies are already compiled and cached.