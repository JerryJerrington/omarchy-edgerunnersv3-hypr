# Edgerunners V3 - Hyprland Borders & Animations

This repo contains just the Hyprland-specific styling for the [Edgerunners V3](https://github.com/JerryJerrington/omarchy-edgerunnersv3-theme) theme. 

## Contents

- `hyprland.lua` - Window border colors, gradients, and animation curves/effects for Hyprland
- `colors.toml` - Color definitions including `hyprland_active_border` and `hyprland_inactive_border`

## Borders

The theme uses a cyberpunk neon gradient for active windows with magenta and cyan accents. Inactive windows use a subtle tinted border to keep focus on the active window without being too distracting.

- **Active border**: Magenta → Cyan gradient (`rgba(E957E8) rgba(9BF1F2) 25deg`) - creates the signature Edgerunners neon glow
- **Inactive border**: Tinted magenta (`rgba(b57edcaa)`) - keeps the cyberpunk aesthetic while clearly indicating focus state

## Animations

Custom animation curves and animations tuned for a snappy, cyberpunk feel:
- Smooth bezier curves for window movements and workspace transitions
- Fast, responsive animations that feel fluid without being sluggish
- Optimized for a sleek desktop experience

## Usage

This repo is meant to be used alongside the main theme. Since Omarchy ignores `.lua` files in git-cloned themes, you can clone this repo separately and link or copy the files to your theme directory if you want just the borders/animations.

```bash
git clone https://github.com/JerryJerrington/omarchy-edgerunnersv3-hypr.git
```

Then copy `hyprland.lua` and `colors.toml` to your theme's directory as needed.


## Main Theme

This pairs with [omarchy-edgerunnersv3-theme](https://github.com/JerryJerrington/omarchy-edgerunnersv3-theme). The main theme no longer ships `hyprland.lua` or terminal configs to comply with Omarchy's theme distribution rules.
