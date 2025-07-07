### Monitor connected but frozen
- resolution is probably wrong
- https://wiki.archlinux.org/title/Xrandr#Adding_undetected_resolutions
- `arandr` doesn't like modes that end with `_60`, do
  ```
  xrandr --output HDMI-1 --mode "2560x1440_60.00"
  ```
- use `arandr` after to adjust screen position
