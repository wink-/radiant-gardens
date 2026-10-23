---
type: Architecture
title: Architecture
description: Runtime shape and key files for the Radiant Gardens Astro site.
tags: [architecture, astro, static-site, marketing]
status: current
generated:
  by: Astro rebuild agent (OpenCode)
  at: 2026-10-23T16:17:32Z
---

# Architecture

## Runtime Shape

- The public site is a static [Astro](https://astro.build) 7 project (`astro@^7.4.2`), the only runtime dependency.
- Pages are pre-rendered to static HTML in `dist/` by `npm run build`; no server, database, or client framework is involved.
- Styling is a single plain-CSS file (`src/styles/global.css`) with CSS custom properties; no Tailwind or CSS framework.
- Fonts (Fraunces for headings, Work Sans for body) load from Google Fonts at runtime, with serif/sans fallbacks; no font build step.
- `astro.config.mjs` intentionally sets no `site` URL: no production domain has been confirmed.

## Page Inventory

| Route | Source | Purpose |
| --- | --- | --- |
| `/` | `src/pages/index.astro` | Hero/mission, services overview, three differentiators, process teaser, service-area note. |
| `/services/` | `src/pages/services.astro` | Detail sections: design, build, planting/coaching, Digital Support Hub; a-la-carte care. |
| `/process/` | `src/pages/process.astro` | Engagement steps: consult, design, build, first harvest & beyond. |
| `/about/` | `src/pages/about.astro` | Founder-led craftsmanship story (the founder is not named). |
| `/contact/` | `src/pages/contact.astro` | Honest in-planning state with visibly marked contact placeholders. |
| `/404` | `src/pages/404.astro` | Not-found page. |

## Key Files

| Path | Role |
| --- | --- |
| `src/layouts/BaseLayout.astro` | Shared HTML shell: banner, header, skip link, footer, fonts, meta. |
| `src/components/*.astro` | Site header/footer, planning banner, botanical SVG art, icon set, JSON-LD. |
| `src/styles/global.css` | Design system: sage/cream/terracotta palette, type, components. |
| `public/favicon.svg` | Leaf favicon. |
| `radiant-gardens-business-plan.md` | Original 2025-2027 business plan (reference only; never published as-is). |
| `updated-business-plan.md` | Updated artisan-model business plan (reference only). |
| `docs/` | OKF-style project documentation. |

## Data Flow

- Content is authored directly in `.astro` page templates; there is no CMS or data layer.
- `npm run build` outputs static files to `dist/` (git-ignored), deployable to any static host.
- A schema.org `LocalBusiness` JSON-LD block appears on the homepage with only true fields (name, description, `areaServed`: Finger Lakes region).
- Public copy must be derived from the business-plan documents under the public/private content boundary documented in `notes.md`.
