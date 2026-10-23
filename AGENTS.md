# Radiant Gardens Agent Instructions

## Project Shape

- Public marketing site built with Astro 7 (`astro@^7.4.2`): pages in `src/pages/`, shared shell in `src/layouts/`, components in `src/components/`, plain CSS in `src/styles/global.css`.
- Business planning/reference documents live at the repository root.
- OKF project documentation lives in `docs/`.

## Commands

- Install: `npm install --no-audit --no-fund`
- Dev server: `npm run dev`
- Build: `npm run build` (verification gate — must pass cleanly)
- Preview built site: `npm run preview`
- Inspect state: `git status --short --branch`

## Guardrails

- Do not overwrite `README.md`; update only the marked `PROJECT-DOCS` block if needed.
- Preserve business-plan source documents when updating site copy.
- Respect the public/private content boundary in `docs/notes.md`: never publish internal financials, unconfirmed pricing, or invented contact details, testimonials, or photos.
- Never commit `node_modules/`, `dist/`, or `.astro/`.

## Validation

- Run `npm run build` after site changes; it must pass cleanly.
- Run `git status --short --branch` before and after edits.

## Docs

- Start with `docs/index.md` for the OKF documentation map.
- Update `docs/status.md` and `docs/log.md` when task state changes.
- Add non-obvious discoveries to `docs/notes.md`.
