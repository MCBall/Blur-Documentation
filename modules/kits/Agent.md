# Agent kit
Place flashbang mines to blind your foes.

3: Receive ONE extra flashbang mine and increased flash radius.
5: Receive TWO extra flashbang mines.
7: Receive ONE extra flashbang mine when you reload.

### Configuration options
General options:
- `base-radius` - Base radius for flashbang effective range.
- `max-placed-flashbangs` - Number of flashbangs a player can have placed at any given time. Flashbangs placed beyond this number will result in the oldest flashbang being removed.
- `flashbang-duration` - Duration of the flashbang effect on affected players.
- `max-held-flashbangs` - Number of flashbangs a player can have in their inventory at any given time.
- `explosion-delay` - Duration between a flashbang being triggered and it exploding.

Killstreak options:
- `ks-3-flashbangs` - Number of flashbangs to give a player when they achieve a 3 killstreak.
- `ks-3-radius` - Relative number to modify the `base-radius`. Usually an addition.
- `ks-5-flashbangs` - Number of flashbangs to give a player when they achieve a 5 killstreak.
- `ks-7-reload-flashbangs` - Number of flashbangs to give a player each time they reload after a 7 killstreak.

  ### Example/default configuration
  ```
  - Paintball:
    kit-configs:
    - agent:
        base-radius: 3
        max-placed-flashbangs: 2
        flashbang-duration: 5s
        max-held-flashbangs: 2
        explosion-delay: 0ms
        ks-3-flashbangs: 1
        ks-3-radius: ~+1
        ks-5-flashbangs: 2
        ks-7-reload-flashbangs: 1
  ```
  _**Note**: the `explosion-delay` option here causes the flashbang to go off on the next tick._
