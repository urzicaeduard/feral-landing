# FERAL — Landing Page

A scroll-driven, single-file landing page for the fictional sports brand **FERAL**.
Built as a portfolio piece with vanilla HTML + CSS + JavaScript — zero frameworks,
zero build step, zero npm dependencies.

> Tagline: *You hear the gun. We're already gone.*

## Features

- **Scroll-driven 3D hero** — 120 frames extracted via FFmpeg, rendered to a `<canvas>`
  and advanced/reversed via `requestAnimationFrame` based on scroll position.
- **Gooey pixel trail** — vanilla port of the SVG `feGaussianBlur` + `feColorMatrix`
  goo filter applied to a mouse-driven pixel grid (manifesto section).
- **Spotlight glow cards** — cursor-tracked radial-gradient borders on the teaser
  grid, masked to the border ring via `mask-composite`.
- **Sticky parallax showcase** — three full-bleed image blocks with scroll-driven
  scale, opacity, and translate transforms.
- **Sliding pill nav** — a cursor that glides between nav items, with the active
  item's text inverting color.
- **Animated warp gradient** — a multi-layered, blurred radial-gradient backdrop
  on the page's white sections, drifting on a slow loop.
- **Trust bar with overlapping avatars**, animated count-up stats, tabbed pillars,
  marquee tagline strip, full a11y (skip link, focus rings, ARIA, keyboard nav,
  `prefers-reduced-motion`), full mobile drawer, and JSON-LD schema for SEO.

## Stack

| Layer | Tech |
| --- | --- |
| Markup | Semantic HTML5 |
| Styles | Vanilla CSS (custom properties, `mask-composite`, `mix-blend-mode`, `backdrop-filter`) |
| Scripts | Vanilla JavaScript (IntersectionObserver, RAF render loops, no libs) |
| Fonts | Google Fonts — *Bagel Fat One*, *Bricolage Grotesque*, *Inter* |
| Imagery | Unsplash (License-free) |

## Run locally

```bash
# Any static server works. Python is the simplest:
python -m http.server 8080
# then open http://localhost:8080/
```

A local server is required because the canvas frame loader fetches `frames/*.jpg`
relative paths.

## Project structure

```
.
├── index.html          # The whole site — HTML + CSS + JS in one file
├── frames/             # 120 JPEG frames extracted from the hero video at 10fps
├── .gitignore
└── README.md
```

## Credits

- Hero video frames generated with **Higgsfield AI** and extracted via **FFmpeg**.
- Photography: **Unsplash** contributors (Annie Spratt, et al.).
- Type: Google Fonts community.

— Built by [@urzicaeduard](https://github.com/urzicaeduard).
