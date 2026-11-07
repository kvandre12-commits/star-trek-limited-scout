---
name: star-trek-limited-scout
description: Magic The Gathering Star Trek (TRK) Sealed and Pick-Two Draft assistant. Use for TRK draft picks, sealed pools, board wipes, targeted removal, bombs, mechanics, archetypes, strategy, card advantage, aggression, mana curves, or launching the bundled Scryfall-powered card sorter.
version: "1.1.0"
author: Kurtis and SharpEdge
tags:
  - magic-the-gathering
  - mtg
  - star-trek
  - trk
  - limited
  - pick-two
  - sealed
  - scryfall
---

# Star Trek Limited Scout

Use the bundled `index.html` as the source of truth for curated categories,
mechanic themes, strategy field notes, and ranking implementation. It loads unique `set:trk` cards
from Scryfall at runtime.

## Launch

```bash
python ~/.code_puppy/skills/star-trek-limited-scout/serve.py --port 8780
```

Verify HTTP 200 before saying the site is running, then provide:

```text
http://127.0.0.1:8780/
```

## Pick advice

1. Inspect all visible candidates, current pool, colors, curve, and pick/pack.
2. Recommend the Pick-Two pair first and one fallback pair.
3. Prioritize efficient interaction, reliable threats, card advantage, curve,
   and fixing. Apply synergy only when the pool supports it.
4. Use commons and uncommons to describe format foundations. Do not let rarity
   make a visible bomb look weaker; Access is planning frequency, not pick order.
5. Separate card facts from estimates. Never invent exact collation, pull odds,
   ALSA, GIH win rate, or format statistics.

## Maintenance

- Keep the app framework-free and mobile friendly.
- Escape external data inserted through `innerHTML`.
- Preserve polite delays between paginated Scryfall requests.
- Validate JavaScript and smoke-test localhost after changes.
- Manually audit curated lists when Oracle text changes.
