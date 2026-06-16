# Popcorn — Website

Marketing and privacy site for **Popcorn**, the movies & TV app for iPhone, iPad, Mac and Apple Vision Pro.

🔗 <https://popcorn.adam-young.co.uk>

## Pages

| Page | File |
|------|------|
| Marketing / home | [`index.html`](index.html) |
| Privacy Policy | [`privacy.html`](privacy.html) |

## Stack

A dependency-free static site — plain HTML and a single CSS file. No build step.

- `styles.css` — design system driven by CSS custom properties, with automatic light/dark mode (`prefers-color-scheme`) and the `#419AFF` brand accent.
- `assets/` — the app icon and favicons.

## Local preview

Open `index.html` directly in a browser, or serve the folder:

```sh
python3 -m http.server 8000
# then visit http://localhost:8000
```

## Deploy

Static hosting from the repo root (e.g. GitHub Pages, Cloudflare Pages, Netlify). Point the `popcorn.adam-young.co.uk` subdomain at the host.

---

© 2026 Adam Young. This product uses the TMDb API but is not endorsed or certified by TMDb.
