The below configs are standard templates for various gamemodes and are a good starting point for map configuration.

### This will be updated with more helpful details in the future. 

# CTF

``` YAML
map:
  name: Koder CTF
  description: Watch your step, it's a long drop!
  version: 2.0
  min-players: 6
  max-players: 32
  authors:
  - {role: Map Builder, uuid: 97eefba2-4910-4166-81ac-fee71cb1e004}
modules:
- Extents:
  - id: deathbox
    protect: true
    cuboid:
      max: 89.0, 18.0, 9.0
      min: 71.0, 2.0, -8.0
  - id: deathbox-spawns
    cuboid:
      max: 74.0, 9.0, -5.0
      min: 84.0, 9.0, 5.0
  - id: red-spawns
    union:
    - block: -27.5, 8.0, -63.5, 0.0, 0.0
    - block: -27.5, 8.0, -59.5, -32.7, 0.0
    - block: -23.5, 8.0, -59.5, 41.4, 0.0
    - block: -23.5, 8.0, -63.5, 0.0, 0.0
    - block: -22.5, 12.0, -75.5, 0.0, 0.0
    - block: -31.5, 12.0, -74.5, 0.0, 0.0
    - block: -25.5, 12.0, -76.5, 0.0, 0.0
    - block: -26.5, 11.0, -46.5, 56.1, 0.0
    - block: -21.5, 10.0, -51.5, 54.7, 0.0
    - block: 37.5, 15.0, -73.5, 51.3, 0.0
    - block: 42.5, 13.0, -72.5, 22.6, 0.0
    - block: 40.5, 10.0, -47.5, 21.1, 0.0
    - block: 48.5, 10.0, -47.5, 37.5, -15.6
  - id: red-flag-block
    block: 8.5, 18.0, -72.5
  - id: blue-spawns
    union:
    - block: -27.5, 8.0, 64.5, 180.0, 0.0
    - block: -27.5, 8.0, 60.5, 147.3, 0.0
    - block: -23.5, 8.0, 60.5, 138.6, 0.0
    - block: -23.5, 8.0, 64.5, 180.0, 0.0
    - block: -22.5, 12.0, 76.5, 180.0, 0.0
    - block: -31.5, 12.0, 75.5, 180.0, 0.0
    - block: -25.5, 12.0, 77.5, 180.0, 0.0
    - block: -26.5, 11.0, 47.5, 123.9, 0.0
    - block: -21.5, 10.0, 52.5, 125.3, 0.0
    - block: 37.5, 15.0, 74.5, 128.7, 0.0
    - block: 42.5, 13.0, 73.5, 157.4, 0.0
    - block: 40.5, 10.0, 48.5, 158.9, 0.0
    - block: 48.5, 10.0, 48.5, 142.5, -15.6
  - id: blue-flag-block
    block: 8.6, 18.0, 73.5
  - id: bounds
    cuboid:
      max: 100.0, 62.0, 100.0
      min: -70.0, -8.0, -93.0
- Teams:
    teams:
    - id: red
      name: RED
      max: 25
      chat-prefix: <span style="c"></span>
      color: Red
      nametag-visibility: ALLIES
      chat-color: red
    - id: blue
      name: BLUE
      max: 25
      chat-prefix: <span style="3"></span>
      color: Blue
      nametag-visibility: ALLIES
      chat-color: dark_aqua
- Spawns:
    spawns:
    - red-spawns:
        filter: team-red
        point-to: ~, ~, ~
    - blue-spawns:
        filter: team-blue
        point-to: ~, ~, ~
- StaggeredGroupRespawns:
    max-timer: 15s
    min-players: 3
    min-timer: 5s
    teleport-to: deathbox-spawns
    deathbox: deathbox
- Goal:
    time-limit: 30m
- Paintball: {}
- CaptureTheFlag:
    flags:
    - home: 8.5, 18.0, -72.5
      team: red
    - home: 8.6, 18.0, 73.5
      team: blue
    max-captures: 3
- WorldProtect:
    player-damage-entity: false
- FixedHunger
- MultiKill
- OutOfBounds:
    extent: bounds
- Suffocation
- CTFStats
- Intro
- EndGameStats
```

