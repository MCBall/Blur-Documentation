BControlPoints is the Blur control points module. It handles defining points and game logic for points being captured. There are many different options for this module that will be expanded on in this documentation in the future. The key parameters for the Conquest gamemode are highlighted below.

`BControlPoints` depends on `Extents` for the control point areas. Each point must have at least an `id`, `name`, and `capture` extent.

In addition to those, an `indicator` extent can be defined, within which all blocks of material `neutral-material` get replaced by `team-materials` when the relevant teams capture the point. The teams `id` fields here must match the team `id` field in the `Teams` module.

Example `BControlPoints` configuration:

```
- Extents:
  - id: shard-point
    cylinder:
      base: 64.5, 79.0, 55.5
      radius: 5.5
      height: 3
  - id: shard-indicator
    cuboid:
      min: 25, 50, 17
      max: 94, 100, 80
  - id: cavern-point
      cylinder:
        base: 0.5, 65.0, 0.5
        radius: 5.5
        height: 3

- BControlPoints:
    capture-time: 5s
    control-points:
    - id: shard
      name: Shard
      capture: shard-point
      indicator: shard-indicator
      neutral-material: EMERALD_BLOCK
      team-materials:
      - id: red
        material: RED_CONCRETE
      - id: blue
        material: BLUE_CONCRETE
    - id: cavern
      name: Cavern
      capture: cavern-point
```
