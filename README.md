# Grooptown — Modernized Website

A modern, single-page revamp of [grooptown.com](https://grooptown.com/) for
Grooptown, a data-engineering consulting firm.

## Highlights

- **3D animated data-graph background** — a drifting network of glowing nodes and
  connecting edges, rendered with [Three.js](https://threejs.org/). Reacts to
  mouse movement and scroll. Built to evoke "data engineering."
- **Scroll & entrance animations** with [GSAP](https://gsap.com/) + ScrollTrigger
  (hero intro, staggered card reveals, timeline).
- **Modern UI**: dark + neon (cyan/violet) theme, glassmorphism cards, gradient
  text, 3D card tilt on hover, sticky blur navbar, scroll-progress bar.
- **Fully responsive** with a mobile hamburger menu.
- **Accessible & performant**: semantic HTML, keyboard-focusable nav, honors
  `prefers-reduced-motion`, caps pixel ratio, pauses rendering on hidden tabs,
  and falls back gracefully if WebGL or the CDN libs are unavailable.

## Run it

It's a single self-contained file — no build step.

```bash
open index.html          # macOS
```

> The 3D library and GSAP load from public CDNs (via an ES-module import map),
> so an internet connection is needed on first load. Opening the file directly
> (`file://`) works in modern browsers.

To serve it locally instead:

```bash
python3 -m http.server 8000
# then visit http://localhost:8000
```

## Structure

- `index.html` — the entire site: HTML, CSS (in `<style>`), the Three.js
  background, and UI interaction scripts.

## Sections

Home (hero) · Services · News (timeline) · Team · References · Contact.

## Customizing

- **Theme colors**: edit the CSS custom properties under `:root` (`--cyan`,
  `--violet`, `--accent-grad`, etc.).
- **3D density/feel**: tweak `NODE_COUNT`, `LINK_DIST`, and `SPREAD` in the
  background `<script type="module">`.
- **Client logos**: the References section currently uses styled text wordmarks
  (Kering, Qorum, Société Générale). Swap in real SVG/PNG logos when available.
- **Contact**: the CTA is a `mailto:` to `contact-from-website@grooptown.com`
  (no backend), matching the original site.

## Content

All copy (services, timeline, team bios) is carried over from the live site.
