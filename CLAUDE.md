# CLAUDE.md

Customer documentation for Avaluma, a [Mintlify](https://mintlify.com) site published at
https://docs.avaluma.ai. Pages are MDX with YAML frontmatter; navigation lives in `docs.json`.
Writing style and Mintlify tooling: [AGENTS.md](AGENTS.md).

This repository is **public** and is a git submodule of the website repo (path `docs/`). Never
commit internal hostnames, keys or customer data.

## Rules

- Bilingual: `de/` and `en/` mirror each other. Every change lands in both trees.
- A new page must be registered in `docs.json` (both languages), or it does not appear.
- Docs change together with the product: a user-facing change in the website ships with its docs
  update in the same unit of work.
- When working inside the website checkout, the submodule starts in detached HEAD: check out a
  branch here, commit and push, then commit the new submodule pointer in the website repo.

Every root-level `.md` file is published as a page unless `.mintignore` lists it. `CLAUDE.md` is
listed there; keep it that way.

## Build

entfällt – Mintlify builds the site. Local preview: `npx mint dev` in this directory, then
http://localhost:3000.

## Test

`npx mint broken-links` reports no broken links, and the changed pages render in `npx mint dev`
in both languages.

## Deploy

Merging to `main` deploys: the Mintlify GitHub app publishes `main` automatically.

## Verify

The changed pages show the new content on https://docs.avaluma.ai, in German and English.
