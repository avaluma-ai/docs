# AGENTS.md

How to write pages for the Avaluma customer docs. Repository rules (public repo, `docs.json`,
preview, deploy): [CLAUDE.md](CLAUDE.md).

## Content boundaries

- Document only what a customer sees and can set in the Studio on avaluma.ai. Check every
  statement against the product code in the website repo
  ([avaluma-website-v2](https://github.com/avaluma-ai/avaluma-website-v2)) before writing it.
- Leave out what only Avaluma staff see (the internal view, `isEmployee`, `/studio/internal`)
  and anything behind a feature flag or not yet on the website's `main`.
- Link instead of repeating: when another page already explains a step, link to it.

## Languages

- `de/` and `en/` mirror each other: same pages, same sections in the same order.
- German addresses the reader as "du", English as "you".
- Internal links carry the language prefix (`/de/...`, `/en/...`). Anchors are the heading in
  lower case with hyphens; encode umlauts (`#agent-%C3%BCbertragen`).

## Wording

- UI elements are bold and use the exact label the Studio shows in that language. The labels
  live in `src/lib/i18n/translations.ts` of the website repo.
- Code formatting for file names, paths, parameters, IDs and commands.
- Terms: **Agent** (de plural "Agenten"), **Avatar**, `.hvia` file, Avatar ID, Agent ID,
  **Studio** for the logged-in area under `avaluma.ai/studio`, **Plan** for the subscription.
  In German prose "Lizenzschlüssel", as a UI label **Lizenz-Schlüssel**.
- Short sentences, one idea each. Headings in sentence case.

## Page format

- Frontmatter with `title`, `sidebarTitle` and `description`.
- Mintlify components in use: `Steps`/`Step`, `Note`, `Tip`, `Warning`, `CardGroup`/`Card`,
  `CodeGroup`. Icons come from Lucide (`docs.json`). Component reference:
  https://mintlify.com/docs.
