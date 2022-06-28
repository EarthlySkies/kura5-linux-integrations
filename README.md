# Kura5 Linux Integrations

A repository for easy access to the extra Linux files that will be provided in the next release of [Kura5](https://chickenhat.itch.io/kura5-bonds-of-the-undying) on [2022-7-29](https://twitter.com/Boktai3D/status/1529130921097670656)

Feel free to download and utilize everything here, but please note that the scripts might not work with the current public release due to the difference in save file locations. Contributions, improvements and bug reports are welcome.


## Contained files
- **A desktop entry**: allows Kura5 to show up in your applications list
- **An icon for the desktop entry**: makes the desktop entry easy to identify
- **A manual page**: describes the game and lists available command line flags
- **An install script**: allows the user to integrate Kura5 into their desktop environment
- **A shell script launcher**: provides extended logging and tries to determine the best renderer

#### Under construction
- **An AppArmor profile**: for sandboxing support (mostly works, but breaks controller support and certain window decorations)

## Expected directory structure

```
Extracted Kura5 tarball
|   install
|   kura5-launcher
|   Kura5.x86_64
|   README_EN.txt
|   README_JPN.txt
|   tinycaw.png
|
└---Integrations
|   |   global-install
|   |   global-uninstall
|   |   kura5-apparmor-additions
|   |   kura5-apparmor-profile
|   |   kura5-desktop-entry
|   |   kura5-desktop-icon
|   |   kura5-manual-page
|   |   local-install
|   |   local-uninstall
|
└---Kura5_Data
    |   ...
```


## Dependencies
Most, if not all, required tools should be provided by the GNU Coreutils package of 
your distribution (or its dependencies).
If not, here is the list of the tools that the scripts use:
- bash
- chmod
- cp
- echo
- find
- install
- ln
- ls
- mkdir
- mv
- rm
- rmdir
- sed
- tput
