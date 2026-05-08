# Flashcard Decks — Public Deck Catalog

This is the public deck catalog for the **Flashcards** app by [Temperate Designs](https://github.com/Temperate-Designs). It hosts community-accessible flashcard decks in YAML format that can be downloaded directly within the app via the **Deck Catalog** screen.

## Decks

| Deck | Description |
|------|-------------|
| US Citizenship Test | All 100 civics questions for the naturalization test |
| US Citizenship Test (2025 - 128 Questions) | 2025 version with 128 civics questions. Must answer 12 of 20 correctly to pass. |

## Deck Format

Decks are plain YAML files stored in the `decks/` directory. See the [Flashcards app YAML Quick Start](https://github.com/Temperate-Designs/flashcards/blob/main/YAML_QUICK_START.md) for the full format specification.

## manifest.json

The `manifest.json` file at the root of this repository is the machine-readable catalog consumed by the app. Each entry has the following fields:

```json
{
  "decks": [
    {
      "id": "unique_deck_id",
      "name": "Human-readable deck name",
      "description": "Short description shown in the catalog",
      "version": 1,
      "filename": "decks/filename.yaml"
    }
  ]
}
```

- **id** — Stable unique identifier. Used to match catalog entries against decks already installed on a user's device.
- **name** — Display name shown in the Deck Catalog screen.
- **description** — One-sentence description shown below the name.
- **version** — Integer. Increment this when the deck content changes so the app can offer an update to users.
- **filename** — Path to the YAML file relative to the repository root.

## Contributing

Contributions are welcome! If you have a deck you'd like to add to the catalog, please open a Pull Request:

1. Add your deck YAML file to the `decks/` directory.
2. Add a corresponding entry to `manifest.json` with a unique `id` and `version: 1`.
3. Open a PR with a brief description of the deck and its source/license.

Please ensure deck content is accurate and appropriately licensed before submitting.
