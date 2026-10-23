---
type: Guide
title: Design Mockups
description: Static design-mockup workflow for exploring visual directions for Radiant Gardens without touching the Astro build.
tags: [design, mockups, workflow]
status: current
generated:
  by: Astro rebuild agent (OpenCode)
  at: 2026-10-24T00:00:00Z
---

# Design Mockups

Plain static HTML explorations of visual directions for the site. They exist
so design can move faster than the Astro build: open a folder in a browser,
tweak one CSS file, compare against the baseline in the gallery.

## Hard boundaries

- **Not Astro routes.** Nothing in `mockups/` is built, bundled, or deployed.
- **Never in `public/` or `dist/`.** The Astro build must stay unaware of
  this folder.
- **Never linked from the site.** No page in `src/pages/` may reference
  `mockups/`.
- **No JS, no new external assets.** Markup, real content, linked CSS —
  nothing else.

## Workflow rules

1. **One variable at a time.** A variant changes exactly one design
   dimension (e.g. token palette, spacing scale, display type scale) versus
   the baseline. Want to try two things? Make two dated variants.
2. **Dated variant folders.** New explorations go in
   `YYYY-MM-DD-<name>/` (e.g. `2026-10-24-linen/`). Never edit another
   variant's folder to "iterate" — open a new dated folder.
3. **Link the real stylesheet, override only.** Every mockup page links the
   production `../../src/styles/global.css` first, then its local
   `variant.css`. Never copy or fork `global.css`; variants override tokens
   and add only what tokens cannot reach.
4. **Identical markup.** All mockup pages share byte-identical HTML (start
   from `current/index.html`). Variants change `variant.css` only — never
   the markup.
5. **Real content only.** Copy comes from `src/pages/`. Respect the
   public/private content boundary in `docs/notes.md`: no invented contact
   details, pricing, testimonials, or photos.
6. **Record verdicts.** After reviewing a variant, write its verdict
   (adopt / reject / iterate, and why) in `docs/notes.md`.

## Promotion path

A winning variant never gets "merged" as a folder. Instead:

```text
review verdict: adopt
  → git checkout -b design/<name>   (from feature/astro-rebuild)
  → port variant.css changes into src/styles/global.css
  → open a normal PR
```

The mockup folder stays behind as reference; the production stylesheet is
the only thing that ships.

## Folder map

| Path | Role |
| --- | --- |
| `index.html` | Neutral dark gallery: labeled previews of every variant plus the baseline. |
| `current/` | Baseline — faithful static reproduction of the homepage with real class names and real copy; `variant.css` is a documented no-op. |
| `2026-10-24-linen/` | First variant, "linen" — lighter/softer direction (tokens only; see its `variant.css` header). |

## Viewing

Open `mockups/index.html` directly in a browser (relative CSS paths work
over `file://`), or serve the repo root so the gallery iframes resolve:

```bash
cd /home/ubuntu/projects/sites/radiant-gardens
python3 -m http.server 4173
# → http://localhost:4173/mockups/
```