# Elimination
``` YAML
map:
  name: Farm ELIM
  description: MCBall Simulator 2013
  version: 1.0
  min-players: 2
  max-players: 18
modules:
- Extents:
  - id: red-soulwell
    cuboid:
      max: 0.0, 36.0, -6.0
      min: -3.0, 33, -9.0
  - id: deathbox
    protect: true
    cuboid:
      max: 7, 85.0, 1
      min: -10, 78.0, -16
  - id: deathbox-spawns
    cuboid:
      max: 1.5, 80.5, -3.5
      min: -4.5, 80.5, -11.5
  - id: red-spawns
    union:
    - block: 54.5, 38.0, -19.5, 20.6, 5.7
    - block: 70.5, 31.0, -32.5, 134.7, -2.5
    - block: 74.5, 31.0, 15.5, 94.2, -3.7
    - block: 54.5, 31.0, 10.5, 103.1, -3.9
    - block: 41.5, 31.0, -39.5, 46.5, -6.1
    - block: 81.5, 31.0, -22.5, 102.8, -2.0
  - id: red-flag-block
    block: 63.5, 32.0, -15.5
  - id: blue-spawns
    union:
    - block: -48.5, 31.5, -8.5, -90.0, 0
    - block: -44.5, 31.5, -28.5, -89.0, 0
    - block: -61.5, 31.5, -4.5, -90.0, 0
    - block: -67.5, 31.5, 6.5, -91.0, 0
    - block: -32.5, 31.5, 16.5, -91.0, 0
    - block: -30.5, 31.5, 6.5, -90.0, 0  
  - id: blue-flag-block
    block: -42.5, 31.0, 5.5
  - id: bounds
    cuboid:
      max: 89.5, 101.0, 41.5
      min: -78.5, 12.0, -55.0
- Teams:
    teams:
    - id: red
      name: RED
      max: 25
      chat-prefix: <span style="c"></span>
      color: Red
      nametag-visibility: ALLIES
      chat-color: red
    - id: blue
      name: BLUE
      max: 25
      chat-prefix: <span style="3"></span>
      color: Blue
      nametag-visibility: ALLIES
      chat-color: dark_aqua
- Spawns:
    spawns:
    - red-spawns:
        filter: team-red
        point-to: ~, ~, ~
    - blue-spawns:
        filter: team-blue
        point-to: ~, ~, ~
- Goal:
    time-limit: 10m
- Paintball: {}
- Elimination:
    deathbox: deathbox-spawns
    soul-wells:
    - team: red
      extent: red-soulwell
    - team: blue
      extent: red-soulwell
- WorldProtect:
    player-damage-entity: false
- FixedHunger
- MultiKill
- OutOfBounds:
    extent: bounds
- Suffocation
- CTFStats:
    record-stats: false
- Intro
- EndGameStats
```

# RTF
``` YAML
map:
  name: Coast RTF
  description: Just a relaxing day in the sun.
  version: 1.0
  min-players: 4
  max-players: 24
modules:
- Extents:
  - id: red-rtf
    cuboid:
      max: 1.5, 69, 72.5
      min: -0.5, 71, 74.5
  - id: blue-rtf
    cuboid:
      max: -0.5, 69, -71.5
      min: 1.5, 71, -73.5
  - id: deathbox
    protect: true
    cuboid:
      max: -8, 107, 8
      min: 8, 100, -8
  - id: deathbox-spawns
    cuboid:
      max: -1.5, 103, -1.5
      min: 2.5, 103, 2.5
  - id: red-spawns
    union:
    - block: -20.5, 69.1, 64.5, 0, 0
    - block: 13.5, 69.1, 73.5, 0, 0
    - block: 37.5, 69.1, 59.5, 0, 0
    - block: 2.5, 69, 95.5, -90, 0
    - block: 0.5, 69, 85.5, 135, 0
    - block: -18.5, 69, 87.5, -180, 0
  - id: red-flag-block
    block: 0, 69, 73
  - id: blue-spawns
    union:
    - block: 21.5, 71.1, -63.5, -180, 0
    - block: -36.5, 71.1, -58.5, -180, 0
    - block: -12.5, 71.1, -72.5, -180, 0
    - block: -1.5, 69, -64.5, 90, 0
    - block: 0.5, 69, -84.5, -45, 0
    - block: 19.5, 69, -86.5, 0, 0
  - id: blue-flag-block
    block: 0, 69, -73
  - id: bounds
    cuboid:
      max: -65, 109, 107
      min: 63, 61, -107
- Teams:
    teams:
    - id: red
      name: RED
      max: 25
      chat-prefix: <span style="c"></span>
      color: Red
      nametag-visibility: ALLIES
      chat-color: red
    - id: blue
      name: BLUE
      max: 25
      chat-prefix: <span style="3"></span>
      color: Blue
      nametag-visibility: ALLIES
      chat-color: dark_aqua
- Spawns:
    spawns:
    - red-spawns:
        filter: team-red
        point-to: ~, ~, ~
    - blue-spawns:
        filter: team-blue
        point-to: ~, ~, ~
- StaggeredGroupRespawns:
    max-timer: 15s
    min-players: 3
    min-timer: 5s
    teleport-to: deathbox-spawns
    deathbox: deathbox
- Goal:
    time-limit: 20m
- Paintball: {}
- RushTheFlag:
    flag-location: 0, 73, 0
    bases:
    - { extent: red-rtf, team: red }
    - { extent: blue-rtf, team: blue }
    max-captures: 3
- WorldProtect:
    player-damage-entity: false
- FixedHunger
- MultiKill
- OutOfBounds:
    extent: bounds
- Suffocation
- CTFStats
- EndGameStats
- Intro
```

