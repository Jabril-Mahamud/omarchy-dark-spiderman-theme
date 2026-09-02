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

Built for Omarchy 4 (Quattro). `colors.toml` is the palette and does almost all
the work: Omarchy renders Hyprland (`hyprland.lua`, `gum_env.lua`), Neovim, the
Quickshell bar and lock screen, Alacritty, Foot, Ghostty, Kitty, btop, Helix,
Chromium and VS Code from it through its own templates on install.

A theme installed from a git repo deliberately cannot ship `*.lua`, a terminal
config or `vscode.json` — those name programs that get launched, so Omarchy
generates them from the palette instead. That is why they are not in here.

That leaves:

| File | Consumer |
|------|----------|
| `colors.toml` | everything above |
| `backgrounds/` | `omarchy theme bg next`, background switcher |
| `icons.theme` | `omarchy-theme-set-gnome` |
| `vencord.theme.css` | Discord (Vencord / Vesktop), wired up manually — see below |

### Discord

`vencord.theme.css` is not applied by Omarchy. Link it once and it follows
whatever Omarchy theme is active:

```bash
ln -sfn ~/.local/state/omarchy/current/theme/vencord.theme.css ~/.config/vesktop/themes/omarchy.css
```

Then enable `omarchy.css` under Vencord → Themes.

It is a child of [base16-discord](https://github.com/imbypass/base16-Discord)
(MIT) with two fixes worth stealing if you build one:

- `--base01`–`--base04` are set explicitly. The parent derives them as
  `color-mix(--color00, white)`, which goes flat neutral grey when your
  background is pure black.
- The muted text roles (`--text-muted`, `--channels-default`, `--text-tertiary`)
  are pulled off `--base03`, which the parent also spends on surfaces. At a
  surface-appropriate value they land at 1.4:1 and the channel and DM lists are
  unreadable; they now sit at 6.1:1.

## Wallpapers

Sourced from [wallhaven.cc](https://wallhaven.cc). Credit to the original artists.
