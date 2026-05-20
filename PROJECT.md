# Project: lm4sci/lm4sci.github.io

## Summary

Academic workshop website for LM4Sci (Language Models for Science). Built with Next.js + Nextra v4 (beta, app-router-based). Site content lives in MDX files under `src/content/`. Pages include schedule, organizers, call for papers, FAQ, and an index. COLM 2026 co-located workshop: October 9, 2026, San Francisco.

## Tech Stack

- Framework: Next.js with Nextra v4 (beta, app router — not pages router)
- Content: MDX files in `src/content/`; page order controlled by `_meta.js` files
- Components: custom JSX components in `src/components/` (OrganizerCard, OrganizerGrid, Collapsible)
- Deployed via GitHub Pages using `.github/workflows/nextjs.yml`

## Agent Setup

- Sepo installed 2026-05-20 from `self-evolving/repo` v0.2.0 (PR #3)
- Existing `nextjs.yml` workflow was preserved during install
- Auth path: `oidc_broker`
- Memory initialized: 2026-05-20 (this bootstrap run)
- Rubrics: not yet initialized

## Open Questions

- PR #6 (open): year-based versioning — moves 2025 content to src/content/2025/, adds 2026 stubs; not yet merged as of 2026-05-20
