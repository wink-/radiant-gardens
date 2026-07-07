# Radiant Gardens Agent Instructions

## Project Shape

- Static single-page marketing site in `index.html`.
- Business planning/reference documents live at the repository root.
- OKF project documentation lives in `docs/`.

## Commands

- Preview: open `index.html` directly in a browser or serve the folder with a static file server.
- Validate docs/static edits: `git diff --check`.
- Inspect state: `git status --short --branch`.

## Guardrails

- Do not overwrite `README.md`; update only the marked `PROJECT-DOCS` block if needed.
- Keep the static site dependency-free unless a concrete build need is introduced.
- Preserve business-plan source documents when updating site copy.

## Validation

- Run `git status --short --branch` before and after edits.
- For HTML-only changes, validate with lightweight text checks and inspect changed files; no dependency install is required.

## Docs

- Start with `docs/index.md` for the OKF documentation map.
- Update `docs/status.md` and `docs/log.md` when task state changes.
- Add non-obvious discoveries to `docs/notes.md`.
