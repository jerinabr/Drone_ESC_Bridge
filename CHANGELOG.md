# Changelog
This is the revision history for the drone ESC bridge
## v1.1
### Schematic
- Changed the `ESC Telemetry` pin function to `Battery Voltage` because this board won't handle DShot telemetry requests
  - Change affected ESC_Debug header as well
- Added voltage divider circuitry to scale the 4S LiPo voltage (max 16.4V) to max 3.3V
- Remapped the XIAO connector pins because I didn't bother checking to see if the XIAO pins could support the function I assigned them to
  | Pin Function                | Previous Pin  | New Pin   |
  | --------------------------- | ------------- | --------- |
  | `Motor 1`                   | D3            | D4        |
  | `Motor 2`                   | D2            | D3        |
  | `Motor 3`                   | D1            | D2        |
  | `Motor 4`                   | D0            | Unchanged |
  | `ESC Current Sense`         | D4            | D5        |
  | `Peripheral Current Sense`  | D5            | D6        |
  | `Battery Voltage`           | D7            | Unchanged |
  | `SPI MOSI`                  | D10           | D8        |
  | `SPI MISO`                  | D9            | D1        |
  | `SPI SCK`                   | D8            | D9        |
  | `SPI CS`                    | D6            | D10       |
- Reordered the SPI connector pin functions to make the board routing a little easier
### Board
- Moved SPI connector closer to Jetson power connector
- Updated SPI connector silkscreen labels to reflect pin reordering
- Removed ground pour on top layer
  - Used polygon pours with stitching vias on ground pads instead
- Updated silkscreen pin info table for ESC_Debug to replace `TLM` with `VBAT`
### Misc
- Added this changelog file
- Added image of MCU connection diagram to the folder
## v1.0
Initial release
