<p align="center">
  <picture><source media="(prefers-color-scheme: dark)" srcset="https://global.media.stux.games/logo-light.png"><source media="(prefers-color-scheme: light)" srcset="https://global.media.stux.games/logo-dark.png"><img src="https://global.media.stux.games/logo-dark.png" height="80" alt="Stux.Games Logo"></picture>
</p>

# Contributing to Maintenance Page

This document is for anyone working on the maintenancepage.stux.games page itself.

## Local setup

There's no build step or dependencies. Run `./dev-server.sh [port] [--no-dev-mode]` (or
`dev-server.bat` on Windows) and open `http://127.0.0.1:8000`. DEV_MODE is on by default: the
dev router answers `/assets/dev-mode.js` with `window.SITE_DEV_MODE = true`, so every page shows
the dev banner. `--no-dev-mode` renders exactly as production does. The server needs PHP 7.4
(`$PHP_BIN`, `php74`, or `%LOCALAPPDATA%\Programs\PHP\7.4\php.exe`).

## Project conventions

- Static HTML pages (`index.html`, `legal.html` + `legal/`, `changelog.html`, `404.html`, `sitemap/`): no framework, no build step, no backend.
- Each page's styles are inline in its `<style>` block, built on the same tokens: `--accent` is `#FFBA1A` on dark and `#855D00` on light. Don't hard-code colours outside the theme blocks.
- The Stux.Games twist on this page is the respawn screen (respawn bar, A/B/X patch checklist). Keep it playful but readable, and keep every animation behind the `prefers-reduced-motion` rule.
- Oxanium is self-hosted under `assets/fonts/` (weights 300 to 600), not pulled from a third-party CDN.
- The sitemap (`sitemap.xml`, `sitemap/index.html`, `robots.txt`) is generated: after adding or removing a page, edit `PAGES` in `scripts/build-sitemap.py` and run `python scripts/build-sitemap.py`, then commit the result.
- `changelog.html` fetches and renders `CHANGELOG.md` at runtime, sorting sections into Added, Changed, Fixed, Removed, Security, Deprecated. Don't hand-copy changelog content into it.
- General contact uses `hello@stux.games`; legal contact uses `legal@stux.games`.

## Versioning and changelog

- The version lives in `VERSION.md` (a bare version string). Bump it on every release, following [Semantic Versioning](https://semver.org/).
- Every release gets a `CHANGELOG.md` entry with `### Added` / `### Changed` / `### Fixed` / `### Removed` / `### Security` / `### Deprecated` subsections, in that order.
- `commit.sh` (bash) and `commit.bat` (Windows) read `VERSION.md` to commit and tag a release.

## Before committing

- Open the page in both themes, and at phone, tablet and desktop widths.
- CI runs `html-validate` on `index.html` and `markdownlint` on every Markdown file.
