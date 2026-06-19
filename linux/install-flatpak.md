---
description: Use your Flatpak with GUI.
icon: basket-shopping
---

## Install Flatpak and Bazaar

You can install it as follows.

```shell
# Debian, Ubuntu, Linux Mint, Kali Linux, Pop!_OS (APT)
sudo apt install -y flatpak

# RHEL, Fedora, CentOS, AlmaLinux, Rocky Linux (DNF)
sudo dnf install -y flatpak

# Arch Linux, Manjaro, CachyOS, EndeavourOS, Artix Linux (Pacman)
sudo pacman -S --noconfirm flatpak

# openSUSE Tumbleweed, openSUSE Leap, SUSE Linux Enterprise, GeckoLinux, Regata OS (Zypper)
sudo zypper -n install flatpak

# Define Flathub remote reference
sudo flatpak remote-add --if-not-exists flathub https://flathub.org/repo/flathub.flatpakrepo

# To use Flatpak with a GUI, we download Bazaar
sudo flatpak install -y io.github.kolunmi.Bazaar
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

## TIP: Uninstall Flatpak

You can uninstall it as follows.

```shell
# Debian, Ubuntu, Linux Mint, Kali Linux, Pop!_OS (APT)
sudo apt purge -y --autoremove flatpak

# RHEL, Fedora, CentOS, AlmaLinux, Rocky Linux (DNF)
sudo dnf remove -y flatpak

# Arch Linux, Manjaro, CachyOS, EndeavourOS, Artix Linux (Pacman)
sudo pacman -Rns --noconfirm flatpak

# openSUSE Tumbleweed, openSUSE Leap, SUSE Linux Enterprise, GeckoLinux, Regata OS (Zypper)
sudo zypper -n remove -u flatpak
```
