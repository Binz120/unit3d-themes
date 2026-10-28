# Synthwave Grid — a UNIT3D theme

A cyberpunk/synthwave skin for [UNIT3D](https://github.com/HDInnovations/UNIT3D-Community-Edition) tracker front ends.
Deep purple-black base, neon magenta and electric cyan accents, glowing panels, a perspective grid background, and geometric SVG icons in place of the default FontAwesome rank badges.

![Synthwave Grid preview](docs/preview.png)

**Live preview:** <https://binz120.github.io/unit3d-themes/>

---

## What's in here

| File | Purpose |
|---|---|
| `synthwave-grid.css` | The theme. Standalone stylesheet, no build step, no dependencies. |
| `index.html` | Static mock of a UNIT3D page so you can review the theme without installing it. |
| `docs/preview.png` | Screenshot of that mock. |

`index.html` is a design mock, not a running tracker: it hardcodes the markup and sample torrents. The theme itself is `synthwave-grid.css`.

## Install

UNIT3D exposes a per-user custom CSS box, so no rebuild is needed:

1. Host `synthwave-grid.css` somewhere public (raw.githubusercontent, a CDN, your own box) or paste its contents directly.
2. In UNIT3D go to **Settings → custom_css** and place the stylesheet there.
3. Pick a dark base first — the theme is tuned for **Galactic (style 1)** or **Material Dark (style 13)**.

Because it overrides UNIT3D's CSS custom properties rather than hardcoding selectors, most of the theme follows the base theme's structure; the glow and icon sections are the parts that assume specific component classes (`.top-nav`, `.panel__head`, `.chatbox`, `.badge-user`, `.bbcode-rendered`).

## Tuning

Everything meaningful lives in `:root` at the top of the file.

| Variable | Default | Controls |
|---|---|---|
| `--body-bg` | `#0d0221` | Page background behind the perspective grid |
| `--panel-bg` | `#1a0b2e` | Panel and card surfaces |
| `--top-nav-bg` | `#2d0a4e` | Top navigation bar |
| `--data-table-th-bg` | `#260a3f` | Table headers |
| `--color-light-blue` | `hsl(190, 100%, 60%)` | Primary accent (links, headings) |
| `--color-light-magenta` | `hsl(330, 100%, 65%)` | Secondary accent, glow, borders |
| `--color-light-green` | `hsl(160, 100%, 55%)` | Ratios and positive stats |
| `--text-color` | `#e0d6ff` | Body text |

To review locally:

```bash
git clone https://github.com/Binz120/unit3d-themes.git
cd unit3d-themes
python3 -m http.server 8000   # open http://localhost:8000
```

## Contributing

Selector fixes for other UNIT3D versions and forks are welcome — open an issue with a screenshot and the version you're on.

## License

MIT — see [LICENSE](LICENSE).
