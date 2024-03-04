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
- [Agent](modules/kits/Agent.md)
- [Commando](modules/kits/Commando.md)
- [Demo](modules/kits/Demo.md)
- [Flash](modules/kits/Flash.md)
- [Frosty](modules/kits/Frosty.md)
- [Graviteer](modules/kits/Graviteer.md)
- [Jedi](modules/kits/Jedi.md)
- [Magician](modules/kits/Magician.md)
- [Magneto](modules/kits/Magneto.md)
- [Mercy](modules/kits/Mercy.md)
- [Ninja](modules/kits/Ninja.md)
- [Protection](modules/kits/Protection.md)
- [Ricochet](modules/kits/Ricochet.md)
- [Shotty](modules/kits/Shotty.md)
- [Sniper](modules/kits/Sniper.md)
- [Spider](modules/kits/Spider.md)
- [Vortex](modules/kits/Vortex.md)
