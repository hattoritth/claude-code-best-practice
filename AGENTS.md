# AGENTS.md

This repository is a reference implementation for Claude Code configuration and
best practices. Keep repository guidance focused on where knowledge belongs, not
on duplicating Claude Code documentation.

## Source Of Truth

- Treat the GitHub private repository as the source of truth.
- Preserve the existing `CLAUDE.md` entrypoint for Claude Code behavior.
- Keep new shared rules small. Prefer updating the nearest existing document
  before creating a new top-level file.

## Where To Put Things

| Need | Location |
|------|----------|
| Claude Code entrypoint and repo-wide workflow notes | `CLAUDE.md` |
| Codex or cross-agent repository rules | `AGENTS.md` |
| Failure records, changed judgments, and recurrence prevention | `tasks/lessons.md` |
| Claude Code best-practice concepts | `best-practice/` |
| Implementation examples | `implementation/` |
| Research comparisons and deeper analysis | `reports/` |
| Community tips and source-backed examples | `tips/` or `videos/` |
| Markdown output conventions | `.claude/rules/markdown-docs.md` |
| Presentation-specific rules | `.claude/rules/presentation.md` |

Do not add standalone `persona.md`, `references.md`, `ng-rules.md`,
`output-format.md`, or `glossary.md` unless a future change has a distinct,
non-overlapping use for that file.

## Editing Rules

- Search this repository first before adding new Claude Code guidance.
- Keep `CLAUDE.md` concise and under its existing 200-line target.
- Put prohibitions and verification expectations here or in the nearest
  existing rule file, not in a separate `ng-rules.md`.
- Record durable mistakes in `tasks/lessons.md` when a fix should prevent a
  repeated bad decision.
- Do not add generated images, PDFs, archives, or local private settings unless
  the task explicitly requires them.

## Verification

Before reporting completion after repository edits, run:

```sh
git status --short --untracked-files=all
git diff --check
rg -n "OPENAI_API_KEY|ANTHROPIC_API_KEY|GITHUB_TOKEN|ghp_|sk-|AIza|xoxb|BEGIN PRIVATE KEY|password|passwd|secret|token" .
find . -type f \( -iname "*.png" -o -iname "*.jpg" -o -iname "*.jpeg" -o -iname "*.gif" -o -iname "*.pdf" -o -iname "*.zip" \) -print
git status --short --untracked-files=all
```

Inspect secret-scan matches before treating them as leaks; this repository may
document token names or configuration keys as examples.
