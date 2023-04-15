# `CommandPortals` module

The CommandPortals module allows portals to be defined that will run a command when a player enters the portal extent. This requires an extent to be defined for each portal. However, if a portal needs to run multiple commands, multiple portals could use the same extent.

Example `CommandPortals` configuration:

```
- Extents:
  - id: vote-1
    cuboid: { min: '2, 106, -20', max: '6, 109, -17' }
  - id: vote-2
    cuboid: { min: '-10, 106, -20', max: '-5, 109, -14' }
- CommandPortals:
    portals:
    - extent: vote-1
      command: 'vote 1'
    - extent: vote-2
      command: 'vote 2'
```
_**Note**: the commands do not include the leading `/`._
