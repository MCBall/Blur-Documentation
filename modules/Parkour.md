# `Parkour` module

The Parkour module manages a parkour or jumping puzzle area. This module allows multiple courses, defined as a list in `courses`. For each course, when a player leaves the extent `area` they are teleported back to their previous checkpoint from the list of `checkpoints`.

Example `Parkour` configuration:

```
  - id: parkour1-bounds
    cuboid: {min: '-9.0, 42.0, -152.0', max: '-139.0, 153.0, -68.0'}
  - id: parkour1-check-0
    cuboid: {min: '-94.0, 77.0, -109.0', max: '-99.0, 81.0, -99.0'}
  - id: parkour1-check-1
    cuboid: {min: '-67.0, 65.0, -114.0', max: '-69.0, 69.0, -109.0'}
  - id: parkour1-check-2
    cuboid: {min: '-53.0, 65.0, -98.0', max: '-59.0, 68.0, -94.0'}
  - id: parkour2-bounds
    cuboid: { min: '71.5, 69.9, 71.5', max: '173.5, 104, 173.5' }
  - id: parkour2-check-0
    cuboid: { min: '96, 72, 83', max: '100, 76, 87' }
  - id: parkour2-check-1
    cuboid: { min: '150, 72, 91', max: '154, 76, 95' }
  - id: parkour2-check-2
    cuboid: { min: '145, 79, 126', max: '149, 83, 130' }
- Parkour:
    courses:
    - area: parkour1-bounds
      checkpoints:
      - parkour1-check-0
      - parkour1-check-1
      - parkour1-check-2
    - area: parkour2-bounds
      checkpoints:
      - parkour2-check-0
      - parkour2-check-1
      - parkour2-check-2
```
