# Shotty kit
Blast your foes away at close range with a shotgun.

3 - Your shotgun cooldown decreases from 12 seconds to 8 seconds. \
5 - Your shotgun spread increases from 30 degrees to 45 degrees. \
7 - Your shotgun range increases from 10 blocks to 15 blocks.

### Configuration options
General options:
- `base-cooldown` - Base duration of cooldown.
- `base-spread` - Base angular spread of shotgun paintballs.
- `base-shots` - Base paintballs per shotgun shot.
- `base-range` - Base range of shotgun paintballs.
- `base-speed` - Base speed of shotgun paintballs.

Killstreak options:
- `ks-3-cooldown` - Relative duration to be applied to `base-cooldown` after a 3 killstreak.
- `ks-3-spread` - Relative number of degrees to be applied to `base-spread` after a 3 killstreak.
- `ks-3-shots` - Relative number of shots to be applied to `base-shots` after a 3 killstreak.
- `ks-3-range` - Relative number of blocks to be applied to `base-range` after a 3 killstreak.
- `ks-3-speed` - Relative number to be applied to `base-speed` after a 3 killstreak.
- `ks-5-cooldown` - Relative duration to be applied to `base-cooldown` after a 5 killstreak.
- `ks-5-spread` - Relative number of degrees to be applied to `base-spread` after a 5 killstreak.
- `ks-5-shots` - Relative number of shots to be applied to `base-shots` after a 5 killstreak.
- `ks-5-range` - Relative number of blocks to be applied to `base-range` after a 5 killstreak.
- `ks-5-speed` - Relative number to be applied to `base-speed` after a 5 killstreak.
- `ks-7-cooldown` - Relative duration to be applied to `base-cooldown` after a 7 killstreak.
- `ks-7-spread` - Relative number of degrees to be applied to `base-spread` after a 7 killstreak.
- `ks-7-shots` - Relative number of shots to be applied to `base-shots` after a 7 killstreak.
- `ks-7-range` - Relative number of blocks to be applied to `base-range` after a 7 killstreak.
- `ks-7-speed` - Relative number to be applied to `base-speed` after a 7 killstreak.

### Example/default configuration
```
- Paintball:
  kit-configs:
  - shotty:
      base-cooldown: 12s
      base-spread: 30
      base-shots: 10
      base-range: 10.0
      base-speed: 2.0
      ks-3-cooldown: ~+-4s
      ks-3-spread: ~+0
      ks-3-shots: ~+0
      ks-3-range: ~+0
      ks-3-speed: ~+0
      ks-5-cooldown: ~+0s
      ks-5-spread: ~+15
      ks-5-shots: ~+0
      ks-5-range: ~+0
      ks-5-speed: ~+0
      ks-7-cooldown: ~+0s
      ks-7-spread: ~+0
      ks-7-shots: ~+0
      ks-7-range: ~+5
      ks-7-speed: ~+0
```
