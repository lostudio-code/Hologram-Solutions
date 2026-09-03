# Hologram Solutions — marketing site

Single-page static site. No build step.

## Files
- `index.html` — the site (deployment entry point, and the editable source)
- `404.html` — not-found page
- `support.js` — runtime required by the page
- `assets/` — video, imagery, logo, icons, share card
- `manifest.webmanifest`, `robots.txt`, `sitemap.xml`, `CNAME`, `.nojekyll`

## Deploy (GitHub Pages)
1. Push this folder to a repo.
2. Settings → Pages → Source: *Deploy from a branch*, branch `main`, folder `/ (root)`.
3. Custom domain: `hologramsolutions.tech` (already in `CNAME`) — point a CNAME DNS record at `<user>.github.io`, or A records at GitHub Pages IPs for the apex domain. Enable *Enforce HTTPS*.

If the domain changes, update: `CNAME`, `robots.txt`, `sitemap.xml`, and the canonical/og/twitter URLs in `index.html`.

## Editing
Edit `index.html` directly. Edit `404.html` directly.
