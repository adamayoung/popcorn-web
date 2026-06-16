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

Deployed to **Cloudflare Pages** automatically on every push to `main` via
[`.github/workflows/deploy.yml`](.github/workflows/deploy.yml). The workflow
copies the publishable files into `dist/` and uploads them with Wrangler.

### One-time setup

1. **Create the Pages project** (direct-upload, production branch `main`):
   ```sh
   wrangler pages project create popcorn-web --production-branch=main
   ```
2. **Add repo secrets** (Settings → Secrets and variables → Actions):
   - `CLOUDFLARE_API_TOKEN` — token with the *Cloudflare Pages: Edit* permission
   - `CLOUDFLARE_ACCOUNT_ID` — your Cloudflare account ID
3. **Add the custom domain** `popcorn.adam-young.co.uk` to the Pages project
   (Pages → popcorn-web → Custom domains).

The project name is set in the workflow (`--project-name=popcorn-web`); change it
there if you name the Pages project differently.

---

© 2026 Adam Young. This product uses the TMDb API but is not endorsed or certified by TMDb.
