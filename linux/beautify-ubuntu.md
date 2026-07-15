---
description: Use Keift style Ubuntu.
icon: ubuntu
---

Paste these commands into your terminal for a Keift style Ubuntu.

```shell
gsettings set org.gnome.desktop.interface accent-color "blue"
gsettings set org.gnome.desktop.interface icon-theme "Yaru-blue"
gsettings set org.gnome.desktop.interface gtk-theme "Yaru-blue"

gsettings set org.gnome.shell.extensions.ding icon-size "standard"
gsettings set org.gnome.shell.extensions.ding start-corner "bottom-right"
gsettings set org.gnome.shell.extensions.ding show-home false
gsettings set org.gnome.shell.extensions.ding show-trash false

gsettings set org.gnome.shell.extensions.dash-to-dock dock-fixed true
gsettings set org.gnome.shell.extensions.dash-to-dock extend-height false
gsettings set org.gnome.shell.extensions.dash-to-dock dash-max-icon-size 48
gsettings set org.gnome.shell.extensions.dash-to-dock multi-monitor false
gsettings set org.gnome.shell.extensions.dash-to-dock dock-position "BOTTOM"
gsettings set org.gnome.shell.extensions.dash-to-dock show-mounts true
gsettings set org.gnome.shell.extensions.dash-to-dock show-mounts-only-mounted false
gsettings set org.gnome.shell.extensions.dash-to-dock show-mounts-network true
gsettings set org.gnome.shell.extensions.dash-to-dock show-trash true
gsettings set org.gnome.shell.extensions.dash-to-dock click-action "minimize"

gsettings set org.gnome.shell.extensions.tiling-assistant enable-tiling-popup true
gsettings set org.gnome.shell.extensions.tiling-assistant disable-tile-groups false

sudo snap remove firefox
sudo apt install -y flatpak gnome-software gnome-software-plugin-flatpak
flatpak remote-add --if-not-exists flathub https://flathub.org/repo/flathub.flatpakrepo
flatpak install -y org.mozilla.firefox

gsettings set org.gnome.shell favorite-apps "['org.gnome.Software.desktop', 'org.gnome.Nautilus.desktop', 'org.gnome.TextEditor.desktop', 'org.gnome.Ptyxis.desktop', 'org.mozilla.firefox.desktop']"
```
