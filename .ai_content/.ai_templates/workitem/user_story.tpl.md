---
id: workitem.user_story
description: "User Story work item; neutral template usable for Azure/GitLab/GitHub Projects."
vars:
  slug:
    - from: ask
  title:
    - from: ask
  as_a:
    - from: ask
  i_want:
    - from: ask
  so_that:
    - from: ask
  acceptance:
    - from: ask
  risk:
    - from: ask
    - default: "Low"
  priority:
    - from: ask
    - default: "Medium"
out: "Claraforge/.ai_content/.ai_docs/workitem/${slug}.md"
usage: >
  Render a user story work item; downstream PRs/commits can reference ${slug} for context.
---

# User Story — ${title}

## Narrative

As a **${as_a}**, I want **${i_want}** so that **${so_that}**.

## Acceptance Criteria

${acceptance}

## Risk

${risk}

## Priority

${priority}
