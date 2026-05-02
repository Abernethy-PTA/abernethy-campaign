# Abernethy Century Campaign

Static site for the Abernethy Elementary campus beautification fundraiser.

Single `index.html`, no build step. Auto-deploys to GitHub Pages on push to `main` (`.github/workflows/pages.yml`).

## Local preview

```
python3 -m http.server 8000
```

Open http://localhost:8000.

## Deploy

Target: `give.supportabernethy.org`

1. Push to `main` — Pages workflow publishes the site.
2. In repo Settings → Pages, set the custom domain to `give.supportabernethy.org` (writes a `CNAME` file).
3. At the DNS provider for `supportabernethy.org`, add a `CNAME` record:
   - Name: `give`
   - Value: `<github-username>.github.io`
4. Enable "Enforce HTTPS" once the cert provisions.

## Structure

- `index.html` — full page (inline CSS)
- `images/`, `Abernethy Website Images/` — photography
- `Abernethy Campaign Canva Files/` — source design files
- `favicon.svg`
