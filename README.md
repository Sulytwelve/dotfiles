# dotfiles

My personal configuration files for Arch Linux on ThinkPad X270.

## Environment

| Component | |
|---|---|
| OS | Arch Linux (rolling) |
| WM | Hyprland 0.55.2 (Wayland) |
| Shell | bash |
| Terminal | kitty |
| Status Bar | waybar |
| Launcher | tofi |
| Notifications | mako |
| File Manager | Thunar (xfce4) |
| Input Method | fcitx5 + Rime |
| Fonts | JetBrainsMono Nerd Font, Noto Sans CJK TC |

## Structure

```
.fontconfig/        # Font rendering configuration
.gtk-3.0/           # GTK3 theme settings
.gtk-4.0/           # GTK4 theme settings
.hypr/              # Hyprland (hyprland, hypridle, hyprlock, hyprpaper)
.kitty/             # Kitty terminal
.mako/              # Notification daemon
.Thunar/            # Thunar file manager
.tofi/              # Application launcher
.waybar/            # Wayland status bar
.xfce4/             # XFCE panel settings
.qq-flags.conf      # QQ Wayland flags
```

## Installation

```bash
# Stow-based approach (recommended)
stow -t ~ */

# Or manual symlinks
ln -sf $(pwd)/hypr ~/.config/hypr
ln -sf $(pwd)/waybar ~/.config/waybar
# ... etc
```

## Notes

- `hypr/` contains template configs — adjust `monitor` and input settings for your hardware.
- Built for **zh_CN.UTF-8** locale with Traditional Chinese support.
