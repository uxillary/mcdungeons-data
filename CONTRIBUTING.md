# Contributing to Optimancer

Thank you for your interest in contributing to **Optimancer's data project!**  
This project aims to build a comprehensive, community-driven database for Minecraft Dungeons item optimization.

We welcome all contributions, whether it’s adding new items, updating enchantments, suggesting combos, or fixing errors.

---

## 🚀 How to Contribute

### 1. Fork This Repository
Click the **Fork** button in the top-right corner to create your own copy of this repo.

### 2. Create a New Branch
Name your branch something like:
```
add-katana-data
```

### 3. Make Your Changes
Edit the relevant JSON files in the `/data` folder.

### 4. Validate Your JSON
Make sure your JSON is correctly formatted.  
You can use:
- [https://jsonlint.com](https://jsonlint.com)
- VSCode with the built-in JSON formatter
- GitHub’s automatic validation (if workflow is enabled)

### 5. Submit a Pull Request (PR)
Open a PR with a clear title like:
```
Add missing enchantments for Katana
```
In your PR description, briefly explain what you added or changed.

---

## 📐 JSON Data Structure

### Items (`data/items.json`)
Each item should follow this structure:
```json
{
  "name": "Katana",
  "type": "Melee",
  "possibleEnchants": ["Thundering", "Busy Bee", "Sharpness"],
  "metaRating": 7.5,
  "synergyNotes": "Works well with speed and AoE builds."
}
```
| Field | Type | Description |
|-------|------|-------------|
| name | string | Item name |
| type | string | Melee, Ranged, Armor, Artifact |
| possibleEnchants | array | List of compatible enchantments |
| metaRating | number | 1-10 rating based on current meta relevance |
| synergyNotes | string | Additional synergy or combo notes |

---

### Enchants (`data/enchants.json`)
Each enchantment should follow this structure:
```json
{
  "name": "Thundering",
  "type": "Damage",
  "conflictsWith": ["Busy Bee"]
}
```
| Field | Type | Description |
|-------|------|-------------|
| name | string | Enchant name |
| type | string | Damage, Defense, Utility |
| conflictsWith | array | Enchantments that can't coexist |

---

### Combos (`data/combos.json`)
Each combo build should follow this structure:
```json
{
  "buildName": "Speed Bee Build",
  "items": ["Katana", "Swift Boots"],
  "enchants": ["Busy Bee", "Swirling"],
  "synergyScore": 9.0,
  "notes": "Great for mobbing, weak against bosses."
}
```
| Field | Type | Description |
|-------|------|-------------|
| buildName | string | Combo or build nickname |
| items | array | Items used in the build |
| enchants | array | Suggested enchantments |
| synergyScore | number | 1-10 synergy rating |
| notes | string | Strengths, weaknesses, or tips |

---

## 🧑‍💻 What Can You Contribute?
- 📄 Add missing items
- ✏️ Add or update enchantments
- ⚙️ Suggest new combo builds
- 🔍 Fix errors or typos
- 📊 Propose meta updates based on gameplay trends
- 🧪 Suggest data structure improvements

---

## ✅ JSON Formatting Rules
- Use **double quotes** `" "` for all keys and string values.
- No trailing commas.
- Keep array elements consistently formatted.
- Validate your JSON before submitting.

---

## 🙌 Contribution Notes
- Feel free to open an issue if you want to suggest changes or discuss structure.
- All contributions, big or small, are appreciated.

Thank you for helping make Optimancer awesome!
