# lazy_c4t — GitHub Pages drop-in

Drop the contents of this folder into your `heartfire567.github.io` repo (at the **repo root**, not in a subfolder), commit, and push. GitHub Pages will serve it automatically.

## Structure

```
heartfire567.github.io/
├── index.html
└── assets/
    ├── model.png            ← your vtuber model photo
    └── sponsor-waifee.png   ← Waifee Coffee sponsor art
```

## Editing content

All text/links/schedule/sponsors live in the `window.LAZY_C4T_CONFIG` object at the **top of `index.html`** (first `<script>` block, around lines 12–60). Change values there and commit — no build step.

- **Socials** — set `href` to your real URLs (empty string = "#" placeholder)
- **Schedule** — each day: `time`, `game`, `vibe` (set `game: null` for off days)
- **Sponsors** — `placeholder: true` renders an "OPEN SLOT" card
- **Support** — Ko-Fi / Throne / Streamlabs links
- **Contact** — `business_email` and `manager`

## Swapping the model image

Replace `assets/model.png` with your own art. Any filename works — just update the `<img src>` in `index.html` (search for `assets/model.png`, one occurrence).

## Dev notes

- Single-file app, no build, no deps except the Google Fonts link
- Fonts: VT323, Press Start 2P, JetBrains Mono (all free via Google Fonts)
- Idle-decay glitch effects fire after 1/2/3/4/5 minutes of inactivity
- Pet meter + blinkies persist in `localStorage`
