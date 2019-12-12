## Usage:
```yaml
resources:
  url: /community_plugin/button-toolbar/button-toolbar.js
  type: module
```

## Images:
Left button toolbar with services call, right one with service call and state of the sensor!

<img src="images/1.png" alt="1" width="200"/> <img src="images/2.png" alt="1" width="200"/>

## Lovelace:
```yaml
- type: custom:button-toolbar
  aspect_ratio: 1/2 # Optional, Default: 1/1
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
      entity: sensor.bedroom_humidity
      unit: % # Optional, Default: entity unit_of_measurement
```
