# Commande Index

| Action            | Gcode               |
| ------------------|:-------------------:|
| Save Settings     | ```M500```          |
| Applied Settings  | ```M501```          |
| Set Z Offset      | ```M851 Z X.XX```   |
| Unlock Axis Limit | ```M211 S0```       |
| Set Home          | ```G28```           |
| Bed Leveling      | ```G29```           |
| Use saved Bed Leveling|  ```M420 S1```       |
| More logs|  ```M111 S247```       |

### Nozzle offset

To configure the nozzle-probe offset here is the protocol:

- `G28` Home the Z axis
- `M280` P0 S10 Raise Z and deploy the probe.
- `M211 S0` unlock z
- Move Z down slowly until the probe triggers.
- Take the current Z=16.9
- Move Z with a paper under the nozzle until it touches slightly
- take current Z value Z=13.3 
- your offset is the difference between the two: 3.6
- Set with `M851 Z-3.6` and #define Z_PROBE_OFFSET_FROM_EXTRUDER -3.5 in marlin code

### Bed leveling

To do the bed leveling once

- set the bed temperature and wait for the bed to warm up
- `G29` do the autmatic bed leveling
- `M500` save it
- `M501` check the eeprom values

### Use bed leveling

In cura settings for the printer, after G28, add:

```
M501
M420 S1
```


## Our cura settings



## install octoprint

https://octoprint.org/download/

install firware updater plugin
ssh to octopi.local and `apt-get install avrdude``
thenyou can configure the firmware updater with avrdude and arduino atmega 2560
