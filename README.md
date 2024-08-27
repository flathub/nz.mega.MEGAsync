# nz.mega.MEGAsync
MEGAsync Desktop App packaged as flatpak.

## Installation

### Method 1: Install via FlatHub

```
flatpak install nz.mega.MEGAsync
```

### Method 2: Install using this repository

```
git clone https://github.com/flathub/nz.mega.MEGAsync.git
cd nz.mega.MEGAsync
flatpak-builder --install --user --keep-build-dirs build nz.mega.MEGAsync.yml
```

# Launch the desktop app

```
flatpak run nz.mega.MEGAsync
```
