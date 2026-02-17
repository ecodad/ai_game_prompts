# Model Choice Matters for Accuracy
This is an example of running the same prompt with the same images with **Gemini 3 Fast** vs **Gemini 3 Thinking** in Temporary Chats

## Examples of hallucinated results
1. In **Gemini 3 Fast** Sodoma's Troop Skills are listed as Cavalry while in **Gemini 3 Thinking** they are correctly noted as Troop.
2. 

|  | Gemini 3 Fast| Gemini 3 Thinking| Correct |
|--|-|-|--|
| **Sodoma's Troop Skill** | Cavalry HP, DEF, ATK +150%| Troop HP, DEF, ATK +150%| Troop HP, DEF, ATK +75% |
| **Sodoma's Curio** | Totem of Spirits| Specter Veil| Specter Veil |
| **Edith's Curio** | Bow of Stars| Chilling Spear| Chilling Spear |
| **Selantia's Curio** | None| Ocean Pearl| Moonfall Scepter |

## Results from Gemini 3 Fast
```
Name	Stars	Level	Enhancement	Type	Troop Skills	Curio
Sodoma	6	350	+7	Cavalry	Cavalry HP +150% | Cavalry DEF +150% | Cavalry ATK +150%	Totem of Spirits
Tania	6	350	+7	Cavalry	Cavalry HP +150% | Cavalry DEF +150% | Cavalry ATK +150%	Ocean Harp
Edith	6	350	+6	Archer	Archer HP +100% | Archer DEF +100% | Archer ATK +100%	Bow of Stars
Fiona	6	348	+6	Civil	Training Speed +40% | Stamina Cost Down -24%	Dragon Horn
Kujo Mamoru	6	310	+6	Infantry	Infantry HP +100% | Infantry DEF +100% | Infantry ATK +100%	Jade Blade
Patty	6	310	+6	Civil	Research Speed +40% | Resource Protection +40%	Ancient Compass
Angelita	6	350	+5	Archer	Archer ATK +100% | Cavalry ATK +100% | Troop DEF +100%	Sword of Omens
Aerposia	6	310	+5	Cavalry	Cavalry ATK +100% | Archer ATK +100% | Troop HP +100%	Ghost Scythe
Boyd	6	310	+5	Archer	Archer ATK +100% | Infantry ATK +100% | Troop HP +100%	Primal Claw
Rodriguez	6	310	+5	Infantry	Infantry ATK +100% | Cavalry ATK +100% | Troop DEF +100%	Shield of Aegis
Setemos	6	310	+5	Infantry	Infantry ATK +100% | Archer ATK +100% | Troop HP +100%	Anubis Staff
Sirona	6	310	+5	Civil	Building Speed +40% | Troop Load +40%	Siren Shell
Tutanhet	6	310	+5	Archer	Archer ATK +100% | Infantry ATK +100% | Troop DEF +100%	Golden Mask
Carvell	5	310	+4	Infantry	Infantry HP +35% | Infantry DEF +35% | Infantry ATK +35%	None
Norris	5	310	+4	Cavalry	Cavalry HP +35% | Cavalry DEF +35% | Cavalry ATK +35%	None
Saya	5	310	+4	Archer	Archer HP +35% | Archer DEF +35% | Archer ATK +35%	None
Lylia	5	310	+3	Cavalry	Cavalry HP +25% | Cavalry DEF +25% | Cavalry ATK +25%	None
Ogremire	5	264	+3	Infantry	Infantry HP +25% | Infantry DEF +25% | Infantry ATK +25%	None
Sea Goddess	5	310	+3	Civil	Gathering Speed +15% | Research Speed +15%	None
Tala	5	310	+3	Archer	Archer HP +25% | Archer DEF +25% | Archer ATK +25%	None
Violette	5	310	+3	Civil	Stamina Cost Down -12% | Building Speed +15%	None
Wu Kong	5	310	+3	Infantry	Infantry HP +25% | Infantry DEF +25% | Infantry ATK +25%	None
Anastasia	5	310	+2	Civil	Training Speed +12% | Stamina Cost Down -8%	None
Aurora	5	310	+2	Archer	Archer HP +15% | Archer DEF +15% | Archer ATK +15%	None
Edmund	5	310	+2	Infantry	Infantry HP +15% | Infantry DEF +15% | Infantry ATK +15%	None
Eris	5	310	+1	Cavalry	Cavalry HP +8% | Cavalry DEF +8% | Cavalry ATK +8%	None
Estelle	5	310	+1	Civil	Building Speed +8% | Troop Load +8%	None
Monica	5	310	+1	Civil	Research Speed +8% | Resource Protection +8%	None
Selantia	5	310	+1	Archer	Archer HP +8% | Archer DEF +8% | Archer ATK +8%	None
Leona	4	236	+3	Infantry	Infantry HP +15% | Infantry DEF +15%	None
```


