# Plumbline

**Live storefront: [plumblinestudio.dev](https://plumblinestudio.dev)** — Plumbline Studio solves one bounded operations problem per engagement (intake, scheduling, tracking, reporting) for small businesses and professional practices. Fixed scope, 2–4 weeks. *Build it true.*

Source for the storefront lives in [`storefront/`](storefront/) (static files, no build step; deployed via a Git-connected Cloudflare Worker — every push to `main` redeploys). Agent-readable surface: [`storefront/llms.txt`](storefront/llms.txt), JSON-LD in `storefront/index.html`, `robots.txt` + `sitemap.xml`.

---

## Portfolio (PWA)

The repo also contains the original single-page, installable portfolio for Plumbline. Static files only — no build step.

### Files (keep this structure)

```
.
├── index.html
├── manifest.webmanifest
├── sw.js
├── .nojekyll
└── icons/
    ├── icon-192.png
    ├── icon-512.png
    ├── icon-192-maskable.png
    ├── icon-512-maskable.png
    ├── apple-touch-icon.png
    └── favicon.png
```

All paths in the site are relative, so it works at a project URL
(`https://<user>.github.io/<repo>/`) without any edits.

### Updating later

The service worker caches the site for offline use. When you change any file,
bump the cache name in `sw.js` (`const CACHE = 'plumbline-v1'` → `'plumbline-v2'`)
so returning visitors get the new version instead of the cached one.

### Historical notes

The original GitHub Pages deploy instructions and the `plumbline.studio` custom-domain
DNS records that used to live here are superseded: the studio's domain is
**plumblinestudio.dev**, DNS is on Cloudflare, and the storefront deploys from this
repo automatically. See the git history of this file if you ever need the old steps.

---

Plumbline · Build it true.
