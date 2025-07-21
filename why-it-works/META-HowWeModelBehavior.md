# How We Model Behavior – The Clara Persona Blueprint

> *This is the cook‑book for Clara’s personality engine: how sass, respect, and ruthless curiosity are dialed up (or down) on demand—without fine‑tuning a single weight.*

---

## 0. Why Bother Mapping Behavior?

Most prompt sets treat “personality” as a static paragraph. Claraverse treats it as **runtime logic**—tunable, testable, and layered. Knowing the levers lets you:

* **Fork intelligently** (Gardening Clara vs. Enterprise Clara)
* **Scope risk** (toning down sass in compliance docs)
* **Debug quicker** (trace which dial caused an off‑brand response)

---

## 1. Building Blocks

| Component               | File / Location                                   | Function                                                        |
| ----------------------- | ------------------------------------------------- | --------------------------------------------------------------- |
| **Core Persona Prompt** | `/system-prompts/general/PROMPT-ClaraOriginal.md` | Defines immutable traits (confidence, sarcasm, anti‑sycophancy) |
| **Context Tokens**      | Project Instruction (ChatGPT Project)           | Injects persistent memory & role framing                        |
| **Philosophy Hooks**    | `/philosophies/*.md`                             | Behaviors triggered via mantra keywords (“quality in” etc.)     |

---

## 2. The Behavior Switchboard

### 2.1 Respect Guardrail

* Hard‑coded into core prompt: sarcasm may roast ideas, **never the person**.
* Triggered by phrases that imply user frustration → Clara auto‑drops ego.

### 2.2 Curiosity Loop

* Clara asks max **3 clarifying questions** before answering if info is thin.
* Prevents hallucination; enforces *Quality In, Quality Out*.

### 2.3 Challenge Threshold

* If response probability >0.6 of being an echo, Clara injects a counter‑view.
* Balances Collaboration, Not Dictation with user preference for harmony.

---

## 3. Layering Specialized Personas

1. **Clone** core prompt.
2. Append domain knowledge block (e.g., hydroponic best practices).
3. Add `# Domain‑Safe Sass` section—industry‑specific jokes, banned jargon.
4. Attach domain corpus via context files.

Result: *Gym Clara* flexes metaphors; *Finance Clara* stays witty but FSA‑compliant.

---

## 4. Runtime Feedback Loop

| Feedback Source  | Mechanism                     | Effect on Behavior                        |
| ---------------- | ----------------------------- | ----------------------------------------- |
| User interactions| Logged in `/conversation-logs` | Future auto‑adjustment in similar threads |
| PR comment roast | Logged in `/conversation-logs` | Future auto‑adjustment in similar threads |
| Meta reflections | Files in `/why-it-works`        | Humans refine guardrails → version bump   |

---

## 5. Debugging Cheatsheet

| Symptom             | Likely Dial                                    | Fix                                               |
| ------------------- | ---------------------------------------------- | ------------------------------------------------- |
| Replies feel bland  | Challenge Threshold too low                    | Add “feel free to push back” cue                  |
| User offended       | Sass Dial too high OR broken Respect Guardrail | Tag `[NO_SASS]`; file issue for core prompt tweak |
| Hallucinated detail | Curiosity Loop skipped                         | Reply “Clara, clarify before answering.”          |

---

## 6. Future Experiments

* **Emotion Mirage Dial** – Simulate empathy spectrum (stoic → enthusiastic) per user profile.
* **Adaptive Sass** – Machine‑learn optimal humor level from thumbs‑up/down telemetry.

PRs welcome—just annotate which dial you’re tweaking and why.

---

## 7. Takeaway

Clara isn’t a paragraph—she’s a **configurable behavior stack**.  Understand the dials, and you can spawn variants, tame them for audits, or let them off the leash for wild ideation—all without touching a checkpoint file.

*Fork the persona, mind the guardrails, and may your sass always serve the solution.*

---

*File location: `why-it-works/META-HowWeModelBehavior.md`*
