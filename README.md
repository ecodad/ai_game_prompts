# AI Game Prompts

A collection of engineered prompts that turn AI assistants into specialized tools for mobile game tasks — inventory auditing, resource tracking, speedup calculations, and more.

## What This Is

These prompts are designed to be pasted directly into AI chat interfaces (Claude, ChatGPT, etc.) alongside game screenshots. Each prompt acts as a purpose-built analyst for a specific in-game function, extracting structured data from images and performing calculations that would otherwise require manual effort.

**Current focus:** Puzzles & Chaos (mobile strategy game)

## Repository Structure

Each game has its own folder containing two subfolders:

- **`prompts/`** — Standalone, self-contained prompts. Copy-paste into any AI chat. No setup required.
- **`skills/`** — Modular pieces for skill-based workflows. A master classifier identifies the screenshot type and loads only the relevant analysis skill, saving context window space.

```
ai_game_prompts/
├── puzzles_and_chaos/
│   ├── prompts/
│   │   └── inventory-audit.md              (standalone, all-in-one)
│   ├── skills/
│   │   ├── classifier.md                   (master: identifies screenshot type)
│   │   ├── resource-audit-skill.md         (Protocol A: resources)
│   │   └── speedup-audit-skill.md          (Protocol B: speedups)
│   └── README.md
└── README.md
```

## Prompts vs. Skills

| Approach | Best for | How to use |
|----------|----------|------------|
| **Prompts** (standalone) | Quick use, free-tier AI, sharing with others | Copy the full prompt file, paste into AI chat, attach screenshots |
| **Skills** (modular) | Repeated use, large inventories, preserving context window | Load the classifier as a skill/system prompt, then load the specific analysis skill as needed |

Both approaches produce the same output. The skills version is more efficient with tokens since it only loads the protocol needed for the screenshot type detected.

## Prompt Design Principles

These prompts use several techniques to get reliable results from AI vision models:

- **Image classification** — The prompt first identifies what type of screenshot it's looking at (e.g., Resources tab vs. Speedups tab) before choosing an analysis path.
- **Protocol branching** — A single prompt handles multiple screenshot types by classifying the input first, then routing to the correct analysis protocol.
- **Visual legend definitions** — Icons and symbols are described explicitly so the model knows what to look for (e.g., "Hammer = Building speedup").
- **De-duplication rules** — Screenshots of scrolling inventories often overlap. The prompts include logic to detect and merge duplicate entries.
- **Structured output formatting** — Every prompt specifies an exact output format so results are consistent and easy to compare across sessions.

## Contributing

This project is in early stages. Contributions welcome:

- **Improve existing prompts** — Better accuracy, edge case handling, clearer instructions.
- **Add new prompts** — For other games or other in-game functions.
- **Report issues** — If a prompt misreads inventory items or miscalculates totals, open an issue with the screenshot(s) and the AI's output.

### File Guidelines

- Use Markdown (`.md`) for all prompt and skill files.
- Place files in the appropriate game folder. Create a new game folder using `snake_case`.
- **Prompts:** Name as `[function].md` (e.g., `inventory-audit.md`). Self-contained, includes all protocols.
- **Skills:** Name as `[function]-skill.md` (e.g., `resource-audit-skill.md`). Each skill handles one protocol.
- Include a header comment explaining what the file does, what screenshot types it handles, and which AI models it has been tested with.

## Roadmap

- [ ] Add hero inventory prompt with wiki lookup integration
- [ ] Expand single-step prompts into multi-step workflows for complex tasks
- [ ] Add prompts for additional Puzzles & Chaos functions
- [ ] Test and document compatibility across AI models (Claude, GPT-4, Gemini)
- [ ] Build a prompt template structure for faster development of new game prompts

## License

MIT License — see [LICENSE](LICENSE) for details.
