# FLauncher Wallpapers

Curated wallpaper repository for [FLauncher](https://github.com/cmcuriqueo/FLauncher),
an open-source Android TV launcher.

## How it works

The app fetches `manifest.json` from the default branch:

```
https://raw.githubusercontent.com/cmcuriqueo/flauncher-wallpapers/main/manifest.json
```

Each entry points to an image in `wallpapers/`, served via
`raw.githubusercontent.com`. No API key required.

## Manifest format

```json
{
  "version": 1,
  "wallpapers": [
    { "name": "Abstract", "file": "wallpapers/abstract.png", "category": "abstract" }
  ]
}
```

## Adding a wallpaper

1. Add a 16:9 image (PNG or JPG) to `wallpapers/`. Keep files reasonably small
   (< 500 KB) so downloads are fast on TV hardware.
2. Add an entry to `manifest.json`.
3. Commit and push to `main` — the app picks it up on the next fetch.