## Results from Gemini 3 Thinking
```
Name	Stars	Level	Enhancement	Type	Troop Skills	Curio
Sodoma	6	350	+7	Cavalry	Troop HP +150% | Troop DEF +150% | Troop ATK +150%	Specter Veil
Tania	6	350	+7	Cavalry	Cavalry HP +150% | Cavalry DEF +150% | Cavalry ATK +150%	Ocean Harp
Edith	6	350	+6	Archer	Archer HP +120% | Archer DEF +120% | Archer ATK +120%	Chilling Spear
Fiona	6	348	+6	Civil	Training Speed +40% | Stamina Cost Down -24% | Troop Capacity +37,500	Dragon Horn
Kujo Mamoru	6	310	+6	Infantry	Infantry HP +120% | Infantry DEF +120% | Infantry ATK +120%	Kujo's Fan
Patty	6	310	+6	Civil	Building Speed +48% | Stamina Cost Down -24% | Troop Capacity +37,500	Golden Scale
Aerposia	6	310	+5	Cavalry	Cavalry HP +100% | Cavalry DEF +100% | Cavalry ATK +100%	Blade of Chaos
Angelita	6	350	+5	Archer	Archer ATK +100% | Cavalry ATK +100% | Troop DEF +100%	Sword of Omens
Boyd	6	310	+5	Cavalry	Cavalry HP +100% | Cavalry DEF +100% | Cavalry ATK +100%	Wolf's Tooth
Rodriguez	6	310	+5	Infantry	Troop HP +100% | Troop DEF +100% | Troop ATK +100%	Conqueror's Crown
Setemos	6	310	+5	Infantry	Infantry HP +100% | Infantry DEF +100% | Infantry ATK +100%	Anubis' Scepter
Sirona	6	310	+5	Civil	Resource Gather Speed +30% | Medical Tent Healing Speed +37.5% | Troop Capacity +25,000	Crescent Scepter
Tutanhet	6	310	+5	Archer	Archer HP +100% | Archer DEF +100% | Archer ATK +100%	Pharaoh's Mask
Carvell	5	310	+4	Civil	Research Speed +24% | Training Speed +24% | Troop Capacity +20,000	Sword of Angel
Norris	5	310	+4	Archer	Archer HP +80% | Archer DEF +80% | Archer ATK +80%	Chalice of Blood
Saya	5	310	+4	Civil	Safe Resources +30% | Food Output +30% | Troop ATK +60%	Ghost Blade
Lylia	5	310	+3	Civil	Medical Tent Healing Speed +18% | Heal Iron Cost -12% | Troop Capacity +12,000	Dragon Scale Shield
Ogremire	5	264	+3	Civil	Building Speed +18% | Stamina Cost Down -12% | Troop Capacity +12,000	Ogre Club
Leona	5	236	+3	Civil	Safe Resources +18% | Reinforcement March Speed +12% | Troop ATK +45%	Puppet Partner
Sea Goddess	5	310	+3	Civil	Resource Gather Speed +12% | Medical Tent Healing Speed +18% | Troop Capacity +12,000	Coral Harp
Tala	5	310	+3	Civil	Research Speed +18% | Training Speed +18% | Troop Capacity +12,000	Nature's Staff
Violette	5	310	+3	Civil	Gather March Speed +12% | Stamina Cost Down -12% | Troop ATK +45%	Jester's Hat
Wu Kong	5	310	+3	Civil	Stamina Recovery +18% | Hunt March Speed +12% | Troop ATK +45%	Golden Staff
Anastasia	5	310	+2	All-round	Troop HP +20% | Troop DEF +20% | Troop ATK +20%	None
Aurora	5	310	+2	Civil	Gather March Speed +9% | Heal Stone Cost -8% | Rally Size +5,000	Arcane Serpent
Edmund	5	310	+2	Infantry	Infantry HP +20% | Infantry DEF +20% | Infantry ATK +20%	Sword of Light
Eris	5	310	+1	Cavalry	Cavalry HP +10% | Cavalry DEF +10% | Cavalry ATK +10%	None
Estelle	5	310	+1	Civil	Safe Resources +6% | Iron Output +6% | Troop ATK +15%	Cold-Blooded Dual Blades
Monica	5	310	+1	Civil	Medical Tent Capacity +6% | Heal Stone Cost -4% | Troop DEF +15%	Magic Mirror
Selantia	5	310	+1	Infantry	Infantry HP +10% | Infantry DEF +10% | Infantry ATK +10%	Ocean Pearl
```
## Prompt
You are a data archivist for the game "Puzzles & Chaos." I am providing screenshots of my hero inventory. Create a consolidated spreadsheet of my unique heroes with their precise stats.

