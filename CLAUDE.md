# CLAUDE.md

Project context for Claude Code sessions in this repository.

## What this is

Christoffer's personal identity page. It exists mainly as a verifiable Person node in schema.org JSON-LD.

**Live:** https://orangeelefant.github.io

## Stack

Plain static HTML with inline CSS and JSON-LD. No build, no dependencies. Published by GitHub Pages from `main`.

## Layout

- `index.html`: the whole page, including the JSON-LD `@graph` (WebSite, ProfilePage, Person)
- `DESIGN.md`, `PRODUCT.md`: design tokens and product brief
- `docs/designhandbok.html`: design handbook generated from DESIGN.md
- `robots.txt`

## Commands

None. Edit the files, commit, push to `main`.

## Definition of done

1. Links checked: every client link keeps its URL and anchor text.
2. `CHANGELOG.md` has a line under `[Unreleased]`.
3. `TODO.md` reconciled.
4. Committed and pushed to `main`.

See `AGENTS.md` for the agent rules.
