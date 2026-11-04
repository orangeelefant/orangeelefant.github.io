# AGENTS.md

Instructions for automation agents (Claude Code, Codex and similar) working in this repository.

## Repository

- **Name:** `orangeelefant/orangeelefant.github.io`
- **Purpose:** Christoffer's personal identity page, published by GitHub Pages.
- **Live:** https://orangeelefant.github.io

## Rules

- Read `CLAUDE.md` and `TODO.md` before changing anything.
- Push directly to `main`. One logical change per commit.
- Never commit credentials. Reference secrets through environment variables.
- Every existing link to a client site keeps its URL and anchor text. The Webraketen backlink engine counts them.
- Public copy is Swedish unless the file is already in English.
- Add a line under `## [Unreleased]` in `CHANGELOG.md` for every change to content or configuration.
- Follow `DESIGN.md` and `PRODUCT.md` for any change to `index.html`.
