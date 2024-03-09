# Magneto kit
Reflect paintballs from yourself when reloading.

3 - Reflect for 3 seconds when you return a flag. \
5 - Reflect for 3 seconds when you pick up a flag. \
7 - Reflect for 3 seconds if you get hit by a paintball.

### Configuration options
General options:
- `base-cooldown` - Base duration of cooldown.
- `base-radius` - Base radius of reflecting effect.

Killstreak options:
- `ks-3-cooldown` - Relative duration to be applied to `base-cooldown` after a 3 killstreak.
- `ks-3-duration` - Duration of reflection when returning a flag after a 3 killstreak.
- `ks-5-cooldown` - Relative duration to be applied to `base-cooldown` after a 5 killstreak.
- `ks-5-duration` - Duration of reflection when picking up a flag after a 5 killstreak.
- `ks-7-cooldown` - Relative duration to be applied to `base-cooldown` after a 7 killstreak.
- `ks-7-duration` - Duration of reflection when hit by a paintball after a 7 killstreak.


### Example/default configuration
```
- Paintball:
  kit-configs:
  - magneto:
      base-cooldown: 23s
      base-radius: 3
      ks-3-cooldown: ~+0s
      ks-3-duration: 3s
      ks-5-cooldown: ~+0s
      ks-5-duration: 3s
      ks-7-cooldown: ~+0s
      ks-7-duration: 3s
```
