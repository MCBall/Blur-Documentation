# Flash kit
Speed ahead of everyone with ease.

3 - Receive 30 seconds of speed II. \
5 - Receive 30 seconds of speed II and jump II. \
7 - Receive speed III when reloading. Your team receives speed II and jump II for 30 seconds.

### Configuration options
General options:
- `base-perma-speed-amp` - Base speed potion amplifier (basic speed I is amplifier 0, speed II is amplifier 1 etc.).

Killstreak options:
- `ks-3-speed-duration` - Duration of speed boost when a player achieves a 3 killstreak.
- `ks-3-speed-amp` - Speed potion amplifier when a player achieves a 3 killstreak.
- `ks-5-perma-speed-amp` - Speed potion amplifier applied to the player permanently after a 5 killstreak.
- `ks-5-jump-amp` - Jump potion amplifier when a player achieves a 5 killstreak.
- `ks-5-jump-duration` - Duration of jump boost when a player achieves a 5 killstreak.
- `ks-7-speed-amp` - Speed potion amplifier applied to the team when a player achieves a 7 killstreak.
- `ks-7-speed-duration` - Duration of speed boost applied to the team when a player achieves a 7 killstreak.
- `ks-7-jump-amp` - Jump potion amplifier applied to the team when a player achieves a 7 killstreak.
- `ks-7-jump-duration` - Duration of jump boost applied to the team when a player achieves a 7 killstreak.
- `ks-7-reload-speed-amp` - Speed potion amplifier applied when a player reloads after a 7 killstreak.
- `ks-7-reload-speed-duration` - Duration of speed boost applied when a player reloads after a 7 killstreak.

### Example/default configuration
```
- Paintball:
  kit-configs:
  - flash:
      base-perma-speed-amp: 0
      ks-3-speed-duration: 30s
      ks-3-speed-amp: 1
      ks-5-perma-speed-amp: 1
      ks-5-jump-amp: 1
      ks-5-jump-duration: 30s
      ks-7-speed-amp: 1
      ks-7-speed-duration: 30s
      ks-7-jump-amp: 1
      ks-7-jump-duration: 30s
      ks-7-reload-speed-amp: 2
      ks-7-reload-speed-duration: 3s
```
