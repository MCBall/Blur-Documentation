# Ricochet kit
Paintballs infused with bouncy ricochet properties.

3 - Paintballs ricochet 2 times. \
5 - Bounce speed increases. \
7 - Paintballs ricochet 3 times.

### Configuration options
General options:
- `base-bounces` - Base number of bounces per paintball.
- `base-elasticity-min` - Base minimum bounce elasticity.
- `base-elasticity-max` - Base maximum bounce elasticity.

Killstreak options:
- `ks-3-bounces` - Number of bounces per paintball after a 3 killstreak.
- `ks-5-elasticity-min` - Minimum bounce elasticity after a 5 killstreak.
- `ks-5-elasticity-max` - Maximum bounce elasticity after a 5 killstreak.
- `ks-7-bounces` - Number of bounces per paintball after a 7 killstreak.
- `ks-100-bounces` - Number of bounces per paintball after a 100 killstreak.


### Example/default configuration
```
- Paintball:
  kit-configs:
  - ricochet:
      base-bounces: 1
      base-elasticity-min: 0.4
      base-elasticity-max: 0.8
      ks-3-bounces: 2
      ks-5-elasticity-min: 0.6
      ks-5-elasticity-max: 1.0
      ks-7-bounces: 3
      ks-100-bounces: 100
```
