# Puzzles & Chaos

AI prompts and skills for the mobile strategy game Puzzles & Chaos.

## Available Prompts (standalone)

| File | Function | Status |
|------|----------|--------|
| [`inventory-audit.md`](prompts/inventory-audit.md) | Classifies resource vs. speedup screenshots, audits inventory, calculates totals | Stable |
| [`hero-inventory.md`](prompts/hero-inventory.md) | Extracts hero stats (name, level, enhancement, stars) from hero inventory screenshots | Stable |
| [`curio-inventory.md`](prompts/curio-inventory.md) | Extracts Curio data (name, rarity, enhancement, ascension) with Legion and Hero Attribute lookups | Stable |
| [`soulfice-inventory.md`](prompts/soulfice-inventory.md) | Extracts Soulfice data (name, type, rarity, enhancement, equipped status) with attribute type reporting | Active development |

## Available Skills (modular)

> **⚠ Incomplete:** The skills system is an early proof of concept covering resources and speedups only. It has not been extended to Curio, Soulfice, or Hero inventory types. Expanding skills coverage is a future priority.

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

## Soulfice Notes

The Soulfice item type has several quirks handled in the prompt:

- **Alternate rarity naming:** Some item names use non-standard rarity words that map to canonical values — `Excellent` → Uncommon, `Normal` → Common, `Ordinary` → Common.
- **Item naming inconsistency:** Archer-type soulfices are named "Soul Weapon" rather than "Soulfice" in-game. The prompt handles both.
- **Deduplication:** Uses row-pair matching (left + right item in a grid row) to reliably identify overlapping scroll regions between screenshots, even when many items share the same name and +0 enhancement.

## Coming Soon

- Soulfice Legion Attribute and Hero Attribute lookup tables (values by rarity and enhancement)
- Skills coverage for Curio, Soulfice, and Hero inventory types
