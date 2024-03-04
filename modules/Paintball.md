# `Paintball` module

The Paintball module handles the combat system in MCBall. It includes the killing, respawns, inventory management, and all kits. The module has extensive configuration options, detailed below and in individual kit config pages (see below for these).

- `reload-duration` - Paintball reload duration.
- `fix-velocity` - Whether to apply our paintball velocity fix (don't add player vertical velocity to paintball velocity).
- `invulnerability-time` - Duration that a player is invulnerable after spawning (spawn shield).
- `enabled-kits` - List of kit names that are enabled on this map. If this option is used, all kits not included will be disabled.
- `disabled-kits` - List of kit names that are disabled on this map. This takes precedence over `enabled-kits`.
- `force-kit` - A kit name to force on all players. This option will override all player choice and permissions limitations.
- `allow-trapdoors` - Whether players can open and close trapdoors on the map.
- `allow-doors` - Whether players can open and close doors on the map.
- `allow-buttons` - Whether players can activate buttons on the map.
- `num-paintballs` - The number of paintballs players start with.
- `kit-configs` - A list of kit configuration modifications. Any values not specified here will be their default values.

Example `Paintball` configuration (all values here are their defaults, except for `enabled-kits`, `disabled-kits`, and `kit-configs`):

```
- Paintball:
    reload-duration: 5s
    fix-velocity: true
    invulnerability-time: 2s
    enabled-kits:
    - jedi
    - sniper
    - magneto
    disabled-kits:
    - ninja
    - vortex
    - shotty
    force-kit: jedi
    allow-trapdoors: false
    allow-doors: true
    allow-buttons: true
    num-paintballs: 64
    kit-configs:
    - jedi:
        base-force-pull-range: 12.3
        base-regen: 10.0
    - sniper:
        base-cooldown: 1s
    - demo:
        radius: 16
        restoreDelayInterval: 20ms
```
_**Note**: the options here for `enabled-kits` would render `disabled-kits` essentially pointless._

## Kit options
Each kit has options specific to its abilities. Use the links below to access them.
- [Agent](kits/Agent.md)
- [Commando](kits/Commando.md)
- [Demo](kits/Demo.md)
- [Flash](kits/Flash.md)
- [Frosty](kits/Frosty.md)
- [Graviteer](kits/Graviteer.md)
- [Jedi](kits/Jedi.md)
- [Magician](kits/Magician.md)
- [Magneto](kits/Magneto.md)
- [Mercy](kits/Mercy.md)
- [Ninja](kits/Ninja.md)
- [Protection](kits/Protection.md)
- [Ricochet](kits/Ricochet.md)
- [Shotty](kits/Shotty.md)
- [Sniper](kits/Sniper.md)
- [Spider](kits/Spider.md)
- [Vortex](kits/Vortex.md)
