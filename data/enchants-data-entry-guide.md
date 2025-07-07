# ✨ Enchants Data Entry Guide

This guide explains how to correctly add and structure entries in `enchants.json` for the Minecraft Dungeons optimization project.

---

## ✅ Example Entry

\`\`\`json
{
  "id": "radiance",
  "name": "Radiance",
  "description": "Has a chance to spawn a circular healing area on hit.",
  "type": "healing",
  "rarity": "rare",
  "maxTiers": 3,
  "cooldownSeconds": null,
  "activationChance": "20% at Tier I, 30% at Tier II, 40% at Tier III",
  "conflictsWith": [],
  "synergyWith": ["leeching", "critical_hit"],
  "tags": ["melee", "survivability", "healing"],
  "image": "https://yourcdn.com/images/enchants/radiance.png",
  "tooltip": "Has a chance to spawn a healing circle that restores health.",
  "addedInVersion": "1.0",
  "notes": "Healing circle effect stacks with other healing enchants.",
  "availableOn": ["melee"],
  "gildable": true,
  "canAppearInTower": true,
  "dlc": null
}
\`\`\`

---

## 🔍 Field Definitions

| Field | Required | Description |
|-------|----------|-------------|
| `id` | ✅ | Unique identifier (lowercase, underscores). |
| `name` | ✅ | Display name of the enchant. |
| `description` | ✅ | Detailed effect description. |
| `type` | ✅ | Enchant type: `damage`, `healing`, `crowd_control`, `utility`, etc. |
| `rarity` | ✅ | Enchant rarity: `common`, `rare`, `unique`. |
| `maxTiers` | ✅ | Maximum upgrade tiers (usually 1-3). |
| `cooldownSeconds` | ❌ | Cooldown time (in seconds) or `null` if not applicable. |
| `activationChance` | ✅ | Activation chance per tier or description string. |
| `conflictsWith` | ✅ | Array of enchant IDs that cannot be used together. |
| `synergyWith` | ✅ | Array of enchant IDs that work well together. |
| `tags` | ✅ | Keywords for filtering: melee, ranged, survivability, damage, etc. |
| `image` | ✅ | Full URL to the enchant's image/icon. |
| `tooltip` | ✅ | Quick in-game style description (one sentence). |
| `addedInVersion` | ✅ | Game version when the enchant was introduced. |
| `notes` | ❌ | Additional useful info, quirks, or stacking effects. |
| `availableOn` | ✅ | Array of item types this enchant can appear on (melee, ranged, armor). |
| `gildable` | ✅ | `true` if enchant can appear on gilded items. |
| `canAppearInTower` | ✅ | `true` if enchant can appear in the tower. |
| `dlc` | ❌ | Name of DLC if enchant is exclusive, else `null`. |

---

## 🛠 Tips for Contributors

- **Keep IDs lowercase** with underscores: `critical_hit`
- **Cross-check enchant IDs** with existing files to prevent duplicates.
- **Use full image URLs** following the shared CDN/image path pattern.
- **Cooldown and activationChance** should be accurate when available, or use `null`/estimates.
- **Use consistent tags** (examples: melee, ranged, aoe, survivability, damage, healing).
- **Leave DLC as `null`** if the enchant is in the base game.

---

## 🚩 Submission Checklist

- [ ] Unique `id` used
- [ ] Enchant conflicts and synergies verified
- [ ] Image URL tested and working
- [ ] All required fields completed
- [ ] JSON formatting validated

---

### 📢 Contact

For questions, corrections, or large submissions, please open an issue or contact a maintainer.
