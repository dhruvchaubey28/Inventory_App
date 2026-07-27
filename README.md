# 🪵 Mango Stock Book

A mobile-first PWA for mango timber traders to track wood stock in CFT (cubic feet).
Built for one-handed use on a phone — no app store, no account, no internet required after first load.

## Features

- **Purchase / Sale entries** with thickness, length group, quantity, rate, party name
- **Stock matrix** — see CFT in hand broken down by thickness × length at a glance
- **Average cost tracking** and gross profit calculation
- **CFT calculator** — work out quantity from pieces × width × length
- **CSV backup** — copy to WhatsApp or email anytime
- **Installable PWA** — works like a native app on Android and iPhone
- **Offline support** — works without internet after first load
- **All data stays on your phone** — nothing is sent to any server

## Tech

Plain HTML + CSS + JS, no frameworks, no build step. Data stored in `localStorage`.

## Deployment

Hosted on [Netlify](https://netlify.com) free tier. Auto-deploys on every push to `main`.

## Installing on your phone

**Android (Chrome):**
Open the site → tap the install banner or use Chrome menu → *Add to Home Screen*

**iPhone (Safari only):**
Open the site in Safari → tap the Share button (□↑) → *Add to Home Screen*

> Chrome on iPhone does not support PWA install — must use Safari.

## Data & Backup

Data lives in your phone's browser storage (`localStorage`). It is **not** backed up to any server.

- To back up: tap **⋯** menu → **Copy backup** → paste into WhatsApp or email
- To move to a new phone: take a CSV backup first, then manually re-enter or keep the backup for reference

## File Structure

```
index.html      Main app (all HTML, CSS, JS in one file)
manifest.json   PWA manifest (app name, icons, display mode)
sw.js           Service worker (offline caching)
icon-192.png    App icon — 192×192
icon-512.png    App icon — 512×512
```

## Local Development

No build tools needed. Just open `index.html` in a browser, or use VS Code Live Server for best results.

```bash
# With Python
python3 -m http.server 8080
# Then open http://localhost:8080
```
