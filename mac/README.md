# Connecting to the internet
An ethernet connection is required during the process of installing arch from a usb because Apple uses stupid Broadcom wifi card

test ethernet connection
``` bash
ping -c 5 archlinux.org
```
update pacman than install archinstall
``` bash
pacman -Sy
pacman -S archinstall
```
then run the script by entering
```bash
archinstall
```
# the Archinstall script
## Mirros and repositories
- select your region and recommened to enable multilib
## Disk configuration
- btrfs: better for creating minimal size snapshots due to use of copy-on-write
- ext4: known for stability
## Swap
- recommened to enable swap on zram
## Authentication
- set the root password for the root account and create a user and give it sudo
## Profile
### Type
there are many options you can choose, but if you want a full blown desktop environment,there are two wellknown options
- GNOME: Have a macOS like style with hidden dock by default
- KDE: Have a Windows like style with a task manager by default
### Graphic driver
Choose All open-source or Intel(open-source) if you want minimal "bloat"
## Applications
- Enable bluetooth
- Choose pipewire for Audio
## network configuration
- Just use networkmanager

Then select timezone and select Install

# Installing AUR Helper
You can use yay or paru, both will do the samething
https://github.com/Jguer/yay
https://github.com/Morganamilo/paru

# Connect to Wifi
```bash
sudo pacman -S broadcom-wl or broadcom-wl-dkms
yay -S b43-firmware-classic

reboot
```
If it still does not appear try this guide:
https://github.com/kr4fty/Config_BCM4360_on_Linux/

# Installing flatpak
```bash
sudo pacman -S flatpak
```
Then add the repo
```bash
sudo flatpak remote-add --if-not-exists flathub https://flathub.org/repo/flathub.flatpakrepo
```
Reboot

# Korean Input (Hangul)
## Install a hangul font
example
```bash
sudo pacman -S noto-fonts-cjk
```
## Gnome
```bash
sudo pacman -S ibus ibus-hangul
```
## KDE
```bash
sudo pacman -S fcitx5-im fcitx5-hangul
```
If you are on Wayland select "Fcitx5 Wayland Launcher" on Settings -> Keyboard -> VirtualKeyboards
