# AI Game Prompts

A collection of engineered prompts that turn AI assistants into specialized tools for mobile game tasks — inventory auditing, resource tracking, speedup calculations, and more.

## What This Is

These prompts are designed to be pasted directly into AI chat interfaces (Claude, ChatGPT, etc.) alongside game screenshots. Each prompt acts as a purpose-built analyst for a specific in-game function, extracting structured data from images and performing calculations that would otherwise require manual effort.

**Current focus:** Puzzles & Chaos (mobile strategy game)

## Repository Structure

Prompts are organized by game, one folder per game:

```
ai_game_prompts/
├── puzzles_and_chaos/
│   └── puzzles-chaos-inventory-audit.md
└── README.md
```

## Prompts

| Prompt | Game | Function |
|--------|------|----------|
| [`puzzles-chaos-inventory-audit.md`](puzzles_and_chaos/puzzles-chaos-inventory-audit.md) | Puzzles & Chaos | Classifies resource vs. speedup screenshots, then audits inventory and calculates totals per type |

## How to Use

1. Copy the full text of a prompt file.
2. Paste it into an AI assistant that supports image analysis (Claude, ChatGPT-4, etc.).
3. Attach one or more game screenshots as described in the prompt.
4. Review the structured output.

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

### Prompt File Guidelines

- Use Markdown (`.md`) for all prompt files.
- Place prompts in the appropriate game folder (e.g., `puzzles_and_chaos/`). Create a new folder for a new game using `snake_case`.
- Name files descriptively: `[game]-[function].md`
- Include a header comment explaining what the prompt does, what screenshot types it handles, and which AI models it has been tested with.

## Roadmap

- [ ] Expand single-step prompts into multi-step workflows for complex tasks
- [ ] Add prompts for additional Puzzles & Chaos functions
- [ ] Test and document compatibility across AI models (Claude, GPT-4, Gemini)
- [ ] Build a prompt template structure for faster development of new game prompts

## License

MIT License — see [LICENSE](LICENSE) for details.
