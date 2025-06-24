# Optimancer Data Repository

This is the public data source for **Optimancer**, a Minecraft Dungeons gear optimization tool.

We aim to build an open, community-driven database of:
- Items
- Enchantments
- Synergy combos
- Meta trends

## 🔥 Contributing
Help us expand and verify the data!

## 📂 Repository Structure
- `data/items.json` – List of all weapons and armor.
- `data/enchants.json` – List of all enchantments with types.
- `data/combos.json` – Known synergies and suggested builds.

## 💬 Get Involved
Raise an issue, suggest changes, or open a pull request.

# Contributing to Optimancer Data

Thank you for helping us build the best Minecraft Dungeons gear database!

## ✅ How to Contribute
1. Fork the repo.
2. Add or update JSON files in `/data`.
3. Open a Pull Request (PR).

## 📐 Data Structure
### Items (items.json)
```
{
  "name": "Katana",
  "type": "Melee",
  "possibleEnchants": ["Thundering", "Busy Bee", "Sharpness"],
  "metaRating": 7.5,
  "synergyNotes": "Works well with speed and AoE builds."
}
```

### Enchants (enchants.json)
```
{
  "name": "Thundering",
  "type": "Damage",
  "conflictsWith": ["Busy Bee"]
}
```

### Combos (combos.json)
```
{
  "buildName": "Speed Bee Build",
  "items": ["Katana", "Swift Boots"],
  "enchants": ["Busy Bee", "Swirling"],
  "synergyScore": 9.0,
  "notes": "Great for mobbing, weak against bosses."
}
```

## ✅ Validation
Please ensure your JSON is valid! You can use tools like https://jsonlint.com.
 ~ workflow will validate before PRs

## Structure
```
optimancer-data/
│
├── data/
│   ├── items.json
│   ├── enchants.json
│   └── combos.json
│
├── .github/
│   └── workflows/
│       └── validate-json.yml  # Optional JSON validation
│
├── README.md
├── CONTRIBUTING.md
└── LICENSE (MIT recommended)
```

