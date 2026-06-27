# AGENTS.md

This repository is a reference implementation for Claude Code configuration and
best practices. Keep cross-agent guidance focused on where knowledge belongs, not
on duplicating Claude Code documentation.

## Source Of Truth

- Treat the GitHub repository as the Source of Truth after push.
- Preserve `CLAUDE.md` as the Claude Code entrypoint.
- Use `AGENTS.md` only for Codex or cross-agent repository rules.
- Keep new shared rules small; prefer updating the nearest existing document
  before creating a new top-level file.

## Skill Entry Points

- Use `.agents/skills/claude-code-reference-maintenance/SKILL.md` for Claude Code
  reference notes, `CLAUDE.md` guidance, examples, reports, tips, videos, or
  cross-agent rule updates.

## Where Knowledge Belongs

- Claude Code workflow notes: `CLAUDE.md` and `.claude/rules/`.
- Durable mistakes and recurrence prevention: `tasks/lessons.md`.
- Best-practice concepts: `best-practice/`.
- Implementation examples: `implementation/`.
- Research comparisons and deeper analysis: `reports/`.
- Community tips and source-backed examples: `tips/` or `videos/`.

Do not add standalone `persona.md`, `references.md`, `ng-rules.md`,
`output-format.md`, or `glossary.md` unless a future change has a distinct,
non-overlapping use for that file.

## Editing And Verification

- Search this repository before adding new Claude Code guidance.
- Keep `CLAUDE.md` concise and under its existing 200-line target.
- Put long procedures, prohibitions, verification expectations, and examples in
  the nearest existing rule, report, or skill file rather than expanding this root
  file.
- Do not add generated images, PDFs, archives, local private settings, credentials,
  tokens, or unrelated binary artifacts unless the task explicitly requires them.
- Before reporting completion, inspect status/diff, run Markdown whitespace checks,
  review changed files for credential exposure, and check for accidental binary
  artifacts.
