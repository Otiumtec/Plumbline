# Plumbline — studio site (PWA)

The public site for **Plumbline Studio** — the parent brand behind Toolwright and
the studio's other doors. A single-page, installable PWA served by GitHub Pages,
live at **https://plumbline.toolwright.dev**.

Static files only — hand-written HTML/CSS/vanilla JS, no framework, no build
step, no dependencies. The animated background is a self-contained particle-life
engine ported from the Toolwright app.

## Status

**Live** at https://plumbline.toolwright.dev (GitHub Pages, `main` branch,
`/ (root)`, custom domain via the `CNAME` file). This repo is public — treat
every commit as brand-visible.

## What's actually here

```
.
├── index.html            # the whole site: content, styles, particle field, SW registration
├── card/                 # digital business card at /card/ (own page + OG image + QR regen script)
├── shots/                # screenshots used by the "Selected projects" grid
├── icons/                # PWA icons, maskable variants, favicon, apple-touch-icon
├── manifest.webmanifest  # installability metadata
├── sw.js                 # cache-first service worker (cache name: plumbline-v4)
├── CNAME                 # plumbline.toolwright.dev
├── .nojekyll             # keep GitHub Pages from running Jekyll
├── plumbline.json        # platform manifest — surfaces + stage
└── ops/                  # Plumbline gate runner + parked workflow (see ops/gate.workflow.yml)
```

All paths are relative, so the site also works at a project URL without edits.

## Run locally

No toolchain needed:

```bash
python3 -m http.server 8000   # then open http://localhost:8000
```

(Use a local server rather than `file://` — the service worker needs HTTP.)

## Updating the site

The service worker caches the site for offline use. When you change any cached
file, **bump the cache name in `sw.js`** (currently `plumbline-v4` → `plumbline-v5`)
so returning visitors get the new version.

Project links on the page point at preview deployments (Vercel / Cloudflare /
Netlify), mostly running mock data — the page says so; keep that honesty when
editing cards.

## Domain

Served at `plumbline.toolwright.dev` (the `CNAME` file is the single source of
truth). If the domain strategy changes (e.g. a future `plumbline.studio`),
update `CNAME`, DNS, and this section together.

---

Plumbline Studio · Build it true.
