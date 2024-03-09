# Magician kit
Wave your wand to make foes lose control of their movement.

3 - Spell cooldown reduces from 25 seconds to 20. \
5 - Spell effect duration increases from 5 seconds to 7. \
7 - Players hit by the spell will be blinded.

### Configuration options
General options:
- `base-cooldown` - Base duration of cooldown.
- `base-duration` - Base duration of spell effect.
- `base-radius` - Base radius of spell effect.

Killstreak options:
- `ks-3-cooldown` - Relative duration to be applied to `base-cooldown` after a 3 killstreak.
- `ks-3-duration` - Relative duration to be applied to `base-duration` after a 3 killstreak.
- `ks-5-cooldown` - Relative duration to be applied to `base-cooldown` after a 5 killstreak.
- `ks-5-duration` - Relative duration to be applied to `base-duration` after a 5 killstreak.
- `ks-7-cooldown` - Relative duration to be applied to `base-cooldown` after a 7 killstreak.
- `ks-7-duration` - Relative duration to be applied to `base-duration` after a 7 killstreak.


### Example/default configuration
```
- Paintball:
  kit-configs:
  - magician:
      base-cooldown: 25s
      base-duration: 5s
      base-radius: 5
      ks-3-cooldown: ~+-5s
      ks-3-duration: ~+0s
      ks-5-cooldown: ~+0s
      ks-5-duration: ~+2s
      ks-7-cooldown: ~+0s
      ks-7-duration: ~+0s
```
