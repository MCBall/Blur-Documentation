# `FreeKits` module

The FreeKits module can be applied to override the permissions requirements of a kit for all players. Typically, this would be applied to the lobby config so that all games started from that lobby have the free kits applied.

Example `FreeKits` configuration:

```
- FreeKits:
  - sniper
  - ninja
  - ricochet
```
_**Note**: leaving the list of kits empty will make all kits free._
