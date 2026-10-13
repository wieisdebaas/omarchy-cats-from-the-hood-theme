# Design: Orange chrome (outlines + folders)

## Goal

Shift Cats From The Hood’s blue UI chrome to orange `#e68e0d` — window outlines, ANSI blue, and folder icons.

## Non-goals

- Do not change wallpapers, `preview.png`, or README branding
- Do not invent a custom icon theme; use an existing Yaru pack
- Do not change red/green/cyan/magenta or backgrounds

## Approach (approved: flat orange)

| Field | Before | After |
| --- | --- | --- |
| `accent` | `#6699ff` | `#e68e0d` |
| `blue` | `#6699ff` | `#e68e0d` |
| `orange` | `#ffcc66` | `#e68e0d` |
| `bright_blue` | `#80b3ff` | `#f0a83a` |
| `icons.theme` | `Yaru-blue` | `Yaru-yellow` |

`bright_blue` is a lighter orange so bright ANSI still differs slightly from normal blue.

## Apply

Update the theme repo and local `~/.config/omarchy/themes/cats-from-the-hood/`, then run `omarchy theme set "Cats From The Hood"`.
