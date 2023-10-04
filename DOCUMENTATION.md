# Extended Documentation for Installation Script

This document offers a comprehensive explanation of the installation script, describing each section of the script and the purpose of individual commands.

## Table of Contents
- [Introduction](#introduction)
- [Script Structure](#script-structure)
- [Commands and Their Functions](#commands-and-their-functions)
  - [Package List Update](#package-list-update)
  - [Flatpak Installation](#flatpak-installation)
  - [Other Applications](#other-applications)
  - [Application Removal](#application-removal)
  - [GNOME Shell Extensions](#gnome-shell-extensions)
  - [Theme Configuration](#theme-configuration)
  - [Wallpaper Configuration](#wallpaper-configuration)
  - [User Interaction](#user-interaction)
- [Customization](#customization)
- [Contributing](#contributing)
- [Contact](#contact)

## Introduction
The installation script automates the setup of an Ubuntu-based Linux system. It updates packages, installs applications, configures themes, and more. It is designed to streamline the initial setup process and enhance user experience.

**Important Note:** Use this script with caution, as I could only test this on my own three coputers.

## Script Structure
The script is organized into several sections, each responsible for a specific aspect of the installation. Here's an overview of its structure:

1. **Package List Update**: Updates the system's package list and upgrades installed packages.
2. **Flatpak Installation**: Installs applications using the Flatpak package manager.
3. **Other Applications**: Installs additional software and packages.
4. **Application Removal**: Removes specific applications.
5. **GNOME Shell Extensions**: Installs GNOME Shell extensions.
6. **Theme Configuration**: Configures GTK themes, icons, and cursors.
7. **Wallpaper Configuration**: Sets the desktop wallpaper.
8. **User Interaction**: Prompts the user for a system restart.

## Commands and Their Functions

### Package List Update
- `sudo apt update`: Updates the package list to retrieve information about available packages.
- `sudo apt upgrade -y`: Upgrades installed packages without asking for confirmation.

### Flatpak Installation
- `sudo apt install flatpak -y`: Installs the Flatpak package manager.
- `sudo apt install gnome-software-plugin-flatpak -y`: Installs the GNOME Software plugin for Flatpak.
- `sudo flatpak remote-add --if-not-exists flathub https://dl.flathub.org/repo/flathub.flatpakrepo`: Adds the Flathub repository to access Flatpak applications.

### Other Applications
- Commands like `sudo apt install curl -y`, `sudo apt install git -y`, and `sudo apt install gnome-tweaks -y` are used to install various additional applications and tools.

### Application Removal
- Commands like `sudo apt remove firefox -y` are used to remove specific applications such as Firefox.

### GNOME Shell Extensions
- The `gnome-shell-extension-installer` script is used to install GNOME Shell extensions from extensions.gnome.org.
- Extensions are installed using commands like `gnome-shell-extension-installer 307 --yes`.

### Theme Configuration
- Commands like `gsettings set org.gnome.desktop.interface gtk-theme "Yaru-dark"` are used to configure GTK themes.
- The script clones and installs custom GTK themes and sets them as the system theme.

### Wallpaper Configuration
- The script downloads wallpapers and sets them as the desktop background using `gsettings set org.gnome.desktop.background picture-uri`.

### User Interaction
- The script prompts the user for a system restart using the `read -p` command.
- After the installation is complete, a notification is displayed using `notify-send`.

## Customization
The script can be customized by modifying variables and options within the script itself. Refer to the script's comments for details on customization options.

## Contributing
Contributions to this script are welcome. Please follow the guidelines in the [CONTRIBUTING](CONTRIBUTING.md) file if you'd like to contribute.

## Contact
For questions, feedback, or issues related to the script, feel free to contact me via email or by opening an issue on the GitHub repository.

---

**Disclaimer:** This script is provided as-is and without any warranty. Use it responsibly and at your own risk.
