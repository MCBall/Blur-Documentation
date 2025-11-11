# Spider kit
Scale walls and shoot web bombs.

3 - Receive ONE extra web bomb. \
5 - Receive ONE extra web bomb when you reload. \
7 - Your team receives climbing ability for 30 seconds.

### Configuration options
General options:
- `scale-radius` - Radius of spider climb vines.
- `bomb-radius` - Radius of web bombs.
- `web-duration` - The duration for which web bombs stay before dissipating.
- `max-bombs` - Maximum number of web bombs a player can have.

Killstreak options:
- `ks-3-bombs` - The number of web bombs given after a 3 killstreak.
- `ks-5-bombs-on-reload` - The number of web bombs given when reloading after a 5 killstreak.
- `ks-7-duration` - Duration of team spider climbing after a 7 killstreak.


### Example/default configuration
```
- Paintball:
  kit-configs:
  - spider:
      scale-radius: 3
      bomb-radius: 4
      web-duration: 4s
      max-bombs: 2
      ks-3-bombs: 2
      ks-5-bombs-on-reload: 1
      ks-7-duration: 30s
```
