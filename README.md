<p align="center">
  <picture><source media="(prefers-color-scheme: dark)" srcset="https://global.media.stux.games/logo-light.png"><source media="(prefers-color-scheme: light)" srcset="https://global.media.stux.games/logo-dark.png"><img src="https://global.media.stux.games/logo-dark.png" height="100" alt="Stux.Games Logo"></picture>
</p>

# Maintenance Page

The maintenance page for Stux.Games games and sites that are temporarily down.

## Overview

It's shown while a Stux.Games game or site is down for maintenance. It's styled as a respawn screen: a looping respawn bar and a server-patch checklist on A/B/X buttons, with links to the live status page (status.stux.games) and a way to get in touch.

It's a static site on GitHub Pages at [maintenancepage.stux.games](https://maintenancepage.stux.games): no framework, no build step and no backend. It comes with the Boring Legal Stuff pages (`/legal`), a changelog page (`/changelog`), a sitemap (`/sitemap/`, `sitemap.xml`) and a themed 404 page, in light and dark themes.

## Features

- 🎮 Stux.Games' gold pair (`#FFBA1A` on dark, `#855D00` on light) on a pixel-dot grid with faint CRT scanlines
- 🌗 Light and dark themes: follows the system, with a toggle that remembers the choice
- 🔤 Oxanium, self-hosted under `assets/fonts/` (SIL Open Font License)
- 📱 Responsive, and animations stop for visitors who prefer reduced motion
- ⚖️ Privacy Policy, Terms and Ethics, Cookies Policy, Imprint, Disclaimer and Opt-Out Preferences

## Local development

```bash
./dev-server.sh            # http://127.0.0.1:8000, DEV_MODE on (dev banner)
./dev-server.sh 8080       # another port
./dev-server.sh --no-dev-mode   # exactly as production renders
```

On Windows use `dev-server.bat` with the same arguments. The server is PHP 7.4's built-in
server with `.github/dev-router.php`, which serves the folder the way GitHub Pages does.
With DEV_MODE on, `?banner=soon,maintenance,site` previews the other banner types.

## Releasing

Update `CHANGELOG.md`, bump `VERSION.md`, then run `./commit.sh "Release message"` (or
`commit.bat`), which commits and tags `vX.Y.Z` from `VERSION.md`. Pushing to `main` deploys
through `.github/workflows/pages.yml`.

## Copyright

Copyright © 2026 Stux.Group. All rights reserved. Oxanium is © The Oxanium Project Authors,
under the SIL Open Font License (`assets/fonts/OFL.txt`).

---

*Built & Maintained by <picture><source media="(prefers-color-scheme: dark)" srcset="https://global.media.stux.games/icon-light.png"><source media="(prefers-color-scheme: light)" srcset="https://global.media.stux.games/icon-dark.png"><img src="https://global.media.stux.games/icon-dark.png" height="14" alt="Stux.Games" valign="middle"></picture> [Stux.Games](https://github.com/StuxGames), Hosted by <img src="https://github.com/Stuxedo.png" height="14" alt="Stuxedo" valign="middle"> [Stuxedo](https://stuxedo.com).
Stux.Games is a part of the <picture><source media="(prefers-color-scheme: dark)" srcset="https://global.media.stux.group/icon-light.png"><source media="(prefers-color-scheme: light)" srcset="https://global.media.stux.group/icon-dark.png"><img src="https://global.media.stux.group/icon-dark.png" height="14" alt="Stux.Group" valign="middle"></picture> Stux.Group brand of businesses.*
