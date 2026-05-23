# Memory

## Durable

- Site uses Nextra v4 (beta, app router); new content pages go in `src/content/` as `.mdx` files; page order set via `_meta.js` in the same directory.
- The repo has an existing `.github/workflows/nextjs.yml` that handles GitHub Pages deployment — do not overwrite or conflict with it.
- Sepo installed 2026-05-20 from v0.2.0; no rubrics branch initialized yet.
- Content is year-versioned: src/content/2025/ (archived) and src/content/2026/ (current default); links use /docs/YYYY/… paths. Add new editions as src/content/YYYY/.
- MDX files under src/content/YYYY/ import components with '../../components/…' (two levels up to reach src/components/); update on any directory restructure.
- nextjs.yml cache key must include **/*.mdx; omitting it lets stale .next/cache survive MDX restructures and causes module-not-found errors in CI.
- Cross-edition sidebar nav lives in the current year's _meta.js: add a 'separator' + link entry pointing to prior editions when a new year goes live.
