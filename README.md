# Acme Prints — Hyperframes

Three [HeyGen Hyperframes](https://hyperframes.heygen.com/) compositions for [acmeprints.com](https://acmeprints.com/). Each is a self-contained 1920×1080 HTML/CSS/JS scene with a GSAP timeline, ready to be previewed in a browser or rendered to MP4 with the Hyperframes CLI.

## Live preview

GitHub Pages: see the **Pages** tab in this repo's settings, or visit the URL printed under "About" once the site is live.

| | | |
|---|---|---|
| **01** | `variation-1/` | **25 Years — Brand Hero.** CMYK chromatic split on the "25", halftone field, registration marks + mono labels, organic SVG ink splats, scrolling product-category marquee, full-bleed word-flash montage, smash-to-paper lockup. ~12.5s. |
| **02** | `variation-2/` | **Lookbook — Product Showcase.** Editorial cream-paper magazine spread. Big "PRINT // ANYTHING.", 3×2 product card grid (T-shirts, mugs, posters, stickers, totes, hoodies), page-flip into a Risograph hero panel, "Order yours." CTA in corner brackets. ~12.5s. |
| **03** | `variation-3/` | **Press Night — Live Event Reel.** Broadcast HUD (live timecode, GPS coords, signal bar). Diagonal "LIVE PRINTING" with chromatic ghosts, glitch-slice transitions, odometer counter (000→247), venue list, "WE BRING THE PRESS TO YOU." smash-cut to a final stats CTA. ~13.5s. |

## Local preview

Any static server. With Python:

```bash
python3 -m http.server 8765
# open http://localhost:8765/
```

Each composition auto-plays via GSAP when loaded in a plain browser. Open the page in a 1920×1080 window for the intended composition.

## Render to MP4

These are Hyperframes-conformant: each root has `data-composition-id`, `data-width`, `data-height`; each act is a `class="clip"` with `data-start`/`data-duration`/`data-track-index`; the GSAP timeline is registered on `window.__timelines[<id>]` (paused).

```bash
npx hyperframes render --output 25-years.mp4
```
