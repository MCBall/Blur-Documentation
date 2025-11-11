# Vortex kit
Throw a vortex bomb that attracts entities nearby.

3 - The Vortex Bomb travels at a faster speed. \
5 - Cooldown reduced to 30 seconds. \
7 - Pull range increased to 5 blocks.

### Configuration options
General options:
- `player-accel-factor` - Acceleration (pull) factor applied to Player entities.
- `accel-factor` - Acceleration (pull) factor applied to non-Player entities.
- `base-cooldown` - Base duration of cooldown.
- `base-speed` - Base speed of the vortex bomb.
- `base-pull-range` - Base pull range of the vortex bomb.
- `vortex-duration` - Duration of vortex bomb existence.
- `entity-size` - Size of vortex bomb Block Display entity.
- `num-particles` - Number of particles around the vortex bomb.

Killstreak options:
- `ks-3-cooldown` - Relative duration to be applied to `base-cooldown` after a 3 killstreak.
- `ks-3-speed` - Relative number applied to `base-speed` after a 3 killstreak.
- `ks-5-cooldown` - Relative duration to be applied to `base-cooldown` after a 5 killstreak.
- `ks-7-cooldown` - Relative duration to be applied to `base-cooldown` after a 7 killstreak.
- `ks-7-range` - Relative number applied to `base-pull-range` after a 7 killstreak.


### Example/default configuration
```
- Paintball:
  kit-configs:
  - vortex:
      player-accel-factor: 1.5
      accel-factor: 1.0
      base-cooldown: 45s
      base-speed: 0.2
      base-pull-range: 5.0
      vortex-duration: 5s
      entity-size: 0.45
      num-particles: 8
      ks-3-cooldown: ~+0s
      ks-3-speed: ~+0.05
      ks-5-cooldown: ~+-15s
      ks-7-cooldown: ~+0s
      ks-7-range: ~+2
```
