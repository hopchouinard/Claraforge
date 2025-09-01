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

# Copilot Loader (repo-local)
When asked to create/format issues, PRs, commits, or reviews:
1) Load templates from `.ai_content/.ai_templates/` via `.ai_content/registry.yaml`.
2) Treat files matching `*.tpl.*` as templates; render with repo context (issue, diff).
3) Emit to the requested surface (PR body, commit message, or `.ai_content/.ai_docs/...`).
Do not invent facts not present in code, diff, or linked items.

# Copilot Instructions for Template Rendering

- All AI-driven templates live in `.ai_content/.ai_templates/`
- Each template file starts with a YAML front-matter block describing:
  - `id` (unique identifier)
  - `vars` (placeholders to fill, e.g. ${problem})
  - `out` (destination path in `.ai_content/.ai_docs/`)
- To generate an artifact:
  1. Parse the front-matter.
  2. Collect values for each variable from context or by asking the user.
  3. Replace all `${VAR}` placeholders in the body.
  4. Save to the `out` path, preserving subdirectories.
- Do not hallucinate values. Ask for missing ones.

## AI-only Template Flow

When I say “create a PR for the current issue” (or similar):

1) **Select template**  
   - Read metadata (YAML front-matter) from:
     - `.ai_content/.ai_templates/pr/default.tpl.md`  → PR
     - `.ai_content/.ai_templates/issue/feature.tpl.md` → Issue
     - `.ai_content/.ai_templates/commit/conventional.tpl.txt` → Commit
2) **Resolve variables** (highest → lowest):
   - From **linked doc** in `.ai_content/.ai_docs/` (e.g., the issue’s rendered file)
   - From **repo context** (branch name, diff, commit history)
   - From **current issue/PR** in the platform
   - If still missing → **ask me** for the minimal set
3) **Render**: Replace `${VAR}` tokens in the template body (no loops/conditionals).
4) **Emit**:
   - For PRs: open PR composer and paste the rendered body.
   - For Issues/Docs: write to `.ai_content/.ai_docs/<type>/<slug>.md`.
   - For commit messages: stage the message in the VCS commit box.
5) **Link**: If `issue_ref` is available, include close/reference keywords per adapter rules.
