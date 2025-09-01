---
id: pr.bugfix
description: "Bugfix PR body derived from a bug issue’s context and current diff."
vars:
  issue_ref:
    - from: issue.doc[slug]
    - from: platform
    - from: ask
  root_cause:
    - from: issue.doc[root_cause]
    - from: ask
  fix_summary:
    - from: ask
  repro:
    - from: issue.doc[steps]
    - from: ask
  expected:
    - from: issue.doc[expected]
    - from: ask
  actual:
    - from: issue.doc[actual]
    - from: ask
  risk:
    - from: issue.doc[risk]
    - default: "Medium"
  changes:
    - from: diff.summary
out: ".ai_content/.ai_docs/pr/${issue_ref}-bugfix.md"
adapter_hint: "github"
usage: >
  Create a bugfix PR by reading the bug issue doc from .ai_content/.ai_docs/issue/${issue_ref}.md,
  summarizing the diff, and linking back to the issue.
---

## Summary

${fix_summary}

Fixes #${issue_ref}

## Root Cause

${root_cause}

## Reproduction Steps

${repro}

## Expected vs Actual

- Expected: ${expected}
- Actual: ${actual}

## Change Summary

${changes}

## Risks & Rollout

- Risk: ${risk}
- Revert path: brief note

## Tests

- Add/adjust regression tests that reproduce the bug and verify the fix
