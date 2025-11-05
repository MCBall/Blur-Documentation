# `Paintball` module

The PaintballPractice module emulates just the throwing paintballs aspect of the [Paintball](Paintball.md) module. It also adds target pigs that give an audible and visual indicator when hit. 

- `reload-duration` - Paintball reload duration.
- `fix-velocity` - Whether to apply our paintball velocity fix (don't add player vertical velocity to paintball velocity).
- `hotbar-slot` - The player hotbar slot to hold paintballs.
- `targets` - A list of locations at which to spawn target pigs.


Example `Paintball` configuration (all values here are their defaults, except for `targets`):

```
- PaintballPractice:
    reload-duration: 5s
    fix-velocity: true
    hotbar-slot: 0
    targets:
    - 28.5, 95, -4.5, 105, 36
    - 23.5, 88, 13.5, 147.5, 19
    - -11.5, 96, 15.5, -163.5, 6
```
