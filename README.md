# Kura5 Linux Packaging

This repository aims to contain files that users should find useful in creating packaging for [Kura5](https://chickenhat.itch.io/kura5-bonds-of-the-undying).
It does not contain prebuilt binaries or the game itself, merely the fluff that should come along in a proper package installed 
from the repositories of your preferred distro.

### Contained files
- **A manual page**: describes the game and lists available command line flags
- **A desktop entry**: allows Kura5 to show up in your applications list
- **An icon for the desktop entry**: makes the desktop entry easy to identify
- **A shell script wrapper**: integrates Kura5 into $PATH 

#### Under construction
- **An AppArmor profile**: for sandboxing support
- **PKGBUILD**: automatic package creation for all Arch-based distros
