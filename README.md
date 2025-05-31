# Drone_ESC_Bridge
## Description
This board is intended to act as a bridge between the Nvidia Jetson and the 4-in-1 ESC on the ADP drone[^1]

It recieves motor speeds and other commands from the Jetson over the SPI interface and outputs motor speeds to the ESC over PWM

It also monitors the LiPo voltage and can report it back to the Jetson over the SPI interface

The board receives 5V power from an off-board buck converter which is used to power both the microcontroller (Seeed XIAO SAMD21) and the Jetson

[^1]: Firmware for the Jetson and Seeed XIAO can be found [here](https://github.com/LarsGart/Autonomous-Drone-Platform)

## BOM
| Reference         | Value                 | Footprint                                                    | Qty | DigiKey Part Number      |
| ----------------- | --------------------- | ------------------------------------------------------------ | --- | ------------------------ |
| C1,C2,C4,C6,C7,C8 | 0.1u                  | Capacitor_SMD:C_0603_1608Metric_Pad1.08x0.95mm_HandSolder    | 6   | 311-1088-1-ND            |
| C3                | 1u                    | Capacitor_SMD:C_0603_1608Metric_Pad1.08x0.95mm_HandSolder    | 1   | 311-1446-1-ND            |
| C5                | 22u                   | Capacitor_SMD:CP_Elec_6.3x5.8                                | 1   | PCE3811CT-ND             |
| ESC1              | Conn_01x08            | Connector_JST:JST_SH_BM08B-SRSS-TB_1x08-1MP_P1.00mm_Vertical | 1   | 455-BM08B-SRSS-TBCT-ND   |
| ESC_DEBUG1        | Conn_01x06            | Connector_PinHeader_2.54mm:PinHeader_2x03_P2.54mm_Vertical   | 1   | 2057-PH2-06-UA-ND        |
| JETSON_PWR1       | Conn_02x02_Top_Bottom | Connector_PinHeader_2.54mm:PinHeader_2x02_P2.54mm_Vertical   | 1   | 2057-PH2-04-UA-ND        |
| Q1                | Si2318CDS             | Package_TO_SOT_SMD:SOT-23-3                                  | 1   | SI2318CDS-T1-GE3CT-ND    |
| R1                | 10m                   | Resistor_SMD:R_2010_5025Metric_Pad1.40x2.65mm_HandSolder     | 1   | 13-PE2010FKE070R01LCT-ND |
| R2                | 100                   | Resistor_SMD:R_0603_1608Metric_Pad0.98x0.95mm_HandSolder     | 1   | 311-100HRCT-ND           |
| R3                | 33k                   | Resistor_SMD:R_0603_1608Metric_Pad0.98x0.95mm_HandSolder     | 1   | 311-33.0KHRTR-ND         |
| R4                | 8.2k                  | Resistor_SMD:R_0603_1608Metric_Pad0.98x0.95mm_HandSolder     | 1   | 311-8.2KGRTR-ND          |
| SPI1,VBUCK1       | Conn_01x04            | Connector_PinHeader_2.54mm:PinHeader_2x02_P2.54mm_Vertical   | 2   | 2057-PH2-04-UA-ND        |
| U1                | LMP8640               | Package_TO_SOT_SMD:SOT-23-6                                  | 1   | 296-48927-1-ND           |
| U2                | LM5050-1              | Package_TO_SOT_SMD:TSOT-23-6                                 | 1   | 296-46427-1-ND           |
| XIAO_L1,XIAO_R1   | Conn_01x07            | Connector_PinSocket_2.54mm:PinSocket_1x07_P2.54mm_Vertical   | 2   | S7040-ND                 |

> [!NOTE]
> `JETSON_PWR1` has the same part number has `SPI1` and `VBUCK1`\
> They're separate entries because the connector footprint used in the schematic was different

## Images
### Schematic
![Schematic Diagram](Images/Schematic.png)
### Top Layer
![PCB top layer with silkscreen](Images/PCB_Top.png)
### Bottom Layer
![PCB bottom layer with silkscreen](Images/PCB_Bottom.png)
### 3D Top View
![3D view of the top of the board with components](Images/3D_View.png)
