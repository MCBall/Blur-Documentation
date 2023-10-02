FixedJumpPads is a module for creating jump pads with a fixed direction and power. They must use a polished blackstone pressure plate as the triggering block.

The configuration for FixedJumpPads should be a list of jump pads (`pads`), with configuration as follows. `loc` is the position of the jump pad. `power` is the speed at which the jump pad launches a player. `pitch` and `yaw` are the pitch and yaw angles of the direction in which the player will be launched.

Example `FixedJumpPads` configuration:

```
- FixedJumpPads:
    pads:
    - { loc: '53.5, 65, -17.5', power: 3, pitch: -50, yaw: 90 }
    - { loc: '-53, 65, 18', power: 5, pitch: -14.2, yaw: -146.7 }
```
