# Fresco releases

Update feed and signed archives for **Fresco**, a menu-bar macOS app that
rotates the desktop wallpaper from remote sources and local folders.

This repository holds only distribution artifacts — the application source lives
elsewhere and is private. Everything here is published automatically by Fresco's
release workflow; nothing is edited by hand.

## What's here

| Path | What it is |
|---|---|
| `appcast.xml` | The [Sparkle](https://sparkle-project.org) update feed the app polls |
| `Fresco-*.zip` | Notarized, stapled application archives |
| `Fresco-*.html` | Release notes for the matching archive |
| `old_updates/` | Archives retired from the feed by `generate_appcast` (not published) |

Served over GitHub Pages at <https://danielyan.github.io/fresco-releases/>.

## Installing

Download the newest `Fresco-*.zip`, unzip it, and move `Fresco.app` to
`/Applications`. The app updates itself after that — Fresco checks this feed on
a schedule, and on demand from **Check for Updates…** in its menu.

Builds are signed with a Developer ID certificate and notarized by Apple, and
each update is additionally signed with an EdDSA key that the app verifies
before installing anything.
