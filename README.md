# clamui-site

Public delivery repo for [clamui](https://murilo-cunha.github.io/clamui-site/) — the
source repo is private, so the landing page and the release binaries are published
from here.

- **gh-pages** — the rendered landing page, mirrored by the source repo on every
  docs change. GitHub Pages serves it.
- **Releases** — the public binaries: macOS app (dmg), VS Code extension (vsix),
  and the Tauri in-app-updater feed (`latest.json`). Published by
  `.github/workflows/publish-release.yml` whenever the source repo pushes a
  `release-staging/vX.Y.Z` branch here.
- **main** — carries the `workflow_dispatch` fallback copy of that workflow
  (the canonical copy lives in the source repo).

Nothing in this repo is edited by hand.
