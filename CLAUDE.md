# CLAUDE.md

Project context for Claude Code sessions in this repository.

## What This Is

Christoffer Holmgren — personal site

**Live:** main

## Stack

Ren statisk HTML. Ingen byggkedja, inga beroenden. Publiceras av GitHub Pages på https://orangeelefant.github.io.

## Layout

- `index.html` — hela sidan, inklusive JSON-LD `@graph` (WebSite + ProfilePage + Person)
- `robots.txt`

## Commands

```bash
# Inga. Redigera index.html, committa, pusha — GitHub Pages publicerar.
```

## Conventions

- Match existing patterns; don't introduce new abstractions without reason.
- Keep files under 500 lines.
- Swedish copy for client-facing text unless otherwise specified.
- Secrets live in `~/.secrets` and are referenced via `${VAR}`.

## Definition of Done

A change is done when:

1. Code works (built and verified locally).
2. `CHANGELOG.md` updated under `[Unreleased]`.
3. `TODO.md` reconciled (completed items removed or ticked, follow-ups added).
4. Committed and pushed to ``.

See `AGENTS.md` for the full agent contract.
