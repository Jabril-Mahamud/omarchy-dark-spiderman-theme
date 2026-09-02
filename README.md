# Dark Spiderman

An [Omarchy](https://omarchy.org) theme. Black background, warm red/orange/gold accents,
nine Spider-Man wallpapers.

Built with [Aether](https://github.com/omacom-io/aether).

## Install

```bash
omarchy theme install https://github.com/Jabril-Mahamud/omarchy-dark-spiderman-theme
omarchy theme set "Dark Spiderman"
```

## Backgrounds

Nine wallpapers ship in `backgrounds/`. Cycle them with `omarchy theme bg next`,
or pick one from `omarchy theme bg-switcher`.

## What's in here

`colors.toml` is the palette. Omarchy renders Alacritty, Foot, Ghostty, Kitty,
Hyprland, Neovim, btop, Chromium, Helix, VS Code and the shell from it via its own
templates, so this repo does not ship those files — a theme installed from a git
repo cannot supply Lua, a terminal config or `vscode.json` anyway.

Everything else here is a config Omarchy has no template for:

| File | App |
|------|-----|
| `hyprlock.conf` | Hyprlock |
| `mako.ini` | Mako notifications |
| `swayosd.css` | SwayOSD |
| `waybar.css` | Waybar |
| `walker.css` | Walker |
| `wofi.css` | Wofi |
| `zellij.kdl` | Zellij |
| `warp.yaml` | Warp |
| `vencord.theme.css` | Discord (Vencord / Vesktop) |
| `aether.zed.json` | Zed |
| `icons.theme` | GTK icon theme |

### Discord

`vencord.theme.css` is not applied automatically. Link it once and it follows
whatever Omarchy theme is active:

```bash
ln -sfn ~/.local/state/omarchy/current/theme/vencord.theme.css ~/.config/vesktop/themes/omarchy.css
```

Then enable `omarchy.css` under Vencord → Themes.

## Wallpapers

Sourced from [wallhaven.cc](https://wallhaven.cc). Credit to the original artists.
