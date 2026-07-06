---
type: Architecture
title: Architecture
description: Runtime shape and key files for Radiant Gardens.
tags: [architecture, static-site, marketing]
timestamp: 2026-07-06T00:00:00Z
---

# Architecture

## Runtime Shape

- `index.html` is a dependency-free static landing page.
- CSS is embedded in the page.
- No JavaScript build step, package manager, or application server is present.

## Key Files

| Path | Role |
| --- | --- |
| `index.html` | Public marketing page for Radiant Gardens. |
| `radiant-gardens-business-plan.md` | Detailed 2025-2027 business plan. |
| `updated-business-plan.md` | Updated business-plan reference material. |
| `docs/` | OKF-style project documentation. |

## Data Flow

Visitors load the static HTML directly from the host. Site copy should be checked against the business-plan documents before major content changes.
