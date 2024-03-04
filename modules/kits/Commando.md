# Agent kit
Reload faster. Press sneak while sprinting to dive and slide.

3 - Immediately reload and your reload time is reduced to 2 seconds. \
5 - Instantly reload until you die. \
7 - Your team receives instant reload for 30 seconds.

### Configuration options
General options:
- `duration` - Relative duration to reduce the base reload time by (e.g. if `duration` is -2 seconds, the reload time is reduced from 5 seconds to 3 seconds).
- `dive-cooldown` - Duration of dive ability cooldown.

Killstreak options:
- `ks-3-duration` - Relative duration to reduce the base reload time by (similarly to `duration`, this applies to the original 5 second reload time).
- `ks-7-team-duration` - Duration of team instant-reload on 7 killstreak.

### Example/default configuration
```
- Paintball:
  kit-configs:
  - commando:
      duration: ~+-2s
      dive-cooldown: 7s
      ks-3-duration: ~+-3s
      ks-7-team-duration: 30s
```
