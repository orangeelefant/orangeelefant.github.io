# Changelog

All notable changes to this project are documented here. Format loosely follows [Keep a Changelog](https://keepachangelog.com/en/1.1.0/).

Every commit that changes behavior, copy, configuration, or dependencies MUST add an entry under `[Unreleased]` before being pushed.

## 2026-08-23

- **DESIGN.md tillagd** Krav enligt repo-standards. Ingen kod ändrad.

## [Unreleased]

- Ersatte bootstrap-platshållarna i `CLAUDE.md` med repots verkliga stack och layout (2026-08-13).

- Added JSON-LD structured data: connected `@graph` with `WebSite`, `ProfilePage`, and `Person` nodes (stable `@id`s, `sameAs` to GitHub/Webraketen/Rastahunden) so crawlers and LLMs can resolve the site identity (2026-06-23).
- Bootstrapped `AGENTS.md`, `CLAUDE.md`, `CHANGELOG.md`, `TODO.md` (2026-05-25).
