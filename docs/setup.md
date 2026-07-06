---
type: Setup
title: Setup
description: Local editing and validation notes for Radiant Gardens.
tags: [setup, static-site]
timestamp: 2026-07-06T00:00:00Z
---

# Setup

## Requirements

- A browser for previewing `index.html`.
- Git for version control.

## Local Preview

Open `index.html` directly in a browser, or serve the folder with any local static file server.

## Validation

No dependency install is required. Lightweight checks:

```bash
git status --short --branch
git diff --check
```

For content changes, inspect the rendered page manually on desktop and mobile widths.
