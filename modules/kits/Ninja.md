# Ninja kit
Launch yourself with hookshots.

3 - Receive ONE extra hookshot and extended grappling range by 5 blocks. \
5 - Receive ONE extra hookshot. \
7 - Your team receives TWO hookshots and you gain 1 hookshot on each reload (max 2).

### Configuration options
General options:
- `base-range` - Base hookshot range.
- `max-hookshots` - Maximum number of hookshots a player can have.

Killstreak options:
- `ks-3-hookshots` - The number of hookshots given after a 3 killstreak.
- `ks-3-range` - Relative number affecting the hookshot range after a 3 killstreak.
- `ks-5-hookshots` - The number of hookshots given after a 5 killstreak.
- `ks-5-range` - Relative number affecting the hookshot range after a 5 killstreak.
- `ks-7-hookshots` - The number of hookshots given after a 7 killstreak.
- `ks-7-range` - Relative number affecting the hookshot range after a 7 killstreak.
- `ks-7-hookshots-on-reload` - The number of hookshots given when reloading after a 7 killstreak.

### Example/default configuration
```
- Paintball:
  kit-configs:
  - ninja:
      base-range: 15
      max-hookshots: 2
      ks-3-hookshots: 1
      ks-3-range: ~+5
      ks-5-hookshots: 1
      ks-5-range: ~+0
      ks-7-hookshots: 2
      ks-7-range: ~+0
      ks-7-hookshots-on-reload: 1
```
