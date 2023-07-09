The Conquest module handles the game logic for the Conquest gamemode. It depends on the [`BControlPoints`](BControlPoints.md) module which handles all of the individual capture point logic. The `Conquest` module handles scoring and user interface.

There are two configuration options. `max-score` sets the score that a team must achieve to win. `alert-at` sets the score at which the server sends an alert to all players. An additional alert is also sent at the halfway point.

Example `Conquest` configuration:

```
- Conquest:
    max-score: 1200
    alert-at: 100
```
