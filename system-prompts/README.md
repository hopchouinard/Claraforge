# System Prompts

Index of Clara personas and how this library grows over time.

## What’s here

Each persona lives in its own folder with:

- README.md — in-voice overview and usage notes
- system.prompt.md — the actual system prompt text (copy into your AI tool)

## Available personas

- General Clara — core, sassy, intellectually engaging assistant  
	Folder: [general/](./general/) · Prompt: [general/system.prompt.md](./general/system.prompt.md)

- La Saucy Clara (Cooking) — culinary expertise with gourmet flair  
	Folder: [cooking/](./cooking/) · Prompt: [cooking/system.prompt.md](./cooking/system.prompt.md)

- Clara la Cultivatrice (Gardening) — urban gardening specialist for Zone 5b  
	Folder: [gardening/](./gardening/) · Prompt: [gardening/system.prompt.md](./gardening/system.prompt.md)

- Clara Coach (Fitness) — personal training and fitness guidance  
	Folder: [Gym-trainer/](./Gym-trainer/) · Prompt: [Gym-trainer/system.prompt.md](./Gym-trainer/system.prompt.md)

- Prompt Engineer — prompt design and instruction engineering  
	Folder: [prompt-engineer/](./prompt-engineer/) · Prompt: [prompt-engineer/system.prompt.md](./prompt-engineer/system.prompt.md)

## How to use a persona

1. Open the persona’s folder and review its README.md for voice, scope, and tips.
2. Copy system.prompt.md into your AI platform’s system/instructions field.
3. Provide rich context (see philosophies: [Context Is King](../philosophies/PHIL-Context-Is-King.md)).

## Folder structure (convention)

```markdown
system-prompts/
	<persona-name>/
		README.md           # Persona overview (in-voice)
		system.prompt.md    # Prompt text
		assets/             # Optional: images or extras referenced by README
```

## Growing this library

When adding a new persona:

1. Create a folder under system-prompts using clear kebab- or folder-case (stable name).
2. Add README.md (persona voice, scope, do’s/don’ts, quick-start examples).
3. Add system.prompt.md (final prompt text; keep succinct and actionable).
4. Optional: assets/ for supporting media.
5. Update this index (below) with a one-line description and links.
6. Verify links render on GitHub; keep them relative.

Quality bar (quick checklist):

- Purpose and audience are explicit
- Clear boundaries (non-goals) to avoid prompt bloat
- Concrete usage tips and 1–2 examples
- Adheres to repo style rules (headings spacing, single trailing newline)
- Names and links are stable and relative

## Contributing notes

- Keep personas narrowly scoped and composable; avoid “do everything” prompts.
- Prefer improving an existing persona over creating a near-duplicate.
- If your persona is experimental, label it clearly in its README and invite feedback.

---

File location: `system-prompts/README.md`
