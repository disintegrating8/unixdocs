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
