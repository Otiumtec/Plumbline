# Changelog

Notable changes to the Plumbline studio site. Newest first.
Discipline: every behavior change updates README + this file in the same PR.

## 2026-07-26 — Vetting: docs truth + platform manifest

- **README.md** rewritten to match the repo as it actually is: real file tree
  (`card/`, `shots/`, `CNAME` were missing), live-status section
  (plumbline.toolwright.dev via GitHub Pages), correct service-worker cache name
  (`plumbline-v4`, README said `v1`), removed the stale `plumbline.studio` DNS
  walkthrough in favor of the actual domain state.
- **CLAUDE.md**: added repo scope, docs-discipline, and two-key-rule sections
  from the plumbline-template pattern (brand-architecture section preserved).
- **plumbline.json** added — `slug: plumbline`, no surfaces (static site),
  stage `active`.
- **ops/gate/run-gates.mjs** copied from plumbline-template;
  **ops/gate.workflow.yml** parked (a human must move it to
  `.github/workflows/` — the agent token cannot write there).
- No code/site behavior changed in this PR.
