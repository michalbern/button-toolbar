## Usage:
```yaml
resources:
  url: /community_plugin/button-toolbar/button-toolbar.js
  type: module
```

## Example:
```yaml
- type: custom:button-toolbar
  content:
    entity: light.bedroom
    image: /local/bedroom_light.png
    height: 60%
  toolbar:
    - type: service # This is toolbar item type
      name: Toggle
      icon: mdi:lamp
      service:
        name: light.toggle
        entity: light.bedroom
    - type: state
      state:
        entity: sensor.bedroom_humidity
        unit: % # Optional (If not specified, returns default entity unit)
```
