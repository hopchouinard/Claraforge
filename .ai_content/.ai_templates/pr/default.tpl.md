---
id: pr.default
description: "Standard PR body derived from the active feature issue’s context."
vars:
  issue_ref:
    - from: issue.doc[slug]
    - from: platform
    - from: ask
  outcome:
    - from: issue.doc[problem]
    - from: ask
  plan:
    - from: issue.doc[acceptance]
    - from: ask
  risk:
    - from: issue.doc[risk]
    - default: "Low"
  has_migrations:
    - from: ask
  changes:
    - from: diff.summary   # Copilot: summarize current diff into bullets/lines
out: ".ai_content/.ai_docs/pr/${issue_ref}.md"
adapter_hint: "github"
usage: >
  Create a PR for the current issue by pulling context from .ai_content/.ai_docs/issue/${issue_ref}.md,
  summarizing the diff into bullet points, and linking back to the issue.
---

## Summary

${outcome}

Fixes #${issue_ref}

## Plan

${plan}

## Change Summary

${changes}

## Risks & Rollout

- Risk: ${risk}
- Migrations: ${has_migrations}
- Revert path: brief note

## Tests

- Outline new/updated cases or rationale if none are required
