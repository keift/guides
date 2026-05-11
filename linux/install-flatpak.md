---
description: Use your Flatpak with Gnome Software.
icon: basket-shopping
---

## Install Flatpak and Gnome Software

You can install it as follows.

```shell
# Debian, Ubuntu, Linux Mint, Kali Linux, Pop!_OS (APT)
sudo apt install -y flatpak
sudo apt install -y gnome-software
sudo apt install -y gnome-software-plugin-flatpak

# RHEL, Fedora, CentOS, AlmaLinux, Rocky Linux (DNF)
sudo dnf install -y flatpak
sudo dnf install -y gnome-software
sudo dnf install -y gnome-software-plugin-flatpak

# Arch Linux, Manjaro, CachyOS, EndeavourOS, Artix Linux (Pacman)
sudo pacman -S --noconfirm flatpak
sudo pacman -S --noconfirm gnome-software
sudo pacman -S --noconfirm gnome-software-plugin-flatpak

# openSUSE Tumbleweed, openSUSE Leap, SUSE Linux Enterprise, GeckoLinux, Regata OS (Zypper)
sudo zypper -n install flatpak
sudo zypper -n install gnome-software
sudo zypper -n install gnome-software-plugin-flatpak

# Define Flathub remote reference
sudo flatpak remote-add --if-not-exists flathub https://flathub.org/repo/flathub.flatpakrepo
```

## TIP: Flatpak integration for Visual Studio Code

If you are using the Flatpak version of Visual Studio Code, the integrated terminal is also sandboxed. To fix this, go to **Settings > Top-Right Icon: Open Settings (JSON)** and paste the configuration below at the end of the file. This will make the IDE's terminal work flawlessly, just like your standard host terminal.

```json
{
  "terminal.integrated.profiles.linux": {
    "bash": {
      "path": "/app/bin/host-spawn",
      "args": ["bash"],
      "icon": "terminal-bash",
      "overrideName": true
    }
  },
  "terminal.integrated.defaultProfile.linux": "bash"
}
```

## TIP: Uninstall Flatpak and Gnome Software

You can uninstall it as follows.

```shell
# Debian, Ubuntu, Linux Mint, Kali Linux, Pop!_OS (APT)
sudo apt purge -y --autoremove flatpak
sudo apt purge -y --autoremove gnome-software
sudo apt purge -y --autoremove gnome-software-plugin-flatpak

# RHEL, Fedora, CentOS, AlmaLinux, Rocky Linux (DNF)
sudo dnf remove -y flatpak
sudo dnf remove -y gnome-software
sudo dnf remove -y gnome-software-plugin-flatpak

# Arch Linux, Manjaro, CachyOS, EndeavourOS, Artix Linux (Pacman)
sudo pacman -Rns --noconfirm flatpak
sudo pacman -Rns --noconfirm gnome-software
sudo pacman -Rns --noconfirm gnome-software-plugin-flatpak

# openSUSE Tumbleweed, openSUSE Leap, SUSE Linux Enterprise, GeckoLinux, Regata OS (Zypper)
sudo zypper -n remove -u flatpak
sudo zypper -n remove -u gnome-software
sudo zypper -n remove -u gnome-software-plugin-flatpak
```
