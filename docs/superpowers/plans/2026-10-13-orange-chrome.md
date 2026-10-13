# Orange Chrome Implementation Plan

**Goal:** Recolor accent/blue chrome to `#e68e0d` and switch folder icons to warm Yaru.

**Architecture:** Two-file Omarchy theme update; Omarchy regenerates borders from `accent` on theme apply.

**Tech Stack:** Omarchy `colors.toml`, `icons.theme`

---

### Task 1: Update palette and icons

**Files:**
- Modify: `colors.toml`
- Modify: `icons.theme`

- [ ] Set `accent`, `blue`, `orange` to `#e68e0d`; `bright_blue` to `#f0a83a`
- [ ] Set `icons.theme` to `Yaru-yellow`
- [ ] Sync the same files into `~/.config/omarchy/themes/cats-from-the-hood/`
- [ ] Run `omarchy theme set "Cats From The Hood"`
- [ ] Commit and push the theme repo
