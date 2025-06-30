# xorg.conf.d
persistant configuration for keyboard and mouse on xorg
[Arch Wiki](https://wiki.archlinux.org/title/Xorg#Configuration)

# Keyboard
[Xorg/Keyboard configuration](https://wiki.archlinux.org/title/Xorg/Keyboard_configuration) - Arch Wiki

Open up the file using any text editor (of course it should be vim)

```bash
/etc/X11/xorg.conf.d/00-keyboard.conf
```
Then add
```bash
Option "XkbOptions" "your options"
```
```bash
localectl list-x11-keymap-layouts
caps:escape, korean:ralt_hangul, korean:rctrl_hanja
```
