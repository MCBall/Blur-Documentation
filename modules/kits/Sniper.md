# Sniper kit
Blast foes from a distance using a high powered sniper rifle.

3 - Sniper Rifle becomes lightweight, making you run faster when holding it. \
5 - Sniper Rifle receives a muzzle suppresor. \
7 - Sniper Rifle's cooldown reduced from 25 seconds to 15 seconds.

### Configuration options
General options:
- `base-cooldown` - Base duration of cooldown.
- `range` - Range of sniper shot.

Killstreak options:
- `ks-3-cooldown` - Relative duration to be applied to `base-cooldown` after a 3 killstreak.
- `ks-5-cooldown` - Relative duration to be applied to `base-cooldown` after a 5 killstreak.
- `ks-7-cooldown` - Relative duration to be applied to `base-cooldown` after a 7 killstreak.


### Example/default configuration
```
- Paintball:
  kit-configs:
  - sniper:
      base-cooldown: 25s
      range: 200
      ks-3-cooldown: ~+0s
      ks-5-cooldown: ~+0s
      ks-7-cooldown: ~+-10s
```
