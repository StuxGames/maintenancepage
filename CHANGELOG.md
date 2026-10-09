# Changelog

All notable changes to the Stux.Games Maintenance Page are documented here.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.1.0/),
and this project adheres to [Semantic Versioning](https://semver.org/) (MAJOR.MINOR.PATCH).

## v1.0.3

### Changed

- The favicon follows the browser's light or dark theme: the deep icon (`icon-dark.png`) on light and the bright one (`icon-light.png`) on dark, straight from the brand's media host, so a brand colour change is just a new file there
- The logos and icons in the Markdown docs (README and the like) follow GitHub's light or dark theme, using each brand's `logo-light`/`logo-dark` and `icon-light`/`icon-dark` files

## v1.0.2

### Changed

- The favicon follows the browser's light or dark theme: the deep icon (`icon-dark.png`) on light and the bright one (`icon-light.png`) on dark, straight from the brand's media host, so a brand colour change is just a new file there
- The logos and icons in the Markdown docs (README and the like) follow GitHub's light or dark theme, using each brand's `logo-light`/`logo-dark` and `icon-light`/`icon-dark` files

## v1.0.1

### Added

- The home page's footer has a copyright line ("© 2026 Stux.Games. All rights reserved."), like the legal pages, with the years kept current automatically

### Fixed

- The legal, changelog and sitemap footers name Stux.Games in the copyright line instead of Stux.Group, and no longer say Stux.Games is operated by Stux Group Ltd: that belongs on the Imprint only, which still says it

## v1.0.0

### Added

- A "respawning shortly" maintenance page for Stux.Games games and sites, styled as a respawn screen: a looping respawn bar and a server-patch checklist on A/B/X buttons, with Live Status (status.stux.games) and Contact Us links
- Light and dark themes in Stux.Games' gold pair (`#FFBA1A` on dark, `#855D00` on light), with the matching logo for each, a pixel-dot grid and faint CRT scanlines; the theme follows the system until the toggle is used, and is remembered in `localStorage`
- Oxanium, self-hosted under `assets/fonts/` with its SIL Open Font License
- The Boring Legal Stuff hub (`/legal`) with Privacy Policy, Terms and Ethics, Cookies Policy, Imprint, Disclaimer and Opt-Out Preferences, a changelog page that renders this file (sections sorted Added, Changed, Fixed, Removed, Security, Deprecated), a themed 404 page, and `/sitemap/` + `sitemap.xml` + `robots.txt`
- Footer with the Stux.Games logo, "Every Stux.Games Game" (games.stux.games) and "Created with love / code / coffee by Stux.Games"
- `dev-server.sh` / `dev-server.bat`: PHP 7.4's built-in server with a router that serves the folder like GitHub Pages, with DEV_MODE on by default (dev banner, `?banner=` previews) and `--no-dev-mode` to render as production
- GitHub Actions: Pages deployment, plus CI that validates `index.html` and lints the Markdown
- `README.md`, `CONTRIBUTING.md`, `VERSION.md` and `commit.sh` / `commit.bat`
