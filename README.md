# Homeassistant and Contactless Water Level Sensor.

Homeassistant and Contactless Water Level Sensor.  Esphome  + Esp8266 Wemos d1 mini

# Component
1. Esp8266 Wemos d1 mini
2. Non-Contact Liquid sensor ...
   
Just found this amazing item on AliExpress. Check it out! MYR13.69  14%OFF | XKC-Y25 Non-Contact Liquid Level Sensor Tank Water Level Sensor Water Level Sensor Liquid Induction Switch
https://a.aliexpress.com/_okMJRIk
   
# Setup
# 1. EspHome
    Refer to file: contactlesswaterlevel.yaml

# 2. Home assistant lovelace
     a. Gauge Card Configuration
        type: gauge
        entity: sensor.watertank_nodemcu
        min: 0
        max: 100
        needle: true
        severity:
          green: 45
          yellow: 20
          red: 0
          blue: 1
     b. Entities Card Configuration
        type: entities
        entities:
          - entity: sensor.tank_level
          - entity: binary_sensor.water_100
          - entity: binary_sensor.water_75
          - entity: binary_sensor.water_50
          - entity: binary_sensor.water_25
        title: Contactless water level
