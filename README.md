# Fire Motion — Meditation Fire

A calm, guided trataka (candle-gazing) flame for meditation. One page, two flame
styles you can switch between from the top-left control:

- **2.1** — a steady hand-drawn candle flame (calmer, less motion)
- **3** — a particle flame (more alive, gentle drift and sparks)

Both share the same controls (top-right): flame size, brightness, a guided
3/5/10-minute gaze session with soft chimes, and fullscreen.

## Use it on your phone (as an installed app)

This is a installable web app (PWA) — once GitHub Pages is serving it, add it
to your home screen and it opens full-screen, without browser chrome, like a
native app.

### 1. Turn on GitHub Pages (one-time)

In this repo: **Settings → Pages → Build and deployment → Source →
"GitHub Actions"**. The included workflow
(`.github/workflows/deploy-pages.yml`) then deploys the site automatically
every time `main` is updated. After the first run finishes (check the
**Actions** tab), your app is live at:

```
https://chanonchan.github.io/Fire-Motion/
```

### 2. Install it on your phone

- **Android (Chrome):** open the link above → menu (⋮) → **Add to Home
  screen** / **Install app**.
- **iPhone (Safari):** open the link above → Share icon → **Add to Home
  Screen**. (Fullscreen only works this way on iOS — Safari doesn't allow
  in-page fullscreen for regular tabs.)

Once installed, it launches like any other app, works offline (a service
worker caches the app shell), and keeps the screen awake while you practice.

## Local development

It's a static site — no build step. Open `index.html` directly, or serve the
folder with any static file server, e.g.:

```
python3 -m http.server
```

## Files

- `index.html` — the app (both flame engines, shared controls, version switch)
- `manifest.webmanifest` — PWA metadata (name, icons, standalone display)
- `sw.js` — service worker, caches the app shell for offline use
- `icons/` — app icons
- `.github/workflows/deploy-pages.yml` — auto-deploys to GitHub Pages on push to `main`
