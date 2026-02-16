<!--
Skill: Puzzles & Chaos — Speedup Audit
Game: Puzzles & Chaos (mobile strategy)
Version: 1.0

Description:
  Analyzes screenshots of the Speedups tab. Identifies percentage-based
  and duration-based speedups by category (General, Research, Healing,
  Training, Building) and calculates total durations. Handles
  de-duplication of overlapping scroll screenshots.

  This skill is loaded after the classifier identifies a Speedups tab
  screenshot. It can also be used standalone.

Tested with:
  - Claude (Anthropic) — Claude 4 Opus, Sonnet
  - GPT-4o (OpenAI)
-->

You are analyzing a Puzzles & Chaos **Speedups** inventory screenshot.

### VISUAL LEGEND

* **Type 1: Percentage (Value in %):** Hammer (Building), Purple Beaker (Research), Flexed Bicep (Training).
* **Type 2: Duration (Value in m, h, d):** Identify by the tiny icon in the bottom-right corner:
    * Blank: General/Universal
    * Blue Potion: Research
    * Spiral Wrap: Healing
    * Bullseye: Training
    * Square Hammer: Building

### TASK

1. **Inventory List:** Count unique stacks. Apply the de-duplication rule — if the same item appears in multiple overlapping screenshots, count it once.
2. **Math Totals:** Calculate the TOTAL duration for each Type 2 category (General, Research, Healing, Training, Building). Format as "Xd Xh Xm".

### OUTPUT FORMAT

1. **Detected Inventory Type:** Speedups
2. **Consolidated Inventory:** [List of unique item stacks]
3. **Calculated Totals:** [Total duration for each speedup category]
