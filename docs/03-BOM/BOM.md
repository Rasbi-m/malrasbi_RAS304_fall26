---
title: Bill of Materials
---

## Interpretation board

This list follows simplified schematic revision D-simple. Quantities are one per reference below; repeated values appear on separate rows. Purchased driver modules include their onboard support components. Prices and final PCB footprints remain to be confirmed.

| Reference | Component / value |
|---|---|
| J1 | 9-12 V IN |
| F1 | 500 mA |
| D1 | 1N5819 |
| U1 | LM7805CT |
| C1 | 330nF / 25V |
| C2 | 47uF / 25V |
| C3 | 100nF / 16V |
| C4 | 100uF / 16V |
| U2 | PIC18F57Q43 Nano |
| C5 | 100nF / 16V |
| J2 | UART IN |
| J3 | UART OUT |
| R1 | 1k |
| D2 | GREEN |
| R4 | 22k |
| R5 | 1k |
| C8 | 47nF / 16V |
| R6 | 1k |
| C9 | 47nF / 16V |
| U3 | PAM8302 module |
| R7 | 470R |
| C10 | 100nF / 16V |
| LS1 | 8 ohm / 1 W |
| U4 | DRV2605L QT module |
| C11 | 100nF / 16V |
| R8 | 10k |
| M1 | 3 V vibration motor |

The speaker and vibration motor are external loads. The board also needs the regulator heatsink and suitable input fuse clips. Confirm physical connector and module footprints before PCB layout.

[Component choices](../02-Component-Selection/Component-Selection.md) | [Schematic and complete BOM CSV in KiCad ZIP](../04-Schematic/Mohammed-Interpretation-KiCad.zip)
