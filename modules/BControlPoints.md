BControlPoints is the Blur control points module. It handles defining points and game logic for points being captured. There are many different options for this module that will be expanded on in this documentation in the future. The key parameters for the Conquest gamemode are highlighted below.

`BControlPoints` depends on `Extents` for the control point areas. Each point must have at least an `id`, `name`, and `capture` extent.

## Point Capture Indicators
An `indicator` extent can be defined, within which all blocks of material `neutral-material` get replaced by `team-materials` when the relevant teams capture the point. The teams `id` fields here must match the team `id` field in the `Teams` module.

## Capture Time Variability
The capture time can be varied based on the number of players. The `time-modifier-per-player` parameter should be a relative operator that is applied recursively for each extra player on a control point (ignoring the initial player). If the number is additive then it should be specified in milliseconds. The modifier is for the total capture time and scales pro rata for ongoing captures. The minimum time can be set using the `min-capture-time` parameter.

Note: `~` denotes relative. Due to oddities in the order of operations, only multiplication (`*`) and addition (`+`) should be used. However, division can be used by multiplying by the reciprocal, and subtraction can be used by adding a negative number. In both cases, the operator must still be specified (see the example below).

## Example Configuration
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
    time-modifier-per-player: ~+-500
    min-capture-time: 2s
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
