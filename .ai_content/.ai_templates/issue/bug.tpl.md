---
id: issue.bug
description: "Bug report; seeds context for downstream bugfix PR and commit."
vars:
  slug:
    - from: ask
  title:
    - from: ask
  problem:
    - from: ask
  steps:
    - from: ask
  expected:
    - from: ask
  actual:
    - from: ask
  root_cause:
    - from: ask
  severity:
    - from: ask
    - default: "Medium"
  risk:
    - from: ask
    - default: "Medium"
  os:
    - from: ask
  browser:
    - from: ask
  version:
    - from: ask
  context:
    - from: ask
  notes:
    - from: ask
out: ".ai_content/.ai_docs/issue/${slug}.md"
usage: >
  Render this first for bugfix flow. pr.bugfix will pull root_cause, steps, expected, actual, and risk from this doc.
---

# Bug Report — ${title}

## Problem / Context

${problem}

## Steps to Reproduce

${steps}

## Expected Behavior

${expected}

## Actual Behavior

${actual}

## Root Cause (if known)

${root_cause}

## Environment

- OS: ${os}
- Browser/Client: ${browser}
- Version/Commit: ${version}
- Additional context: ${context}

## Severity

${severity}

## Risk

${risk}

## Notes

${notes}

## Acceptance Checklist (for PR & Tests)

- [ ] Reproduction is reliable using **Steps to Reproduce**
- [ ] Tests/logs capture the failing behavior
- [ ] Fix restores **Expected Behavior** without regression
- [ ] Risk documented in PR (mirrors this field)
