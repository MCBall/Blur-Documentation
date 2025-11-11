# `TelePortals` module

The TelePortals module allows portals to be defined that will teleport entities between portals. This requires an extent to be defined for each portal. It's worth noting that the term "portal" here is just semantic, the logic is solely based on the extent which can physically contain anything (or nothing).

The fundamental structure of the module is groups of portals. Each group can have as many portals as desired. When an entity enters a portal, a random portal is selected from the group (of the allowed exit portals), and the entity is teleported to it.

Each portal has the following configuration options:
- `extent` - A `cuboid` extent covering the portal area.
- `direction` - The axis-aligned vector defining the active direction of the portal (length 1).
- `up` - The axis-aligned vector defining the 'up' direction of the portal (length 1, orthogonal to `direction`). - Default: `'0, 1, 0'`
- `is-entry` - Boolean, whether the portal can be used as an entry. - Default: `true`
- `is-exit` - Boolean, whether the portal can be used as an exit. - Default: `true`

Each group has the following configuration options:
- `invert` - Whether the entity direction is inverted relative to the portal direction when teleported. - Default: `true`
- `momentum` - Whether the entity retains its momentum when teleported. - Default: `true`
- `transform-direction` - Whether the entity direction is transformed when teleported. - Default: `true`
- `portals` - The array of portals.
- `players-only` - Whether a portal is restricted to only teleport players. - Default: `false`

The root of the configuration is simply `groups` which is a list of portal groups.

This diagram shows the physical layout of portals and how `invert` affects the direction that an entity exits a portal. This defines which side of the portal the entity is placed after teleportation.

![TelePortals Diagram](../images/teleportals-diagram.svg)

Combinations of `is-entry` and `is-exit` portals can be easily used to create many-to-many portal groups, one-to-many portal groups, and many-to-one portal groups.

Portals are visibly indicated by `enchant` particles. If further visual indication is desired, it is recommended to use [Block Display](https://minecraft.wiki/w/Display#Block_Displays) entities. These could even be used to create fake walls or similar constructions.

Example `TelePortals` configuration (from the Hub map):

```
- Extents:
  - id: portal-house-0
    cuboid: { min: '-87, 76, 105', max: '-86, 79, 106' }
  - id: portal-house-1
    cuboid: { min: '-88, 76, 113', max: '-87, 79, 114' }
  - id: portal-barrys-bank
    cuboid: { min: '-90, 76, 127', max: '-89, 78, 131' }
  - id: portal-als-naming
    cuboid: { min: '-92, 76, 142', max: '-91, 78, 146' }
  - id: portal-mikes-maps
    cuboid: { min: '-96, 76.5, 150', max: '-95, 79, 152' }
  - id: portal-tids-tavern
    cuboid: { min: '-107, 82.5, 171', max: '-105, 87, 172' }
  - id: portal-end-of-pier
    cuboid: { min: '-178, 64, 166', max: '-175, 65, 169' }
  - id: portal-water-hole
    cuboid: { min: '-161, 64, 162', max: '-158, 65, 165' }
  - id: portal-garfields-guns
    cuboid: { min: '-100, 80, 158.7', max: '-99, 82, 160.3' }
  - id: portal-house-2
    cuboid: { min: '-146, 75.5, 190', max: '-145, 78, 191' }
  - id: portal-house-3
    cuboid: { min: '-169, 66, 187', max: '-165, 69, 188' }
  - id: portal-freddys-fireworks
    cuboid: { min: '-136, 66, 176', max: '-133, 69, 177' }
  - id: portal-grunts-gubbins
    cuboid: { min: '-100, 69, 153', max: '-99, 71, 154.3' }
  - id: portal-fitches-fish
    cuboid: { min: '-94, 66, 127', max: '-93, 68, 132' }
  - id: portal-freds-fishy-food
    cuboid: { min: '-93, 66, 112', max: '-92, 68, 116' }
  - id: portal-billys-bakery
    cuboid: { min: '-93, 66, 102', max: '-92, 68, 107' }
- TelePortals:
    groups:
    - invert: false
      momentum: true
      portals:
      - extent: portal-house-0
        direction: '1, 0, 0'
      - extent: portal-house-1
        direction: '1, 0, 0'
      - extent: portal-barrys-bank
        direction: '1, 0, 0'
      - extent: portal-als-naming
        direction: '1, 0, 0'
      - extent: portal-mikes-maps
        direction: '1, 0, 0'
      - extent: portal-garfields-guns
        direction: '1, 0, 0'
      - extent: portal-tids-tavern
        direction: '0, 0, 1'
      - extent: portal-house-2
        direction: '0, 0, 1'
      - extent: portal-house-3
        direction: '0, 0, 1'
      - extent: portal-freddys-fireworks
        direction: '0, 0, 1'
      - extent: portal-grunts-gubbins
        direction: '1, 0, 0'
      - extent: portal-fitches-fish
        direction: '1, 0, 0'
      - extent: portal-freds-fishy-food
        direction: '1, 0, 0'
      - extent: portal-billys-bakery
        direction: '1, 0, 0'
    - invert: true
      momentum: true
      transform-direction: false
      portals:
      - extent: portal-end-of-pier
        is-entry: false
        is-exit: true
        direction: '0, 1, 0'
        up: '1, 0, 0'
      - extent: portal-water-hole
        is-entry: true
        is-exit: false
        direction: '0, 1, 0'
        up: '0, 0, 1'
```
