# dotfiles

Wayland (Hyprland) dotfiles for Arch Linux on ThinkPad X270.

- **zh_CN.UTF-8** locale with Traditional Chinese support
- Built around the Hyprland ecosystem on Wayland

## Environment

| Component | |
|---|---|
| OS | Arch Linux (rolling) |
| Display Server | **Wayland** |
| WM / Compositor | **Hyprland** 0.55.2 |
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
.fontconfig/        # Font rendering (.antialias, .hinting, CJK fallback order)
.gtk-3.0/           # GTK3 theme settings
.gtk-4.0/           # GTK4 theme settings
.hypr/              # Hyprland — compositor, idle, lock, wallpaper
.kitty/             # Kitty terminal (JetBrainsMono Nerd Font, opacity)
.mako/              # Notification daemon (dark theme, CJK font)
.Thunar/            # Thunar file manager (custom actions)
.tofi/              # Application launcher (full-screen, dark)
.waybar/            # Wayland status bar (Hyprland-centric modules)
.xfce4/             # XFCE panel & Thunar integration
.qq-flags.conf      # QQ Wayland Electron flags
```

## Installation

```bash
# Stow (recommended)
stow -t ~ */

# Or manual symlinks
ln -sf $(pwd)/hypr ~/.config/hypr
ln -sf $(pwd)/waybar ~/.config/waybar
# ... etc
```

## Notes

- `hypr/` contains template configs — adjust `monitor` and input settings for your hardware.
- This repo is Wayland + XWayland only; no X11/i3 configs.