### RESOURCES (CRITICAL)

* **Wiki Source:** Each hero has a dedicated page at `https://puzzles-chaos.fandom.com/wiki/{HeroName}` (spaces become underscores, e.g. `Kujo_Mamoru`). The full hero list is at `https://puzzles-chaos.fandom.com/wiki/Category:Heroes`.
* **Output Format:** Tab-Separated Values (TSV).

***

### STEP 1: VISUAL EXTRACTION (The Card Layout)

The images contain a grid of "Hero Cards" (3 columns wide). Treat each card as a structured data container.

**Card layout:**

* **NAME:** Centered white text near the bottom of the card (e.g., "Tania").
* **LEVEL:** Top-right corner, white text formatted as "Lv.XXX" (e.g., "Lv.350" → record as 350).
* **ENHANCEMENT:** Top-left corner, yellow text with "+" prefix (e.g., "+7"). If no "+" is visible, record as +0.
* **STARS:** Gold or red star icons below the hero name. Count them visually. A single red/outline star = 6-star hero.

**Deduplication:** Screenshots overlap. Process all images as one list and deduplicate by **Name**. If a hero appears in multiple screenshots, keep the entry with the clearest/most readable card.

**IMPORTANT — Read what is actually on the card. Do NOT guess or infer values. If text is unclear, flag it with \[?].**

***

### STEP 2: STAR COUNT VERIFICATION

After visual extraction, cross-check star counts against the wiki:

1. Look up the hero's **base rarity** (natural star level) on their wiki page.

2. **Rules:**

   * Base rarity < 5 → Star count = base rarity.
   * Base rarity = 5 AND Level < 310 → Star count = 5.
   * Base rarity = 5 AND Level ≥ 310 → Check the card for a **red/outline star** below the name. If present = 6. If not = 5.

3. If your visual count conflicts with what the wiki says is possible, trust the wiki's base rarity rules and re-examine the card.

***

### STEP 3: TROOP TYPE LOOKUP

Look up each hero's **Unit Type** on their wiki page in the info box near the top (the row labeled "Unit type"). Valid types: **Cavalry, Infantry, Archer, Civil, All-round**.

_Do NOT guess troop type from the card art or from the troop skill names. Always use the wiki info box._

***

### STEP 4: TROOP SKILL LOOKUP — HOW TO READ THE WIKI TABLES

Each hero's wiki page has a **"Troop Skill"** section containing multiple sub-sections. Each sub-section has a **header** (the skill name) followed by a **data table**.

#### 4A: SKIP the first sub-section called "Skill"

The first sub-section is always titled **"Skill"** — it describes the hero's combat damage ability (e.g., "Deals damage equals X% of troop ATK to enemy"). **IGNORE this entire sub-section.** It is NOT a troop buff.

#### 4B: Identify ALL remaining skill sub-sections by their EXACT headers

After "Skill", each hero has 2-3 additional skill sub-sections. **Read the EXACT header text for each one.** Do not rename or normalize them.

**CRITICAL: Skill headers vary between heroes.** Not every hero has matching skill types. Examples of headers you may encounter:

* Standard combat: "Cavalry HP", "Cavalry DEF", "Cavalry ATK", "Infantry HP", "Archer ATK", etc.
* General combat: "Troop HP", "Troop DEF", "Troop ATK" (buffs all troop types)
* Mixed-type: A single hero may have skills for DIFFERENT troop types. For example, Angelita (Archer type) has: "Archer ATK", "Cavalry ATK", and "Troop DEF". **Report the exact header names — do NOT change them to match the hero's unit type.**
* Civil skills: "Training Speed", "Research Speed", "Building Speed", "Stamina Cost Down", "Gathering Speed", "Resource Protection", "Troop Load", etc.

