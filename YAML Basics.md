YAML is a configuration file format commonly used in Minecraft. Below are some examples of YAML formatting. Attention to indentation is important as it defines the levels of subsections.

``` YAML
section:
  subsection:
    property: "value"
    other-property: 42.0
  collapsed-section: {property: "value", other-property: 42.0}
  list-header:
  - list-item-1: "value"
  - list-item-2: "value2"
```

Note that the following formats are equivalent. In particular, the way the list `flags` is broken up into items.

``` YAML
- CaptureTheFlag:
    flags:
    - home: 8.5, 18.0, -72.5
      team: red
    - home: 8.6, 18.0, 73.5
      team: blue
    max-captures: 3
```
``` YAML
- CaptureTheFlag:
    flags:
    - {home: '8.5, 18.0, -72.5', team: red}
    - {home: '8.6, 18.0, 73.5', team: blue}
    max-captures: 3
```
