# Arch PACMAN

This repositories has some basic command for Arch Linux package manager - pacman. 
And also the tool `paru` to install and manage additional packages
from the AUR (Arch User Repository).

## PACMAN

### Update && Upgrade

```bash
sudo pacman -Syu
```

### Install Package

```bash
sudo pacman -S bat
```

### Uninstall Package

```bash
# To remove a package and its dependencies which are not required by any other installed package:
sudo pacman -Rs bat
# Remove including backup file
sudo pacman -Rsn bat
```

### Search for Package

```bash
sudo pacman -Ss neovim
# To search for already installed packages:
sudo pacman -Qs neovim
```

### Reference

- https://wiki.archlinux.org/title/Pacman

## PARU

### Installation

`paru` is a tool written in rust, it is from one of the authors whom had
contributed in writting `yay` which is in go. To install it, you will
 need to compile from source.

```bash
sudo pacman -S --needed base-devel
mkdir $HOME/reference/
cd $HOME/reference/
git clone https://aur.archlinux.org/paru.git
cd paru
makepkg -si
```

### Commands

Command | Description
--- | ---
`paru <target>` | Interactively search and install `<target>`.
`paru` | Alias for `paru -Syu`.
`paru -S <target>` | Install a specific package.
`paru -Sua` | Upgrade AUR packages.
`paru -Qua` | Print available AUR updates.
`paru -G <target>` | Download the PKGBUILD and related files of `<target>`.
`paru -Gp <target>` | Print the PKGBUILD of `<target>`.
`paru -Gc <target>` | Print the AUR comments  of `<target>`.
`paru --gendb` | Generate the devel database for tracking `*-git` packages. This is only needed when you initially start using paru.
`paru -Bi .` | Build and install a PKGBUILD in the current directory.