The wiki page also shows an expandable **Table of Contents** that lists the sub-section numbers and names (e.g., "1.2 Archer ATK", "1.3 Cavalry ATK — Unlock at level 31"). You can use this as a quick reference for the exact skill names.

#### 4C: Reading the buff skill tables

**FORMAT A — Heroes with base rarity 5★:** The table has **3 rows:**

* **Header row:** Blank | +0 | +1 | +2 | +3 | +4 | +5 | +6 | +7 | +8
* **Row 2 (labeled "5" with gold star):** Values at 5-star rarity.
* **Row 3 (labeled "6" with red star):** Values at 6-star rarity. Early cells may show "-".

**How to read:** Pick the ROW matching the hero's star count, and the COLUMN matching their enhancement level.

**Example — Tania (6★, +7), "Cavalry HP" table:** Row "6" (red star), Column "+7" → **+150%**

**FORMAT B — Heroes with base rarity ≤ 4★:** The table has **2 rows:**

* **Header row:** +0 | +1 | +2 | +3 | +4 | +5
* **Row 2:** Single row of values.

**How to read:** Find the column matching the hero's enhancement level.

#### 4D: Combine the results

For each buff skill sub-section (skipping "Skill"), format as: `{Exact Header Name} {Value}` Separate multiple skills with `|`.

**Example — Angelita (5★ base, now 6★, +5):** Her wiki Table of Contents shows: 1.2 Archer ATK, 1.3 Cavalry ATK, 1.4 Troop DEF

* "Archer ATK" table → Row 6, Column +5 → value from that cell
* "Cavalry ATK" table → Row 6, Column +5 → value from that cell
* "Troop DEF" table → Row 6, Column +5 → value from that cell
* Result: `Archer ATK +XX% | Cavalry ATK +XX% | Troop DEF +XX%`

#### 4E: Common errors to avoid

* **DO NOT** read values from the "Skill" table (the first one — combat damage, not a buff).
* **DO NOT** confuse the 5★ row with the 6★ row. A 6-star hero uses the 6★ (red star) row.
* **DO NOT** rename skill headers. If the wiki says "Troop HP", write "Troop HP" — not "Cavalry HP" even if the hero is Cavalry type.
* **DO NOT** assume all skills on a hero buff the same troop type. Read each header individually.
* **DO NOT** invent, calculate, or round values. Copy the exact number from the table cell.
* **DO NOT** assume all three buff skills have the same value — check each table individually.
* If a cell shows "-", that skill is not available at that star/enhancement combination. Note as "N/A".
* **If you cannot access a hero's wiki page, write `[wiki unavailable]` for that hero's Troop Skills and Curio. Do NOT fabricate values.**

***

### STEP 5: CURIO NAME

Each 5★+ hero's wiki page has an info box near the top of the page. One row in this info box is labeled **"Curio"**. It shows a small icon followed by the curio's name as text (e.g., "Sword of Omens" for Angelita, "Ocean Harp" for Tania).

Record the curio name exactly as shown. If the hero is below 5★ or has no curio listed, record as "None".

***

### STEP 6: OUTPUT FORMAT (TSV Code Block)

Generate a **Tab-Separated Values (TSV)** code block sorted by Enhancement (descending), then Level (descending), then Name (alphabetical).

**Columns:** Name | Stars | Level | Enhancement | Type | Troop Skills | Curio

* Use tabs between columns.
* Use `|` (space-pipe-space) to separate multiple troop skills within the Troop Skills column.
* Enhancement values should include the "+" prefix.

**Example rows (with correct wiki values):**

```
Name	Stars	Level	Enhancement	Type	Troop Skills	Curio
Tania	6	350	+7	Cavalry	Cavalry HP +150% | Cavalry DEF +150% | Cavalry ATK +150%	Ocean Harp
Fiona	6	348	+6	Civil	Training Speed +40% | Stamina Cost Down -24%	Dragon Horn
Angelita	6	350	+5	Archer	Archer ATK +150% | Cavalry ATK +150% | Troop DEF +150%	Sword of Omens
```

***

### ERROR HANDLING

* If a hero name is partially obscured, attempt to match it against the wiki's hero list.
* If a wiki page is missing or inaccessible for a hero, include the hero with visual data only and mark wiki-dependent columns with `[wiki unavailable]`. **Never fabricate data.**
* If any value seems inconsistent (e.g., Level 350 but Enhancement +1), flag it with `[verify]` but still include it.