# TDM
``` YAML
map:
  name: Shyre TDM
  description: We seem to be a bit short of hobbitses.
  version: 2.0
  min-players: 2
  max-players: 10
  authors:
  - {role: Map Builder, uuid: 8693ae19-ecfc-4d57-8695-451697ec0bec}
  - {role: Map Builder, uuid: 97eefba2-4910-4166-81ac-fee71cb1e004}
  - {role: Map Builder, uuid: a00e63f2-e6eb-4362-b10b-53d32f18cd22}
  - {role: Map Builder, uuid: f4a2979c-b9af-4908-a88e-51313fcc47a3}
modules:
- Extents:
  - id: deathbox
    protect: true
    cuboid:
      max: 7.0, 60.0, 3.0
      min: -6.0, 56.0, -3.0
  - id: deathbox-spawns
    cuboid:
      max: 4.5, 57.5, 1.5
      min: 03.5, 57.5, -0.5
  - id: red-spawns
    union:
    - block: 59.5, 66.5, 29.5, 90.0, 0.0
    - block: 59.5, 66.5, 33.5, 90.0, 0.0
    - block: 54.5, 66.5, 38.5, 180.0, 0.0
    - block: 50.5, 66.5, 38.5, 180.0, 0.0
    - block: 48.5, 65.5, 10.5, 0.0, 0.0
    - block: 55.0, 65.5, 9.0, 180.0, 0.0
    - block: 35.5, 65.5, 16.5, 0.0, 0.0
    - block: 31.5, 65.5, 26.5, 90.0, 0.0
    - block: 35.5, 65.5, 25.5, -180.0, 0.0
    - block: 53.5, 65.5, -17.5, 90.0, 0.0
    - block: 54.5, 65.5, -11.5, 90.0, 0.0
  - id: blue-spawns
    union:
    - block: -58.5, 66.5, -28.5, -90.0, 0.0
    - block: -58.5, 66.5, -32.5, -90.0, 0.0
    - block: -53.5, 66.5, -37.5, 0.0, 0.0
    - block: -49.5, 66.5, -37.5, 0.0, 0.0
    - block: -47.5, 65.5, -9.5, 180.0, 0.0
    - block: -54.0, 65.5, -8.0, 0.0, 0.0
    - block: -34.5, 65.5, -15.5, 180.0, 0.0
    - block: -30.5, 65.5, -25.5, -90.0, 0.0
    - block: -34.5, 65.5, -24.5, 0.0, 0.0
    - block: -52.5, 65.5, 18.5, -90.0, 0.0
    - block: -53.5, 65.5, 12.5, -90.0, 0.0
  - id: bounds
    cuboid:
      max: 80.0, 134.0, 65.0
      min: -73.0, 53.0, -56.0
- Teams:
    teams:
    - id: red
      name: RED
      max: 25
      chat-prefix: <span style="c"></span>
      color: Red
      nametag-visibility: ALLIES
      chat-color: red
    - id: blue
      name: BLUE
      max: 25
      chat-prefix: <span style="3"></span>
      color: Blue
      nametag-visibility: ALLIES
      chat-color: dark_aqua
- Spawns:
    spawns:
    - red-spawns:
        filter: team-red
        point-to: ~, ~, ~
    - blue-spawns:
        filter: team-blue
        point-to: ~, ~, ~
- StaggeredGroupRespawns:
    max-timer: 15s
    min-players: 3
    min-timer: 5s
    teleport-to: deathbox-spawns
    deathbox: deathbox
- TeamDeathmatch:
    max-score: 50
- Goal:
    time-limit: 15m
- Paintball:
    allow-doors: false
    allow-trapdoors: false
    allow-buttons: false
- WorldProtect:
    player-damage-entity: false
- FixedHunger
- MultiKill
- OutOfBounds:
    extent: bounds
- Suffocation
- CTFStats:
    record-stats: false
- Intro
- EndGameStats
```
