# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## What this is

Static QA portfolio site for Eduardo Gallifa, served via **GitHub Pages**. Pure HTML/CSS/JS — there is **no build step, no package.json, no bundler, and no dependencies to install**. Edit the HTML files directly; preview by opening them in a browser or with any static server (e.g. `python -m http.server`).

`.nojekyll` disables Jekyll processing so files are served as-is.

## Architecture

Three hand-written pages share an inline design system (CSS custom properties in `:root`, with a `@media (prefers-color-scheme: dark)` override). Accent color `#06b6d4` / `#22d3ee`, Inter font from Google Fonts.

- **`index.html`** — landing page. Hero + a `.grid` of `.card` project entries. Each card links to `project.html` with query params (see below) and references a screenshot in `assets/`. Also contains the image lightbox.
- **`project.html`** — generic README viewer. Reads `?repo=owner/name&title=...&return=...` from the URL, then client-side fetches the project's README from `raw.githubusercontent.com`, renders it with **marked** + sanitizes with **DOMPurify** (both loaded from CDN). It probes multiple branches (`main`, `master`, `dev`, `gh-pages`) and filename variants, and rewrites relative image/link URLs to absolute GitHub URLs. No README content is stored in this repo — it is fetched live.
- **`contact.html`** — contact page.

**Adding/editing a project card:** duplicate an existing `<article class="card">` block in `index.html`. The link URL is `project.html?repo=eduardogallifaochoa/<repo>&title=<URL-encoded>&return=index.html`. Add the screenshot to `assets/` and reference it from the card.

## Submodules

The actual project code lives in **git submodules** under `projects/` (defined in `.gitmodules`), each pointing at a separate GitHub repo. This portfolio repo only pins commit references — it does not contain that source. Note the site fetches READMEs live from GitHub at runtime, so the submodules are not required for the site to function; they exist to vendor the pinned references.

- Init/update locally: `git submodule update --init --recursive`
- Submodules are bumped automatically every Monday by `.github/workflows/update-submodules.yml` (`git submodule update --remote --merge`, commit, push to `main`).

## CI

- `update-submodules.yml` — weekly submodule bump (cron + manual).
- `readme-check.yml` / `readme-link-check.yml` — run lychee link checking on `README.md`, `index.html`, and `docs/` on push.

There is no test suite in this repo. When changing links, expect the lychee workflows to validate them.
