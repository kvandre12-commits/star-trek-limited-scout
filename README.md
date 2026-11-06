# Star Trek Limited Scout

A mobile-friendly **Magic: The Gathering | Star Trek** Limited scouting site
for Sealed and Pick-Two Draft. It loads all unique `set:trk` cards from
Scryfall and keeps card power separate from rarity-based accessibility.

## Features

- Curated board wipes, targeted removal, and Limited bomb candidates
- Cards grouped by rarity so commons/uncommons stay visible
- Ten selectable two-color archetypes plus a set-mechanics view
- Color filtering across every category
- Pick-Two and Sealed curve-planning modes
- Separate **Power**, **Access**, and **Planning Rank** labels
- Responsive card-image gallery with Oracle text and Scryfall links

The rankings are transparent heuristics, not game win-rate data, exact booster
odds, or a replacement for reading the actual card. Cardboard remains rude.

## Run locally

```bash
python serve.py --port 8780
```

Then open <http://127.0.0.1:8780/>.

## Method

Scryfall supplies live card facts and images. Curated category names,
archetype definitions, and scoring logic live in `index.html`.

- **Power** estimates Limited efficiency, interaction, evasion, resilience,
  and card advantage.
- **Access** is a broad rarity tier: High (common), Medium (uncommon), Low
  (rare), or Very low (mythic). It is not an exact pull probability.
- **Planning Rank** adds a small accessibility and format-flexibility bonus to
  Power. It helps identify repeatable deck foundations; it is not pick order.

## License and acknowledgements

Source code is MIT licensed. Card data and images come from
[Scryfall](https://scryfall.com/). This unofficial Fan Content is not approved
or endorsed by Wizards of the Coast. Portions of the materials used are
property of Wizards of the Coast. © Wizards of the Coast LLC.
