---
title: Mohammed Al Rasbi
---

# Interpretation Board

**Mohammed Al Rasbi | Team 105 | RAS 304**

Our project is a handheld LiDAR device intended to help visually impaired users notice nearby obstacles through sound and vibration. The enclosure is inspired by a portal gun. My interpretation board receives range information from the data-collection board and controls a warning speaker and a small vibration motor in the grip.

## My contribution

I am responsible for the interpretation controller, audio output, vibration output, and their local power circuitry. The main motor that rotates the LiDAR belongs to the scanning subsystem.

- [Individual block diagram](01-Block-Diagram/Block-Diagram.md)
- [Component selection and proposed MCC configuration](02-Component-Selection/Component-Selection.md)
- [Bill of materials](03-BOM/BOM.md)
- [Schematic and project downloads](04-Schematic/schematic.md)
- [Estimated power budget](05-Power-Budget/Power-Budget.md)

## Current design

The design uses a PIC18F57Q43 Curiosity Nano, PAM8302 speaker amplifier, DRV2605L vibration driver, and a local 5 V regulator. The documentation follows simplified schematic revision D-simple.

Current figures are estimates and controller settings are proposed. Hardware testing and an actual MCC project have not been completed. Team UART levels, data format, and available supply current still need confirmation.

[Team 105 project website](https://ras304-f26-105.github.io/RAS304-F26-105/)
