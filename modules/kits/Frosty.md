# Frosty kit
Throw frost bombs to freeze your foes.

3 - Receive TWO extra freeze bombs. \
5 - Receive TWO extra freeze bombs. \
7 - Receive ONE extra freeze bomb when you reload.

### Configuration options
General options:
- `radius` - Radius for flashbang effective range.
- `freeze-duration` - Duration of the freeze effect on affected players.
- `slowness-duration` - Duration of the slowness effect on affected players.
- `snow-duration` - Duration that snow tiles placed by bombs will stay on the ground.
- `max-held-bombs` - Number of bombs a player can have in their inventory at any given time.

Killstreak options:
- `ks-3-bombs` - Number of bombs to give a player when they achieve a 3 killstreak.
- `ks-5-bombs` - Number of bombs to give a player when they achieve a 5 killstreak.
- `ks-7-reload-bombs` - Number of bombs to give a player each time they reload after a 7 killstreak.

### Example/default configuration
```
- Paintball:
  kit-configs:
  - frosty:
      radius: 4
      freeze-duration: 2s
      slowness-duration: 4s
      snow-duration: 6s
      max-held-bombs: 2
      ks-3-bombs: 2
      ks-5-bombs: 2
      ks-7-reload-bombs: 1
```
