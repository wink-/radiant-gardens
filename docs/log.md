# Log

## 2026-10-24

- Added the `mockups/` design-mockup workflow, plain static HTML outside the Astro build: a dark gallery (`mockups/index.html`), a faithful homepage baseline (`mockups/current/`), and the first variant (`mockups/2026-10-24-linen/` — "linen", a lighter/softer tokens-only direction).
- Documented the mockup rules in `mockups/README.md` and `docs/notes.md`: one variable at a time, dated variant folders, the real `src/styles/global.css` linked and overridden only via `variant.css`, identical markup, real content only, promotion via `design/<name>` branch → PR, verdicts recorded in `docs/notes.md`.
- No production files changed; the Astro build is unaffected.

## 2026-10-23

- Rebuilt the site as a modern Astro 7 project on branch `feature/astro-rebuild`; the superseded placeholder `index.html` was removed.
- Added the first real pages: home, services, process, about, contact (honest in-planning state with `[to be announced]` placeholders), and 404, styled with a sage/cream/terracotta botanical design system in plain CSS.
- Added a site-wide "In planning — launching 2026" banner and a homepage LocalBusiness JSON-LD block limited to true fields.
- Recorded the public/private content boundary rule in `notes.md` (no internal financials, no invented contact details or social proof).
- Updated OKF docs (architecture, setup, status, notes, index) and repo agent instructions for the new stack.
- `npm run build` passes cleanly on the feature branch.

## 2026-07-07

- Refined OKF documentation format, repo agent command guidance, and status resume details.

## 2026-07-06

- Added repo-specific agent instructions.
- Added OKF documentation scaffold for architecture, setup, status, notes, and log.
- Linked project docs from the README in a marked `PROJECT-DOCS` block.
- 2026-10-23 — Documented intentional standalone status: not a Streetcats publication destination, not a content-platform theme.
