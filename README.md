# Arch PACMAN

This repositories has some basic command for Arch Linux package manager - pacman.

## Update && Upgrade

```bash
sudo pacman -Syu
```

## Install Package

```bash
sudo pacman -S bat
```

## Uninstall Package

```bash
# To remove a package and its dependencies which are not required by any other installed package:
sudo pacman -Rs bat
# Remove including backup file
sudo pacman -Rsn bat
```

## Search for Package

```bash
sudo pacman -Ss neovim
# Search for installed package
```

