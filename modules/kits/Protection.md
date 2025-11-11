# Protection kit
Bring extra protection into the battlefield.

3 - Gain SPEED II for 3 seconds upon protective vest destruction. \
5 - The protective vests are rigged with flashbangs that blind enemies within 5 blocks of its wearer. \
7 - The protective vests become strong enough to resist a sniper bullet.

### Configuration options
General options:
- `base-cooldown` - Base duration of cooldown.

Killstreak options:
- `ks-3-cooldown` - Relative duration to be applied to `base-cooldown` after a 3 killstreak.
- `ks-3-speed-duration` - Duration of speed effect applied after a 3 killstreak.
- `ks-5-cooldown` - Relative duration to be applied to `base-cooldown` after a 5 killstreak.
- `ks-5-flashbang-radius` - Radius of flashbang effect when hit after a 5 killstreak.
- `ks-5-flashbang-duration` - Duration of flashbang effect when hit after a 5 killstreak.
- `ks-7-cooldown` - Relative duration to be applied to `base-cooldown` after a 7 killstreak.


### Example/default configuration
```
- Paintball:
  kit-configs:
  - protection:
      base-cooldown: 30s
      ks-3-cooldown: ~+0s
      ks-3-speed-duration: 3s
      ks-5-cooldown: ~+0s
      ks-5-flashbang-radius: 5
      ks-5-flashbang-duration: 5s
      ks-7-cooldown: ~+0s
```
