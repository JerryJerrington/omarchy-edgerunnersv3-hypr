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

## Installation

### Option 1: Clone both as git repos (recommended for updates)

1. Install the main theme:
```bash
omarchy theme install https://github.com/JerryJerrington/omarchy-edgerunnersv3-theme.git
```

2. Clone the animations/borders repo separately:
```bash
git clone https://github.com/JerryJerrington/omarchy-edgerunnersv3-hypr.git ~/.config/omarchy/themes/edgerunners-v3-hypr
```

3. Copy the files to your active theme:
```bash
cp ~/.config/omarchy/themes/edgerunners-v3-hypr/hyprland.lua ~/.config/omarchy/themes/edgerunners-v3/
cp ~/.config/omarchy/themes/edgerunners-v3-hypr/colors.toml ~/.config/omarchy/themes/edgerunners-v3/
```

4. Apply the theme:
```bash
omarchy theme set edgerunners-v3
```

### Option 2: Remove .git from main theme to use bundled files

If you want to use the main theme with its original files as-is (without separate repos), clone it locally and remove the `.git` directory:
```bash
git clone https://github.com/JerryJerrington/omarchy-edgerunnersv3-theme.git ~/.config/omarchy/themes/edgerunners-v3
rm -rf ~/.config/omarchy/themes/edgerunners-v3/.git
omarchy theme set edgerunners-v3
```

**Note:** Omarchy ignores `.lua` files and terminal configs in themes that contain a `.git` directory (installed via `omarchy theme install`). To use custom `hyprland.lua` with animations/borders, either remove `.git` from the theme directory, or copy the files from this separate repo as shown above.
