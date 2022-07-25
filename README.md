# Kura5 Linux Integrations

A repository for easy access to the extra Linux files provided with [Kura5: Bonds of the Undying](https://chickenhat.itch.io/kura5-bonds-of-the-undying)

## Contained files
- **A desktop entry**: allows Kura5 to show up in your applications list
- **An icon for the desktop entry**: makes the desktop entry easy to identify
- **A manual page**: describes the game and lists available command line flags
- **An install script**: allows the user to integrate Kura5 into their desktop environment
- **A shell script launcher**: provides extended logging and tries to determine the best renderer
- **An AppArmor profile**: for sandboxing support (breaks certain window decorations)

## Installation
### The itch.io version (supported way)
- Download the latest release of Kura5 from itch.io
- Extract the archive
- (Make the install script executable)
- Run the install script and follow the instructions

### A custom Kura5 version (unsupported)
- Verify that all file names are unmodified
- Create a directory named "Integrations" in the same directory as the Kura5.x86_64 executable
- Copy the contents of "src" to "Integrations"
- Move "kura5-launcher" and "install" to the same directory as the Kura5.x86_64 executable
- (Make the install script executable)
- Launch the install script and follow instructions

#### Support for older versions of Kura5
Please note that all components are only built to support the lastest official release of Kura5.
No support will be provided for older versions, even if problems arise.

The launcher will probably work without issue for older version, but the log files will most likely
be in separate locations (untested)

The local install will probably also work (untested)

The global install will probably break the game, even if done successfully (untested)

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
These are the tools the scripts utilize and depend upon.
All of them should be installed on every Linux system based on the GNU Coreutils,
either as a part of them or as a dependency. Please note that the package names might be
different on your distribution of choise.

### Hard dependencies
- bash
- coreutils
- ncurses
- sed

### Optional dependencies
- vulkan-tools: for trying to determine if Vulkan can be used for rendering
- apparmor: for sandboxing support when running a globally installed instance
