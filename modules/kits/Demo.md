# Demo kit
Blow your path open with C4! After using your C4 you receive another C4 45 seconds later.

3 - C4 kills enemies. \
5 - Your C4 explodes on contact. \
7 - Have a maximum of 2 C4s.

### Configuration options
General options:
- `radius` - Effective radius of C4 explosions.
- `restore-delay-initial` - Duration between C4 explosion and first block being restored.
- `restore-delay-interval` - Duration between blocks being restored.
- `max-c4` - Maximum C4 bombs a player can have in their inventory.
- `base-cooldown` - Duration a player must wait to receive an extra C4 bomb.

Killstreak options:
- `ks-3-cooldown` - Relative duration to modify `base-cooldown` on a 3 killstreak.
- `ks-5-cooldown` - Relative duration to modify `base-cooldown` on a 5 killstreak.
- `ks-7-cooldown` - Relative duration to modify `base-cooldown` on a 7 killstreak.

### Example/default configuration
```
- Paintball:
  kit-configs:
  - demo:
      radius: 3
      restore-delay-initial: 55s
      restore-delay-interval: 200ms
      max-c4: 2
      base-cooldown: 45s
      ks-3-cooldown: ~+0s
      ks-5-cooldown: ~+0s
      ks-7-cooldown: ~+0s
```
_**Note**: the killstreak cooldown modifiers are not used by default (hence they are all +0s)._
