# `Parkour` module

The Parkour module manages a parkour or jumping puzzle area. When a player leaves the extent `area` they are teleported back to their previous checkpoint from the list of `checkpoints`.

Example `Parkour` configuration:

```
- Extents:
  - id: parkour-bounds
    cuboid: { min: '-212, 104, -199', max: '-128, 215, -69' }
  - id: parkour-check-0
    cuboid: { min: '-169, 139, -114', max: '-159, 143, -109' }
  - id: parkour-check-1
    cuboid: { min: '-174, 127, -141', max: '-169, 131, -139' }
  - id: parkour-check-2
    cuboid: { min: '-158, 127, -155', max: '-154, 130, -149' }
- Parkour:
    area: parkour-bounds
    checkpoints:
    - parkour-check-0
    - parkour-check-1
    - parkour-check-2
```
