---
type: Setup
title: Setup
description: Install, develop, build, and verify the Radiant Gardens Astro site.
tags: [setup, astro, build]
status: current
generated:
  by: Astro rebuild agent (OpenCode)
  at: 2026-10-23T16:17:32Z
---

# Setup

## Requirements

- Node.js 20+ and npm (Astro 7 requirement).
- Git for version control.

## Install

```bash
npm install --no-audit --no-fund
```

## Develop / build / preview

```bash
npm run dev       # local dev server
npm run build     # static build to dist/ — the verification gate
npm run preview   # serve the built site locally
```

## Validation

```bash
npm run build
git status --short --branch
git diff --check
```

`npm run build` must pass cleanly after any site change; it is the documented
verification command for this repo.

## Notes

- No environment variables or API keys are needed; the site is fully static.
- No `site` URL is configured in `astro.config.mjs` until a production domain is confirmed.
- `node_modules/`, `dist/`, and `.astro/` are git-ignored and must never be committed.
