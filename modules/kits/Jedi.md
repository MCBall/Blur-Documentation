# Jedi kit
Wield a lightsaber and become one with the force!

3 - Regenerate Force energy faster. \
5 - Draw Force energy from lightsaber kills. \
7 - Increase the range of your Force abilities.

### Configuration options
General options:
- `base-force-pull-range` - Base range for force pull to have an effect.
- `base-regen` - Base regeneration rate of force energy (in energy per tick, 100 is full energy).

Killstreak options:
- `ks-3-regen` - Regeneration rate of force energy after a 3 killstreak.
- `ks-5-regen` - Regeneration rate of force energy after a 5 killstreak.
- `ks-7-regen` - Regeneration rate of force energy after a 7 killstreak.
- `lightsaber-kill-regen` - Force energy to regenerate from a lightsaber kill after a 5 killstreak.
- `ks-7-range-mult` - Multiplier applied to `base-force-pull-range` after a 7 killstreak.

### Example/default configuration
```
- Paintball:
  kit-configs:
  - jedi:
      base-force-pull-range: 24.0
      base-regen: 0.25
      ks-3-regen: 0.375
      ks-5-regen: 0.375
      ks-7-regen: 0.375
      lighsaber-kill-regen: 50
      ks-7-range-mult: 1.5
```
