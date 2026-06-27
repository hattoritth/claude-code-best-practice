---
name: claude-code-reference-maintenance
description: Use when updating Claude Code best-practice notes, CLAUDE.md guidance, examples, reports, tips, videos, or cross-agent rules in this reference repository.
---

# Claude Code Reference Maintenance Skill

## Purpose

Maintain this repository as a reference implementation without duplicating Claude Code documentation or expanding root `AGENTS.md`.

## Procedure

1. Search existing files before adding new guidance.
2. Keep `CLAUDE.md` as the Claude Code entrypoint and `AGENTS.md` as the cross-agent/Codex rule file.
3. Put durable mistakes and recurrence prevention in `tasks/lessons.md`.
4. Put best-practice concepts in `best-practice/`, examples in `implementation/`, deeper analysis in `reports/`, and community/source-backed notes in `tips/` or `videos/`.
5. Do not add standalone `persona.md`, `references.md`, `ng-rules.md`, `output-format.md`, or `glossary.md` unless the new file has a distinct non-overlapping purpose.
6. Keep long procedures, examples, and verification expectations in the nearest existing rule/report/skill file instead of root `AGENTS.md`.

## Verification

- Reread changed files.
- Check Markdown formatting and focused diff.
- Confirm no generated images, PDFs, archives, local private settings, credentials, tokens, or unrelated binary artifacts were introduced unless explicitly required.
- Treat documentation examples of credential names as non-leaks only after inspection.

## Report

Report changed files, verification performed, commit/push status, and remaining follow-ups.
