# lpalmas zmk-conifg

to edit keyboard layout:

```txt
config/corne_choc_pro.keymap
```

## compile new firmware

1. after changes push to github --> runner is compiling the firmware.
2. downloaded from actions page.
3. plugin keyboard via usb cable (both sides needed)
4. drag and drop firmware from downloads folder

## keymap drawer

run in project root

```bash
keymap -c keymap-drawer/keymap_drawer.yaml parse -z config/corne_choc_pro.keymap | sed 's/zmk_keyboard: corne_choc_pro/zmk_keyboard: corneish_zen/' | sed 's/layout_name: default_layout/layout_name: foostan_corne_6col_layout/' > keymap-drawer/keymap.yaml && keymap draw keymap-drawer/keymap.yaml > keymap-drawer/keymap.svg
```
