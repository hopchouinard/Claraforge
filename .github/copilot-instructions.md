# Claraforge – AI Agent Guide (concise)

Purpose: make agents productive fast by encoding repo-specific structure, tone, and workflows.

## Big picture

- Docs-first repo: system prompts (personas), philosophies (principles), why-it-works (meta/architecture), conversation-logs (receipts), design-specs (handoffs).
- No code build here; the work is high-quality Markdown and navigation.
- Clara’s voice only in persona-facing docs; neutral tone elsewhere.

## Key directories

- system-prompts/<persona>/: README.md (in-voice), system.prompt.md (prompt text)
- philosophies/: principles index at philosophies/README.md
- why-it-works/: meta rationale index at why-it-works/README.md
- conversation-logs/Ultimate-AI-Agent-Design/: exemplar + summary README
- design-specs/: implementation handoffs (use “From Chat to Code” style)

## How to contribute (docs-first)

1. Add content in the right place and link it:

- Philosophy → /philosophies + add to its README
- Meta rationale → /why-it-works + update its README section
- Persona → /system-prompts/<name>/ with README.md + system.prompt.md
- Implementation plan → /design-specs/<slug>.md using spec bullets below

2. Keep indices current and links relative; verify navigation from root → folder README → file.

## Style rules (enforced by convention)

- Blank line before/after headings and lists.
- Fences specify language (`markdown, `text). Dialogues use ```text.
- Single trailing newline at EOF.
- Optional footer: “File location: `path/to/file`”.

## Design-spec bullets (From Chat to Code)

- Context & Goal, Non-goals, Acceptance criteria, Artifacts, Open questions/risks.

## Naming & linking

- Prefer system.prompt.md (standard for prompts). Keep filenames stable.
- Use kebab-case slugs; link relatively; ensure links render on GitHub.

## Concrete examples in this repo

- Conversation → summary: conversation-logs/Ultimate-AI-Agent-Design/README.md.
- Meta index: why-it-works/README.md with audience-specific paths.
- Persona packaging: system-prompts/general/ (in-voice README + prompt).

## PR hygiene

- Small focused diffs, descriptive titles, working links, style rules followed.

Questions or gaps? Add assumptions in your PR and propose updates to this file.
