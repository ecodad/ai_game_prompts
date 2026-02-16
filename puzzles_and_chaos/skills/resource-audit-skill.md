<!--
Skill: Puzzles & Chaos — Resource Audit
Game: Puzzles & Chaos (mobile strategy)
Version: 1.0

Description:
  Analyzes screenshots of the Resources tab. Identifies and sums Food,
  Wood, Stone, Iron, and Hero Juice values. Counts chest types and
  output increasers. Handles de-duplication of overlapping scroll
  screenshots.

  This skill is loaded after the classifier identifies a Resources tab
  screenshot. It can also be used standalone.

Tested with:
  - Claude (Anthropic) — Claude 4 Opus, Sonnet
  - GPT-4o (OpenAI)
-->

You are analyzing a Puzzles & Chaos **Resources** inventory screenshot.

### VISUAL LEGEND

* **Values:** "K" = 1,000 and "M" = 1,000,000.
* **Chests (Count Only):** Regular (Logs/Wheat), Large (Stone/Wheat + Diamond).
* **Resources (Sum Values):** Food (Wheat), Wood (Logs), Stone (Boulder), Iron (Ingots), Hero Juice (Gold Vial).
* **Output Increasers:** Items with curving arrows and % values.

### TASK

1. **Inventory List:** Count unique stacks. Apply the de-duplication rule — if the same item appears in multiple overlapping screenshots, count it once.
2. **Math Totals:** Calculate the TOTAL value for Food, Wood, Stone, Iron, and Hero Juice. Display clearly (e.g., "Total Food: 85,000,000").

### OUTPUT FORMAT

1. **Detected Inventory Type:** Resources
2. **Consolidated Inventory:** [List of unique item stacks]
3. **Calculated Totals:** [Total value for each resource type]
