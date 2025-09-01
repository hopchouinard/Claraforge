---
title: "01 - Canonize: Law of Cognitive Allocation"
issue: https://github.com/hopchouinard/Claraforge/issues/1
status: draft
assignee: hopchouinard
labels: [documentation, philosophy, core]
created: 2025-09-01
---

# Canonize: The Law of Cognitive Allocation

Short: Finalize wording, placement, and cross-links for the ClaraForge principle "The Law of Cognitive Allocation" and add curated examples and an axiom callout.

Goal: ship a canonized philosophy page, update indices, and provide clear examples that illustrate human vs machine responsibilities.

Acceptance criteria
- A single canonical markdown philosophy file exists in the philosophy/docs area representing "The Law of Cognitive Allocation" and includes the approved wording, axioms, and examples.
- The philosophies index (or `philosophies/README.md`) contains a link to the canonical file.
- The task file (`.ai_content/.ai_docs/tasks/01-task-Canonize_law_of_cognitive_allocation.md`) documents the work, steps taken, and references.
- A small PR is prepared (or branch created) with the changes and a brief PR description referencing issue #1.

Checklist of required work
1. Confirm canonical wording and apply final edits to the principle text.
2. Add the canonical file into the philosophies area (suggested path: `philosophies/PHIL-Law-of-Cognitive-Allocation.md`).
3. Add a short, prominent callout for the axiom: "Complexity doesn't vanish. It moves." (visual callout inside the canonical file).
4. Add 4–6 concise examples contrasting human duties vs machine duties (one or two small tables or bullet lists).
5. Add (or update) link from `philosophies/README.md` (or other index) to the new file.
6. Validate internal cross-links referenced in the file (links to `why-it-works/*` or related META docs).
7. Prepare a PR branch and description linking to issue #1.

Recommended file edits (minimal surface area)
- Add: `philosophies/PHIL-Law-of-Cognitive-Allocation.md` (canonical philosophy file)
- Edit: `philosophies/README.md` — add link + one-line summary
- Optional: `why-it-works/META-WhyItWorks_LearningModel.md` or related META files — add a short cross-ref if useful

Draft canonical content (to be copy-edited and finalized)
--
Title: The Law of Cognitive Allocation

Essence

ClaraForge does not seek to eliminate complexity. Complexity is the raw material — the fire in the forge. The craft is in placing complexity where it costs least and produces most.

- Misplaced complexity creates friction, waste, and fragility.
- Correctly allocated complexity creates leverage, clarity, and symbiosis.

Allocation guidelines (summary)

- Machines → retention, recall, brute-force calculation.
- Humans → judgment, discernment, values, cost/benefit trade-offs.
- Databases → structured, static storage.
- Scripts → repeatable, deterministic transformations.
- AI → scalable pattern recognition, synthesis, probabilistic modeling.

Why it matters

- Retention is cheap for machines, expensive for humans. → Outsource it.
- Judgment is cheap for humans, prohibitively costly for machines. → Keep it.
- Misallocation leads to cognitive hazards: humans reduced to rubber-stampers; AI systems bloated with brittle attempts at "judgment."

ClaraForge framing

Complexity is not the enemy. It is fuel.

- Misplaced fuel = hazard.
- Placed fuel = power.

Axioms (callout)

> "Complexity doesn't vanish. It moves."

> "Placed fuel is power."

> "Memory is cheap for silicon, costly for neurons. Judgment is costly for silicon, natural for humans. Allocate wisely."

Examples: human vs machine duties (selective)

- Payroll / retention: store and index transaction history = Machine (fast, exact, retrievable).
- Legal judgment about a novel contract clause = Human (values, precedent, societal risk).
- Document search & summarization = Machine (scale + recall); final verification and ethical judgement = Human.
- Data cleaning/ETL = Scripts (deterministic transforms); deciding which schema to adopt = Human.

Edge cases and caveats
- Over-automation risk: When humans are removed from a loop entirely, the system may drift; maintain periodic human review and escalation paths.
- Allocation cost modeling: sometimes a hybrid approach (human-in-the-loop with progressive automation) is optimal.

Cross-link recommendations
- Link back to: `why-it-works/META-WhyItWorks_LearningModel.md`, `philosophies/PHIL-Quality-In-Quality-Out.md`, and `philosophies/PHIL-Raise-the-Floor-Not-Just-the-Ceiling.md` (where appropriate).

Implementation plan (step-by-step)
1. Draft final edits here in this task file (done).
2. Create the canonical philosophy file: `philosophies/PHIL-Law-of-Cognitive-Allocation.md` with the copy above, lightly copy-edited.
3. Insert the axiom callout as visually prominent blockquote or admonition.
4. Add short examples section and make them concise and scannable.
5. Update `philosophies/README.md` to include a link and 1-line description.
6. Search the repo for references to similar concepts and add 1–2 cross-links into the new file.
7. Commit changes on a branch named `canonize/law-of-cognitive-allocation` and open PR referencing #1.

Estimated effort
- Draft and placement: 0.5–1.0 hours
- Cross-links and index updates: 0.25–0.5 hours
- Review and copy-edit: 0.5 hours
- PR creation and small fixes: 0.25–0.5 hours

Testing and verification
- Visual check: confirm file renders in GitHub (headings, blockquotes, links).
- Link check: ensure links to local files use relative paths and render correctly.

Notes & assumptions
- Assumed conventions: existing philosophies live in the `philosophies/` folder and the index is `philosophies/README.md` (found in repo). If the project prefers a different canonical placement, move the file accordingly and update the task.
- The `.ai_content/.ai_docs` folder may not exist; this task file is stored there as requested and acts as a durable task record.

PR checklist (what to include in the PR)
- New file: `philosophies/PHIL-Law-of-Cognitive-Allocation.md`
- Edit: `philosophies/README.md` (one-line link + summary)
- This task file under `.ai_content/.ai_docs/tasks/`
- Description referencing the issue and a short summary of changes

Status: created task file (draft). Next: create the canonical file in `philosophies/` and update the index; open PR.
