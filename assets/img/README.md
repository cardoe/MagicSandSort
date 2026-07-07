# Site images

Drop the game's images here with these **exact filenames** — the site picks them
up automatically (and gracefully falls back to placeholders if any are missing):

| File                | Used for                                             |
| ------------------- | ---------------------------------------------------- |
| `icon.png`          | App icon — favicon, header logo, and home-page hero  |
| `screenshot-1.png`  | First screenshot in the home-page gallery            |
| `screenshot-2.png`  | Second screenshot                                    |
| `screenshot-3.png`  | Third screenshot                                     |

Notes:

- `icon.png` should be square (e.g. 512×512 or 1024×1024). It's displayed rounded.
- Screenshots can be full phone captures (portrait). They're scaled down to fit.
- To add more screenshots, save `screenshot-4.png`, etc., and bump the `seq 1 3`
  range in `layouts/index.html`.
- These live under `assets/` (not `static/`) so Hugo only publishes the ones that
  are actually present — no broken image links.
