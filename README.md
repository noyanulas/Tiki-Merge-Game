# 🍹 Tiki Merge

A relaxing, tropical **cocktail merge game** that runs **fully offline** on an iPhone — built so my girlfriend has something to play during long lectures with no signal.

It's a single self‑contained web page (HTML5 canvas + vanilla JavaScript). No servers, no accounts, no tracking, no dependencies. Once it's loaded once, it lives on the phone and works with zero internet.

> Replace the bracketed bits below (`<…>`) with your own link / username.

**▶ Play:** `<https://gentle-kringle-f638e7.netlify.app/>`

---

## How to play

Serve cocktails up the bar. When two **matching** drinks touch, they **merge** into the next, fancier glass — all the way from a humble Lemon Fizz up to the legendary Tiki Royale.

- **Drag** anywhere to aim, **release** to serve.
- Desktop: **← / →** to aim, **Space** to serve.
- Fill the **To‑Go Order** on the hanging sign for big tips.
- Chain merges quickly for a **combo multiplier**.
- Tap **⇄ Swap** to trade your current drink for the next one.
- Don't let the glasses pile back past the **dashed line**.

**The 8 tiers:** Lemon Fizz → Cranberry → Sunset → Mojito → Blue Lagoon → Grape Punch → Pink Lady → **Tiki Royale**.

---

## Why it works offline

The page registers a **service worker** (`sw.js`) that caches the whole game on the first visit. After that, every launch is served from the phone's cache, so it runs with no connection. A **web app manifest** (`manifest.webmanifest`) + Apple meta tags make it install to the home screen and open fullscreen like a native app.

**The only requirement:** open it online **once** so it can cache itself. After that, no internet is ever needed.

---

## Add it to an iPhone home screen (for offline play)

1. Open the live URL in **Safari** while you have Wi‑Fi.
2. Tap **Share** → **Add to Home Screen**.
3. Launch it from the new icon. It now runs fullscreen and offline.

It stays cached as long as it's opened every so often — daily use keeps it permanently. If you want a copy that can *never* expire, you can also open `index.html` inside the free **Documents by Readdle** app, which runs it locally with no hosting at all.

---

## Deploy

### Option 1 — Netlify Drop (fastest)

Drag this **whole folder** onto [app.netlify.com/drop](https://app.netlify.com/drop). You get a live URL instantly.

### Option 2 — GitHub Pages

1. Create a repo and push these files to the root (or a subfolder).
2. **Settings → Pages → Build and deployment → Deploy from a branch**, pick `main` / `/ (root)`.
3. Your site goes live at `https://<your-username>.github.io/<repo>/`.

Relative paths are used throughout, so the service worker and manifest work correctly even under the `/<repo>/` subpath.

> If you change files and redeploy, bump the `CACHE` version string in `sw.js` (e.g. `tiki-merge-v1` → `v2`) so phones pick up the new version instead of the cached old one.

---

## What's in this folder

| File | Purpose |
|------|---------|
| `index.html` | The entire game (canvas, physics, art, audio — all inline). |
| `sw.js` | Service worker — caches everything for offline play. |
| `manifest.webmanifest` | App name, colors, icons, fullscreen settings. |
| `icon-180/192/512.png` | Home‑screen / app icons. |
| `IDEAS.md` | Roadmap of more games to add. |

---

## Tech notes

- Pure **HTML5 `<canvas>`** + vanilla JS in one file. No frameworks, no build step.
- Custom lightweight **2D physics** (gravity, collision relaxation, contact‑merging).
- Every glass, garnish, torch, and the table are **drawn procedurally** — the only raster asset is the app icon.
- Best score persists via `localStorage`.
- Tuned for a portrait phone screen with safe‑area (notch) insets.

---

## Roadmap

This is meant to grow into a small **offline arcade** — one home‑screen icon, several games behind a menu. See **[IDEAS.md](IDEAS.md)** for the full list and build notes.

---

Made with love. 🌴
