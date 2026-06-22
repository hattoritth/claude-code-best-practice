# Lessons

Use this file for durable failure records, changed judgments, and recurrence
prevention notes that should shape future repository work.

## Entry Format

```md
## YYYY-MM-DD - Short Title

- Context:
- Mistake or changed judgment:
- Prevention:
- Related files:
```

## 2026-06-22 - Do Not Mirror Seven Claude Files By Default

- Context: Evaluated a proposed seven-file Claude Code structure:
  `CLAUDE.md`, `persona.md`, `lessons.md`, `references.md`, `ng-rules.md`,
  `output-format.md`, and `glossary.md`.
- Mistake or changed judgment: Creating all seven files would duplicate this
  repository's existing `CLAUDE.md`, `.claude/rules/`, `README.md`,
  `best-practice/`, `reports/`, `tips/`, and `videos/` structure.
- Prevention: Add only files with a distinct role. Keep Claude entrypoint
  guidance in `CLAUDE.md`, cross-agent repository rules in `AGENTS.md`,
  durable failure records here, Markdown output rules in
  `.claude/rules/markdown-docs.md`, and source-backed references in the
  existing documentation directories.
- Related files: `AGENTS.md`, `CLAUDE.md`, `.claude/rules/markdown-docs.md`
