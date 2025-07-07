# 📦 Items Data Entry Guide

This guide explains how to correctly add and structure entries in `items.json` for the Minecraft Dungeons optimization project.

Each item should follow this schema to ensure consistency and scalability.

---

## ✅ Example Entry

\`\`\`json
{
  "id": "katana",
  "name": "Katana",
  "type": "melee",
  "subtype": "sword",
  "unique": false,
  "gildable": true,
  "basePower": 145,
  "rarity": "common",
  "dlc": null,
  "possibleEnchants": ["thundering", "busy_bee", "sharpness"],
  "metaRating": 7.5,
  "tags": ["speed", "aoe", "damage"],
  "synergyNotes": "Works well with speed and AoE builds.",
  "recommendedBuilds": ["glass_cannon_speed", "crowd_control"],
  "image": "https://yourcdn.com/images/items/katana.png",
  "tooltip": "A swift blade that excels at cutting through mobs with speed.",
  "addedInVersion": "1.0",
  "notes": "Can be found in Soggy Cave and Desert Temple.",
  "canBeGilded": true,
  "canBeAncient": true,
  "availableInTower": true
}
\`\`\`

---

## 🔍 Field Definitions

| Field | Required | Description |
|-------|----------|-------------|
| `id` | ✅ | Unique identifier (lowercase, underscores). |
| `name` | ✅ | Display name. |
| `type` | ✅ | Item type: `melee`, `ranged`, `armor`, `artifact`. |
| `subtype` | ✅ | Further classification: `sword`, `axe`, `bow`, etc. |
| `unique` | ✅ | `true` if this is a unique item variant. |
| `gildable` | ✅ | `true` if the item can appear as gilded. |
| `basePower` | ✅ | Typical base power level (use best estimate if variable). |
| `rarity` | ✅ | Common, rare, unique, etc. |
| `dlc` | ❌ | Set to DLC name or `null` if base game. |
| `possibleEnchants` | ✅ | Array of enchant IDs that can roll on this item. |
| `metaRating` | ✅ | A curated 1-10 balance rating based on community/meta. |
| `tags` | ✅ | Keywords to help with filtering (speed, AoE, survivability, etc.). |
| `synergyNotes` | ✅ | Brief explanation of the item's synergy potential. |
| `recommendedBuilds` | ❌ | List of predefined builds this item works well in. |
| `image` | ✅ | Full URL to the item’s image/icon. |
| `tooltip` | ✅ | A short game-style description (one sentence). |
| `addedInVersion` | ✅ | Game version when this item was introduced. |
| `notes` | ❌ | Additional useful info (drop locations, quirks, etc.). |
| `canBeGilded` | ✅ | `true` or `false`. Explicit gilding flag. |
| `canBeAncient` | ✅ | `true` or `false`. Can this appear as an ancient variant? |
| `availableInTower` | ✅ | `true` or `false`. Can this item spawn in the tower? |

---

## 🛠 Tips for Contributors

- **Keep IDs lowercase** with underscores: `flail_of_the_forge`
- **Use accurate enchant IDs** from the `enchants.json` file.
- **Use full image URLs** or follow the shared CDN/image path pattern.
- **BasePower** can be estimated if it varies but try to reflect typical drop levels.
- **MetaRating** is subjective but aim to keep scores consistent across similar items.
- **Leave DLC as `null`** if the item is available in the base game.

---

## 🚩 Submission Checklist

- [ ] Unique `id` used
- [ ] Enchant IDs cross-checked with `enchants.json`
- [ ] Image URL tested and correct
- [ ] All required fields completed
- [ ] JSON formatting validated

---

### 📢 Contact

For questions, corrections, or large data submissions, please open an issue or contact a maintainer.
