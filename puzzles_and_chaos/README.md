# Puzzles & Chaos

AI prompts and skills for the mobile strategy game Puzzles & Chaos.

## Available Prompts (standalone)

| File | Function |
|------|----------|
| [`inventory-audit.md`](prompts/inventory-audit.md) | Classifies resource vs. speedup screenshots, audits inventory, calculates totals |
| [`hero-inventory.md`](prompts/hero-inventory.md) | Extracts hero stats (name, level, enhancement, stars) from hero inventory screenshots |
| [`curio-inventory.md`](prompts/curio-inventory.md) | Extracts Curio data (name, rarity, enhancement, ascension) from Curio Warehouse screenshots with Legion Attribute and Hero Attribute lookups |

## Available Skills (modular)

| File | Role |
|------|------|
| [`classifier.md`](skills/classifier.md) | Master classifier — identifies screenshot type and routes to the correct skill |
| [`resource-audit-skill.md`](skills/resource-audit-skill.md) | Analyzes Resources tab screenshots |
| [`speedup-audit-skill.md`](skills/speedup-audit-skill.md) | Analyzes Speedups tab screenshots |

## Skill Workflow

1. Load `classifier.md` as your system prompt or skill.
2. Attach inventory screenshots.
3. The classifier identifies the tab type and tells you which skill to load.
4. Load the appropriate skill (e.g., `resource-audit-skill.md`) and run the analysis.

## Coming Soon

- Curio Legion Attributes and Exclusive Attributes lookup tables
- Curio-to-Hero partner mapping
