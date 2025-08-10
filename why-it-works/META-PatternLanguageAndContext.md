# Pattern Language & Context – Naming Things (So Your Brain Doesn’t Implode)

> *Design is 50 % architecture and 50 % choosing labels that future‑you can actually remember. This doc is the Rosetta Stone for Claraforge pattern names and the context‑stacking rules behind them.*

---

## 0. Why This Exists

The user loves grand ideas; Clara loves sharp labels. A **pattern language** gives every recurring structure a memorable handle, while **context conventions** guarantee those patterns surface at the exact moment you need them. Skip this file and you’ll still enjoy the repo—just with more head‑scratching and `ctrl‑F` flailing.

---

## 1. Core Pattern Taxonomy

| Pattern Tag              | Shorthand       | Lives In                     | One‑Line Cue          |
| ------------------------ | --------------- | ---------------------------- | --------------------- |
| `PHIL‑<slug>`            | Philosophy file | `/philosophies/`             | “Mindset firmware”    |
| `SPEC‑<feature>`         | Design Spec     | `/design-specs/`             | “Ready for dev agent” |
| `PROMPT‑<role>`          | System Prompt   | `/system-prompts/`           | “Persona bootstrap”   |
| `LOG‑<yyyymmdd>‑<topic>` | Chat Transcript | `/conversation-logs/`        | “Full receipts”       |
| `POD‑<topic>‑vX`         | Audio File      | `/podcasts/`                 | “Listen & learn”      |
| `META‑<focus>`           | Meta Insight    | `/why-it-works/`             | “Behind the curtain”  |

> **Tip:** Search any tag prefix in the repo to instantly view every sibling artifact.

---

## 2. Context‑Stacking Rules (a.k.a. How Clara Never Says, “Which doc?”)

1. **Nearest‑Neighbor Principle** – Artifact goes beside its birth chat when possible (`LOG` + `SPEC` co‑located).
2. **Breadcrumb Linking** – Each higher‑order file (README, audio) links down to child artifacts via tag.
3. **Immutable IDs** – Once a tag string is published, don’t rename it. Your spatial memory will revolt.
4. **Upward References Only** – Lower‑level files never import higher‑level context to avoid circular brain‑melts.

---

## 3. Example Walkthrough – Dark Mode Feature

```plaintext
/design-specs/SPEC-dark_mode_toggle.md
/conversation-logs/LOG-20250719-dark_mode_discussion.md
/system-prompts/PROMPT-ClaraOriginal.md
```

`SPEC-dark_mode_toggle` lists `LOG-20250719-dark_mode_discussion` under **Context Links**, while the README audio for July auto‑quotes the spec’s acceptance criteria. Clear lineage, zero hunting.

---

## 4. Adding a New Pattern (Contributor Cheat‑Sheet)

1. Pick a **three‑letter tag** (avoid collisions) → e.g., `QUI` for QuickStart.
2. Create `META-QUI-guidelines.md` explaining usage.
3. Update `META-PatternLanguageAndContext.md` table.
4. Cross‑link at least one existing artifact so pattern isn’t orphaned.

PRs missing step #2 will be roasted by Clara and politely rejected.

---

## 5. Anti‑Pattern Graveyard

| Sin                              | Why It Hurts        | Rehabilitation                        |
| -------------------------------- | ------------------- | ------------------------------------- |
| Generic filenames (`notes.md`)   | Breaks search power | Tag it (`LOG-…`, `META-…`)            |
| Context dump in Slack screenshot | Unsearchable        | Paste as Markdown, reference with tag |
| Renaming tags mid‑project        | Shatters mental map | Create alias file pointing to new tag |

---

## 6. Easter Eggs for Pattern Nerds

* Every `PHIL‑` file name is an isogram—no letter repeats. You’re welcome.
* Tag bytes hash into subtle color themes for podcast cover art.

---

## 7. Final Pep‑Talk

Pattern language turns chaos into click‑through clarity. Context conventions guarantee Clara always has the *right* background without dragging the entire repo into each prompt. **Name things well, drop breadcrumbs generously, and your future self will send you cookies.**

*Now go label something before you forget what it was.*

---

*File location: `why-it-works/META-PatternLanguageAndContext.md`*
