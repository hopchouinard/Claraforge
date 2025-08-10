# WhyItWorks Learning Model – How Claraforge Teaches Itself (and You)

> *A repo that just sits there is a museum. Claraforge is a dojo—every commit a new sparring match in the art of thinking with AI.*

---

## 0. Why This Doc Exists

People see the philosophies, the prompts, the meta docs and ask, “Great, but how does all this *improve* over time?”  **Answer:** Claraforge is wired with a built‑in learning model—capturing feedback, versioning insight, and auto‑up‑skilling every fork.  This file is the blueprint.

---

## 1. The Learning Loop (Clara‑Spiraled)

```plaintext
Use → Reflect → Fork/PR → Merge ↻
```

1. **Use** – Someone deploys a Clara variant or philosophy in the wild.
2. **Reflect** – Wins & fails logged in `/conversation-logs` or `/why-it-works/reflections`.
3. **Fork/PR** – Improvements proposed (new dial, sharper spec template, fresh philosophy).
4. **Merge** – Maintainers vet alignment → semantic version bump.
5. **Repeat** – Next user starts higher up the mountain.

Every spin raises the floor (see *RTF*), shrinking the gap to the next breakthrough.

---

## 2. Feedback Channels (a.k.a. How the Repo Hears You)

| Channel                           | Expected Payload                                | Action                                            |
| --------------------------------- | ----------------------------------------------- | ------------------------------------------------- |
| **PR with ****`LEARN:`**** tag**  | New philosophy, guardrail tweak, or doc upgrade | Triggers CI doc‑lint + human review               |
| \*\*Issue with \*\***`REFLECT:`** | Field story, bug, or cognitive snag             | Routes to `/reflections` folder via GitHub action |
| **Stars / Forks spike**           | Community adoption metric                       | Maintainers reassess roadmap priorities           |
| **Audio README feedback**         | Emoji reactions & listen stats                  | Regenerates host script tone if boredom detected  |

---

## 3. Governance & Versioning

* **Semantic Philosophy Versioning** – Major = worldview shift, Minor = clarification, Patch = typo or joke upgrade.
* **Sass Dial Tests** – CI pipeline runs tone‑consistency checks against sample prompts; fails if Enterprise Clara suddenly cracks a dad joke.
* **Spec Template Linter** – Ensures new `SPEC‑*` files include non‑goals & acceptance criteria.

If your PR breaks a test, Clara will roast politely. Fix and re‑push.

---

## 4. Metrics That Actually Matter

| KPI                          | Why We Care                           | Target (2025) |
| ---------------------------- | ------------------------------------- | ------------- |
| **Fork Adoption Rate**       | Measures real replication, not vanity | 10 % of stars |
| **Philosophy Delta Ratio**   | % forks that modify philosophies      | ≥30 %         |
| **Conversation Re‑use Hits** | Times old logs cited in new threads   | 100 / month   |
| **Spec Cycle Time**          | Chat‑to‑Spec average duration         | <45 min       |

Because what gets measured gets meme‑ified.

---

## 5. Mini‑Case Study – The Sass Dial Incident

> *Problem:* Enterprise Clara accidentally roasted a board director.
>
> *Reflection:* Issue logged with `REFLECT:` → proposed `[NO_SASS]` fallback flag.
>
> *PR:* Patch added auto‑tone detection; Philosophy Map bumped minor version.
>
> *Outcome:* Financial fork adopted update within 24 h; no directors harmed since.

Learning loop in action.

---

## 6. Contributor Quick‑Start (Level‑Up Edition)

1. **Clone & Run** – Deploy a Clara variant in real work.
2. **Capture Reflection** – Log what surprised, delighted, or broke.
3. **Propose Upgrade** – Open PR with `LEARN:` prefix.
4. **Pass CI Gauntlet** – Tone, linter, version bump.
5. **Brag** – Post your success meme in Discussions.

---

## 7. Future Learning Upgrades

* **Telemetry‑Driven Dial Tuning** – Anonymous usage stats auto‑adjust default sass levels.
* **Philosophy Recommendation Engine** – Suggests new mindsets based on repo analytics.
* **Cross‑Fork Knowledge Sync** – GitHub Action to surface breakthroughs from popular forks back upstream.

PRs welcome—just remember: a learning repo never sleeps.

---

## 8. Final Rally

Tools age. **Learning systems evolve.** Claraforge eats feedback for breakfast and spits out smarter defaults by lunch. Fork it, feed it data, and watch both of you get sharper every release cycle.

*Your brain upgrades daily—your repo should too.*

---

*File location: `why-it-works/META-WhyItWorks_LearningModel.md`*
