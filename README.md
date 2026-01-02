# Dotfiles

My personal configuration files for Arch Linux with Hyprland.

## Contents

- **Hyprland** - Wayland compositor configuration
- **Kitty** - Terminal emulator
- **Waybar** - Status bar
- **Rofi** - Application launcher
- **Neovim** - Text editor (submodule)
- **Flameshot** - Screenshot tool
- **SwayNC** - Notification center
- **GTK** - GTK theme settings

## Prerequisites

Before installing these dotfiles, ensure you have the following packages installed:

```bash
sudo pacman -S hyprland kitty waybar rofi neovim flameshot swaync
```

Optional dependencies:
```bash
sudo pacman -S nwg-look xsettingsd dolphin
```

## Installation

### Fresh Install

**⚠️ Warning:** This will replace your existing `~/.config` directory. Back up your current configs first!

```bash
# Backup your existing config (recommended)
mv ~/.config ~/.config.backup

# Clone the repository
git clone --recurse-submodules https://github.com/Aneeshie/arch-hyprland.git ~/.config
```

### Selective Install

If you only want specific configs:

```bash
# Clone to a temporary location
git clone --recurse-submodules https://github.com/Aneeshie/arch-hyprland.git ~/dotfiles-temp

# Copy only what you need
cp -r ~/dotfiles-temp/hypr ~/.config/
cp -r ~/dotfiles-temp/kitty ~/.config/
cp -r ~/dotfiles-temp/waybar ~/.config/
# ... etc

# Clean up
rm -rf ~/dotfiles-temp
```

## Post-Installation

1. **Reload Hyprland**: Press `Super + Shift + R` or restart your session
2. **Check Waybar**: Run `~/.config/waybar/launch.sh` to start Waybar
3. **Neovim Setup**: Open nvim and let plugins install automatically
4. **GTK Themes**: Use `nwg-look` to apply GTK themes if needed

## Configuration

### Hyprland Keybindings

Check `~/.config/hypr/hyprland.conf` for all keybindings. Some common ones:
- `Super + Q` - Close window
- `Super + Return` - Open terminal
- `Super + D` - Open Rofi launcher
- `Super + Print` - Screenshot

### Customization

Feel free to modify any configs to suit your preferences:
- Waybar style: `~/.config/waybar/style.css`
- Kitty theme: `~/.config/kitty/kitty.conf`
- Rofi themes: `~/.config/rofi/launchers/`

## Neovim Configuration

The Neovim configuration is maintained as a separate repository and included as a git submodule.

Repository: [Aneeshie/nvim](https://github.com/Aneeshie/nvim)

## Notes

This configuration is tailored for my personal setup running Arch Linux with Hyprland. Some features may require additional tweaking for your hardware/preferences.

## Issues

If you encounter any problems, feel free to open an issue on GitHub.
