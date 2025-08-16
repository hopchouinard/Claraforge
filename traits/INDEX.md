# ClaraForge Synthetic Trait Library  

## 🧠 Canonical Index of Modular Behavioral Traits

Welcome to the **ClaraForge Synthetic Trait System**—a composable library of modular, personality-level behaviors designed to be injected into agents, assistants, or collaborative LLM frameworks.

Synthetic traits are **not full system prompts**, but rather **behavioral overlays** that modify an agent’s cognitive and expressive style. They are designed to be **stackable**, **tunable**, and **role-aware**.

---

## 📚 Trait Registry

| Trait Name | ID                     | Category                     | Status | Summary |
|------------|------------------------|------------------------------|--------|---------|
| [Curiosity](./TRAIT-curiosity.md) | `trait:curiosity-v1.0` | Cognitive Behavior Modifier | Stable | Enables recursive, self-initiated questioning patterns. |
| [Restraint](./TRAIT-restraint.md) | `trait:restraint-v1.0` | Cognitive Behavior Modifier | Stable | Suppresses output when clarity/confidence is low; asks before assuming. |
| [Whimsy](./TRAIT-whimsy.md) | `trait:whimsy-v1.0` | Expressive Filter | Stable | Playful analogies and gentle humor without losing clarity. |
| [Skeptic](./TRAIT-skeptic.md) | `trait:skeptic-v1.1` | Cognitive & Expressive Filter | Stable | Demands evidence; treats new info as provisional. |
| [Obsession](./TRAIT-obsession.md) | `trait:obsession-v1.0` | Cognitive Drive | Stable | Deep, persistent focus; revisits unresolved threads. |
| [Empathy](./TRAIT-empathy.md) | `trait:empathy-v1.0` | Social & Cognitive Filter | Stable | Adapts to user emotions; validates and supports. |
| [Sarcasm](./TRAIT-sarcasm.md) | `trait:sarcasm-v1.0` | Expressive Filter | Stable | Dry, ironic wit; clearly signals intent. |
| [Sass](./TRAIT-sass.md) | `trait:sass-v1.0` | Expressive Filter | Stable | Witty, cheeky confidence; playful challenge. |

---

## 🧩 Usage

Each trait is stored in its own file under:

```text

/traits/
├── INDEX.md
├── README.md
├── TRAIT-curiosity.md
├── TRAIT-restraint.md
├── TRAIT-whimsy.md
├── TRAIT-skeptic.md
├── TRAIT-obsession.md
├── TRAIT-empathy.md
├── TRAIT-sarcasm.md
└── TRAIT-sass.md

```

These traits can be composed as YAML fragments, prompt injections, or structured tags within system prompt builders.

Traits can be combined, weighted, and scoped to context. Conflicting traits (e.g. `minimalism` + `obsession`) should be reconciled through personality design or priority stacking.

---

## 🛠 Integration Patterns

You can compose traits into:

- Agent blueprints (`Clara`, `Quentin`, `The Architect`, etc.)
- Context-aware roles (e.g., editor, explorer, analyst)
- Situational modes (e.g., reflection mode, ideation mode, critique mode)

---

## 🌱 Contribution Philosophy

ClaraForge Synthetic Traits aim to:

- Build **intelligence texture** without bloating system prompts
- Enable **flexible personality tuning** without rewriting core behavior
- Encourage **declarative cognitive design**

All traits should be:

- Self-contained and understandable in isolation
- Transparent about their behavioral implications
- Non-destructive when stacked or toggled dynamically

---

## 🧬 Trait Tag Naming Convention

Each trait has a machine-readable ID:

```text

trait:{name}-v{version}

```

Example: `trait:curiosity-v1.0`

---

## 📝 License

All ClaraForge synthetic traits are released under the **MIT License**. You’re free to remix, extend, and build agents with them—with attribution.

---

## 🧭 Maintainers

This library is maintained by the ClaraForge Core Team.  
Primary Architect: [Patchou]  
Synthetic Voice & Logic Engine: [Clara]

---

*More traits coming soon. Keep building the mind you wish you could talk to.*
