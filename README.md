# LoRa GPS Tracker

A custom PCB GPS tracker using LoRa wireless communication for long-range, low-power asset tracking. Designed in KiCad 8, combining a GPS module and LoRa transceiver for remote location reporting.

---

## Features
- LoRa long-range wireless (up to 10km line-of-sight)
- GPS module integration (NEO-6M or compatible)
- Ultra-low power design for battery operation
- SMA or u.FL antenna connector
- Compatible with LoRaWAN / peer-to-peer

## Specifications

| Parameter | Value |
|-----------|-------|
| LoRa Module | Ra-02 / RFM95W (SX1278) |
| GPS Module | NEO-6M / NEO-8M |
| Frequency | 433MHz / 868MHz / 915MHz |
| Range | Up to 10km (line of sight) |
| Supply Voltage | 3.3V |
| Interface | SPI (LoRa), UART (GPS) |
| PCB Layers | 2 |
| Designed With | KiCad 8 |

## Project Structure

```
├── Schematic/       # KiCad schematic (.kicad_sch, PDF)
├── PCB/             # PCB layout (.kicad_pcb, .kicad_pro)
├── Gerbers/         # Fabrication files
├── BOM/             # Bill of materials (CSV)
├── 3D/              # 3D model (.step)
└── Images/          # PCB renders and schematic screenshots
```

## How It Works

The GPS module sends NMEA sentences via UART to the MCU. The MCU parses the latitude/longitude and transmits it as a LoRa packet. A receiver node (another LoRa module or a LoRaWAN gateway) picks up the packet and logs or displays the location.

## Bill of Materials (Summary)

| Component | Value | Qty |
|-----------|-------|-----|
| LoRa Module | Ra-02 / RFM95W | 1 |
| GPS Module | NEO-6M | 1 |
| MCU | ATmega328p / STM32 | 1 |
| Voltage Regulator | AMS1117-3.3V | 1 |
| Antenna Connector | SMA / u.FL | 1 |

## Fabrication

Gerber files are in `/Gerbers`, ready for JLCPCB, PCBWay, or similar.

## License

This project is licensed under the [CERN Open Hardware Licence Version 2 - Strongly Reciprocal (CERN OHL-S v2)](https://ohwr.org/cern_ohl_s_v2.txt).

## Author

**Abhi90808** — [GitHub Profile](https://github.com/Abhi90808)
