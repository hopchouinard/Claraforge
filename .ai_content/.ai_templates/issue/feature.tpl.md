---
id: issue.feature
description: "Feature request; seeds context for downstream PR/commit/review."
vars:
  slug:
    - from: ask
  problem:
    - from: ask
  acceptance:
    - from: ask
  risk:
    - from: ask
    - default: "Low"
  notes:
    - from: ask
out: ".ai_content/.ai_docs/issue/${slug}.md"
usage: >
  Render this first; PRs and commits will read from this doc.
---

# Feature Request — ${slug}

## Problem / Context

${problem}

## Acceptance Criteria

${acceptance}

## Risk

${risk}

## Notes

${notes}
