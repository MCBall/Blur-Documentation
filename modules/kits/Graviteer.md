# Graviteer kit
Place down a Gravity Cannon and fly away!

3 - Gravity cannons will launch you further and have a reduced cooldown. \
5 - Gravity cannons have 2(+2) uses. \
7 - All teammates receive one gravity cannon that last until until death.

### Configuration options
General options:
- `base-cooldown` - Duration of base pad placement cooldown.
- `base-uses` - Base number of times players can use each pad.
- `base-multiplier` - Base velocity multiplier (speed) upon using a pad.
- `replaceable-blocks` - Materials of blocks that can be replaced by pads.
- `place-above-blocks` - Materials of non-solid blocks that pads can be placed above.

Killstreak options:
- `ks-3-cooldown` - Relative duration to modify `base-cooldown` on a 3 killstreak.
- `ks-3-uses` - Relative number to modify `base-uses` on a 3 killstreak.
- `ks-3-multiplier` - Velocity multiplier (speed) upon using a pad placed after a 3 killstreak.
- `ks-5-cooldown` - Relative duration to modify `base-cooldown` on a 5 killstreak.
- `ks-5-uses` - Relative number to modify `base-uses` on a 5 killstreak.
- `ks-7-cooldown` - Relative duration to modify `base-cooldown` on a 7 killstreak.
- `ks-7-uses` - Relative number to modify `base-uses` on a 7 killstreak.


### Example/default configuration
```
- Paintball:
  kit-configs:
  - graviteer:
      base-cooldown: 30s
      base-uses: 2
      base-multiplier: 2
      ks-3-cooldown: ~+-10s
      ks-3-uses: ~+0
      ks-3-multiplier: 3
      ks-5-cooldown: ~+0s
      ks-5-uses: ~+2
      ks-7-cooldown: ~+0s
      ks-7-uses: ~+0
      replaceable-blocks:
      - GRASS
      - SNOW
      place-above-blocks:
      - FARMLAND
      - DIRT_PATH
```
_**Note**: `replaceable-blocks` doesn't cover all replaceable blocks as some are covered by material tags. Tag options may be added at a later date when a serializer is written for them._
