# Design: Apply Ayaka color palette (keep cat wallpapers)

## Goal

Update **Cats From The Hood** so its Omarchy `colors.toml` uses the full [Ayaka](https://omarchytheme.com/themes/ayaka/) color palette, while keeping this theme’s own background images.

## Non-goals

- Do not copy Ayaka wallpaper/background images
- Do not change repo file layout to Ayaka’s older multi-config format
- Do not change `icons.theme`, README branding, or cat `preview.png`
- Do not restyle Hyprland layout / blur / gaps beyond what Omarchy derives from `colors.toml`

## Approach

Single-file update: rewrite `colors.toml` in Omarchy v4 format, mapped 1:1 from Ayaka’s published palette (and matching values in Ayaka’s `alacritty.toml`).

## Color mapping

| `colors.toml` field | Value | Ayaka source |
| --- | --- | --- |
| `mode` | `dark` | dark theme |
| `background` | `#222222` | Ayaka bg softened (not pitch black) |
| `dark_background` | `#262626` | color0 |
| `darker_background` | `#1a1a1a` | slightly darker than bg |
| `lighter_background` | `#404040` | color8 |
| `foreground` | `#e6e6e6` | foreground |
| `dark_foreground` | `#404040` | color8 |
| `light_foreground` | `#f2f2f2` | color7 |
| `bright_foreground` | `#ffffff` | color15 |
| `accent` | `#6699ff` | accent / color4 |
| `selection` | `#2a2a2a` | selection background |
| `selection_foreground` | `#ffffff` | selection foreground |
| `muted` | `#404040` | color8 |
| `red` | `#e65c5c` | color1 |
| `green` | `#66cc66` | color2 |
| `yellow` | `#ffcc66` | color3 / cursor |
| `orange` | `#ffcc66` | color3 (no separate orange) |
| `blue` | `#6699ff` | color4 |
| `magenta` | `#cc66cc` | color5 |
| `cyan` | `#66cccc` | color6 |
| `brown` | `#262626` | no Ayaka brown; reuse color0 |
| `bright_red` | `#ff6666` | color9 |
| `bright_green` | `#80e680` | color10 |
| `bright_yellow` | `#ffdd80` | color11 |
| `bright_blue` | `#80b3ff` | color12 |
| `bright_magenta` | `#e680e6` | color13 |
| `bright_cyan` | `#80e6e6` | color14 |

## Files

| Path | Action |
| --- | --- |
| `colors.toml` | Replace with Ayaka-mapped palette |
| `backgrounds/Cats02.jpg` | Keep |
| `preview.png` | Keep |
| `icons.theme` | Keep (`Yaru-blue`) |
| `README.md` | Keep |

## Success criteria

- `colors.toml` values match Ayaka’s palette as mapped above
- Cat wallpaper remains the only background asset in the repo
- Theme still installs/applies as an Omarchy v4 theme (`omarchy theme set "Cats From The Hood"`)
