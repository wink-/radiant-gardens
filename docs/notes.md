---
type: Notes
title: Notes
description: Repo-specific notes and gotchas for Radiant Gardens.
tags: [notes]
status: current
generated:
  by: Astro rebuild agent (OpenCode)
  at: 2026-10-24T00:00:00Z
---

# Notes

## Public/private content boundary (binding for the site)

Derived from the business-plan documents; apply to everything published on
the website:

- Never publish internal financials: revenue projections, profit/margin
  figures, startup costs, break-even math, or growth/acquisition/franchise
  strategy.
- Never publish unconfirmed operational details as fact: legal formation
  status, supplier arrangements, staffing plans, or specific pricing.
- No invented contact details: no phone, email, or address until they exist.
  `/contact/` uses visibly marked `[to be announced]` placeholders, and every
  page carries a site-wide "In planning — launching 2026" banner.
- No fabricated social proof: no testimonials, portfolio projects, or photos
  of gardens that do not exist. Decorative art is CSS/SVG only.
- The plans name the founder as "[Your Name]"; the site refers to "the
  founder" without inventing a name.
- Safe public material: mission, services (design, build, planting/coaching,
  Digital Support Hub), process, service area, and the honest in-planning
  status.

## Design mockup workflow (`mockups/`)

- `mockups/` holds plain static HTML design explorations, outside the Astro
  build: not Astro routes, never in `public/` or `dist/`, never linked from
  the site. No JS, no external assets, no build step.
- `mockups/current/` is the baseline: a faithful static reproduction of the
  homepage with real class names and real copy, linking the real
  `../../src/styles/global.css` plus a documented no-op `variant.css`.
- Variants live in dated folders (`YYYY-MM-DD-<name>/`) with markup
  byte-identical to the baseline; all changes live only in that folder's
  `variant.css`. One variable at a time. Real content only (respect the
  public/private boundary above).
- Promotion path: a winning variant is ported into `src/styles/global.css`
  on a `design/<name>` branch and merged via a normal PR. Mockup folders
  never ship. Full rules: `mockups/README.md`. Verdicts are recorded here.
- 2026-10-24 `linen` — intent: a lighter/softer direction. More cream,
  lighter sage, terracotta accent pulled back, extra whitespace, larger
  serif display scale, gentler shadows/borders. Tokens-only change.
  Verdict: pending review.

## Gotchas

- The site is Astro 7 (`astro@^7.4.2`); plain modern CSS lives in
  `src/styles/global.css`, with no Tailwind or other CSS framework.
- `astro.config.mjs` deliberately has no `site` URL until a domain is
  confirmed; add it before canonical/sitemap work.
- The updated (artisan) plan supersedes the original plan's app-subscription
  model: the Digital Support Hub is free and lifetime for clients. Do not
  publish subscription pricing or per-visit prices from either plan.
- The business plan targets Finger Lakes customers around Ithaca, Corning,
  Horseheads, and Elmira — safe to name as the service area.
- `README.md` is protected; update only the marked `PROJECT-DOCS` block if
  needed.
