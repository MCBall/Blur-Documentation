This site contains documentation for Blur modules used on the [MCBall](https://mcball.net) server. Contained herein are pages with descriptions, examples, and recommendations for usage of Blur modules.

Some documentation is for the open source modules available from the [Blur project](https://github.com/BlurEngine/Blur). The remainder is from the closed source CodeRack project used within MCBall. Pages for modules are listed accordingly.

All configuration uses YAML. Examples of YAML formatting can be found [here](YAML-Basics.md).

Templates for each game mode can be found [here](default-config.md).

Many configuration options use common serializers (how data is formatted). Details of many of these can be found [here](Common-Serializers.md).

## Module List
### Blur
- Root `map` section
- [`Extents`](modules/Extents.md)
- `Teams`
- `Spawns`
- `Goal`
- `WorldProtect`
- `FixedHunger`
- [`BControlPoints`](modules/BControlPoints.md)

### CodeRack
- `StaggeredGroupRespawns`
- [`Paintball`](modules/Paintball.md)
- [`PaintballPractice`](modules/PaintballPractice.md)
- `CaptureTheFlag`
- `MultiKill`
- `OutOfBounds`
- `Suffocation`
- `CTFStats`
- `Intro`
- `EndGameStats`
- [`CommandPortals`](modules/CommandPortals.md)
- [`Conquest`](modules/Conquest.md)
- [`SimpleJumpPads`](modules/SimpleJumpPads.md)
- [`FixedJumpPads`](modules/FixedJumpPads.md)
- [`FreeKits`](modules/FreeKits.md)
- [`Parkour`](modules/Parkour.md)
