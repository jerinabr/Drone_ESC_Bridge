# Changelog

This is the revision history for the drone ESC bridge

## v1.1

### Schematic

- Remapped the XIAO connector pins because I didn't bother checking to see if the XIAO pins could support the function I assigned them to.
  
  - **Motor 1:** D3 -> D4
  - **Motor 2:** D2 -> D3
  - **Motor 3:** D1 -> D2
  - **Motor 4:** Unchanged  (D0)
  - **ESC Current Sense:** D4 -> D5
  - **Peripheral Current Sense:** D5 -> D6
  - **ESC Telemetry:** Unchanged (D7)
  - **SPI MOSI:** D10 -> D8
  - **SPI MISO:** D9 -> D1
  - **SPI SCK:** D8 -> D9
  - **SPI CS:** D6 -> D10
    
- Reordered the SPI connector pin functions to make the board routing a little easier

### Board

- Move SPI connector closer to Jetson power connector
- Update SPI connector silkscreen labels to reflect pin reordering

## v1.0

Initial release
