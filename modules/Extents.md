# `Extents` module

Example `Extents` section:

```
- Extents:
  - id: deathbox
    protect: true
    cuboid:
      max: 6.0, 108.0, -87.0
      min: -9.0, 93.0, -104.0
  - id: deathbox-spawns
    cuboid:
      max: 4.0, 100.5, -89.0
      min: -7.0, 100.5, -100.0
  - id: red-spawns
    union:
    - block: 31.5, 80.5, 36.5, 66.0, -20.0
    - block: 34.5, 80.5, 36.5, 70.0, -15.0
    - block: 72.5, 85.5, -10.5, 100.0, 0.0
```
