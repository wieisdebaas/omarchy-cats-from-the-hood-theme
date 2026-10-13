# Ayaka Palette for Cats From The Hood Implementation Plan

> **For agentic workers:** REQUIRED SUB-SKILL: Use superpowers:subagent-driven-development (recommended) or superpowers:executing-plans to implement this plan task-by-task. Steps use checkbox (`- [ ]`) syntax for tracking.

**Goal:** Replace `colors.toml` with Ayaka’s full palette, using `#222222` as the main background instead of pitch black, while keeping cat wallpapers.

**Architecture:** Single Omarchy v4 theme file update. No wallpaper, preview, icon, or README changes. Omarchy regenerates app configs from `colors.toml` on theme apply.

**Tech Stack:** Omarchy theme `colors.toml` (TOML)

## Global Constraints

- Keep `backgrounds/Cats02.jpg`, `preview.png`, `icons.theme`, `README.md` unchanged
- Do not copy Ayaka background images
- Main `background` must be `#222222` (not `#000000`)

---

### Task 1: Update colors.toml

**Files:**
- Modify: `colors.toml`

**Interfaces:**
- Consumes: Ayaka palette mapping from `docs/superpowers/specs/2026-10-13-ayaka-palette-design.md`
- Produces: Valid Omarchy v4 `colors.toml` with Ayaka accents and `#222222` background

- [ ] **Step 1: Write the new colors.toml**

Replace entire file with:

```toml
# Ayaka palette (background softened to #222222). Omarchy v4.
mode = "dark"

accent = "#6699ff"
selection = "#2a2a2a"
selection_foreground = "#ffffff"
muted = "#404040"

background = "#222222"
dark_background = "#262626"
darker_background = "#1a1a1a"
lighter_background = "#404040"

foreground = "#e6e6e6"
dark_foreground = "#404040"
light_foreground = "#f2f2f2"
bright_foreground = "#ffffff"

red = "#e65c5c"
yellow = "#ffcc66"
orange = "#ffcc66"
green = "#66cc66"
cyan = "#66cccc"
blue = "#6699ff"
magenta = "#cc66cc"
brown = "#262626"

bright_red = "#ff6666"
bright_yellow = "#ffdd80"
bright_green = "#80e680"
bright_cyan = "#80e6e6"
bright_blue = "#80b3ff"
bright_magenta = "#e680e6"
```

- [ ] **Step 2: Verify palette values**

Run:

```bash
grep -E '^(mode|background|accent|red|blue) ' colors.toml
```

Expected:

```
mode = "dark"
background = "#222222"
accent = "#6699ff"
red = "#e65c5c"
blue = "#6699ff"
```

Also confirm wallpapers untouched:

```bash
ls backgrounds/
```

Expected: `Cats02.jpg` only (or existing cat assets).

- [ ] **Step 3: Commit**

```bash
git add colors.toml docs/superpowers/specs/2026-10-13-ayaka-palette-design.md docs/superpowers/plans/2026-10-13-ayaka-palette.md
git commit -m "$(cat <<'EOF'
Apply Ayaka color palette with softer #222222 background.

EOF
)"
```
