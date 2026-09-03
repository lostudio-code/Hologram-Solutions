# Hologram Solutions — marketing site

Single-page static site. No build step, no dependencies to install.

## Files
- `index.html` — the site (deployment entry point and editable source)
- `404.html` — not-found page
- `support.js` — runtime required by both pages
- `assets/` — video, imagery, logo, icons, share card
- `manifest.webmanifest` — PWA/homescreen metadata
- `robots.txt`, `sitemap.xml` — crawler directives
- `CNAME` — custom domain for GitHub Pages
- `.nojekyll` — tells Pages to serve files as-is

## Deploy (GitHub Pages)
1. Push this folder to a repo.
2. Settings → Pages → Source: *Deploy from a branch*, branch `main`, folder `/ (root)`.
3. Custom domain: `hologramsolutions.tech` (already in `CNAME`). Point a CNAME DNS record at `<user>.github.io`, or A records at the GitHub Pages IPs for the apex domain. Enable *Enforce HTTPS*.

If the domain changes, update `CNAME`, `robots.txt`, `sitemap.xml`, and the canonical / og / twitter URLs in `index.html`.

## Local preview
Serve from the project root over HTTP — opening `index.html` from the filesystem blocks the runtime fetch.

```
python3 -m http.server 8000
```

## Editing
Both pages are plain HTML with inline styles. Edit `index.html` and `404.html` directly.

## SEO / social
Title, description, canonical, Open Graph, Twitter card, and Organization JSON-LD live in the `<head>` of `index.html`. The share image is `assets/og-card-mark-white.png` (1200×630).
