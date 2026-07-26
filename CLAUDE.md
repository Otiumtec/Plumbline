# Plumbline

## Plumbline Brand Architecture (canonical)

**Plumbline Studio** is the parent company and the "build it true" philosophy, and the
services arm for established businesses. Its products are separate doors under it:
- **Toolwright** — startups & individuals; the entry point; seminars on building with AI (toolwright.dev)
- **Old World Trade** — artisans
- **Breakpoint** — churches
- *(TBD)* — healthcare / chronic-illness

There is NO "Tool Maker" master brand above Plumbline — Plumbline is the top.
Philosophy through-line: build true, well-made tools that should exist, for people
already worthy of their path; meet people where they are. Grow one product at a time
(Pieter Levels model): one live and earning before the next.
**This repo's place:** Plumbline Studio — the parent company brand and site.

## Scope of this repo

A public, static, no-build PWA (see README). No app code, no secrets, no user
data. It is live at plumbline.toolwright.dev — every merged change is
immediately brand-visible. Keep tone professional; no placeholder copy on `main`.

## Docs discipline (platform rule — keep in every project)

- Update `README.md` and `CHANGELOG.md` in the same PR as every behavior change.
  The README describes what exists, not what's planned.
- `plumbline.json` declares this repo's surfaces (`auth`, `payments`, `webhooks`,
  `realtime`, `pii`) and stage. Adding a capability = updating the manifest in the same PR.
- Verify before push: open the site locally and click through before any push.
  If your environment can't verify, say so in the PR.
- Secrets live in env, never in code — and never reproduce credential values in
  code, docs, commits, or PR bodies.

## Two-key rule

Agents working unattended **open PRs and never merge**. Every merge has a human
behind it. Never push to `main`. Never create or modify files under
`.github/workflows/` — parked workflow copies live at `ops/*.workflow.yml` for a
human to move.

## Loose ends (from the Plumbline dashboard)

At session start, list the open GitHub issues labeled `loose-end` on this repo and offer to pick one up. These are notes Kyle captured from dashboard.toolwright.dev — the context for each lives in the issue body. When one is finished, close the issue.
