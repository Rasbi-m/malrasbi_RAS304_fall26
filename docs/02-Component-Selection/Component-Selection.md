---
title: Component Selection
---

# Component Selection

**Mohammed Al Rasbi - Interpretation Board**

Prices and availability below are historical notes from October 21, 2026 (USD, quantity one; tax and shipping excluded), not current purchase quotes.

## Audio amplifier

| Solution | Pros | Cons |
|---|---|---|
| **Option 1: Adafruit 2130 - PAM8302A module**<br>![Adafruit 2130 - PAM8302A module](2130-05.png){ width="150" }<br>$3.95 each<br>[Product link](https://www.adafruit.com/product/2130) | - One channel matches the required warning speaker.<br><br>- Small module and input trim simplify assembly and level adjustment. | - Needs analog audio conditioning from PWM.<br><br>- Available output can exceed the selected speaker rating; limit drive. |
| **Option 2: Adafruit 987 - MAX98306 module**<br>![Adafruit 987 - MAX98306 module](987-11.png){ width="150" }<br>$8.95 each<br>[Product link](https://www.adafruit.com/product/987) | - Selectable gain provides useful volume headroom.<br><br>- Two channels allow a later left/right audio experiment. | - Second channel is unnecessary in this design.<br><br>- Higher price than the mono option; speaker power still needs limiting. |
| **Option 3: Adafruit 1552 - TPA2012 module**<br>![Adafruit 1552 - TPA2012 module](1552-11.png){ width="150" }<br>$9.95 each<br>[Product link](https://www.adafruit.com/product/1552) | - Gain switches simplify prototype tuning.<br><br>- Built-in protection and analog inputs suit a breadboard prototype. | - Costs more than the selected mono module.<br><br>- Unused stereo channel and short-speaker-wire guidance complicate packaging. |

**Choice:** Adafruit 2130 / PAM8302A

**Rationale:** The PAM8302A is compact, inexpensive, and provides the single audio channel needed for warning tones. Its volume trim makes adjustment easier; filter and attenuate the PIC PWM signal and keep output within the speaker rating.

*Product photos and specifications: linked supplier pages.*

## Speaker

| Solution | Pros | Cons |
|---|---|---|
| **Option 1: Adafruit 3923 - mini oval**<br>![Adafruit 3923 - mini oval](3923-06.png){ width="150" }<br>$1.95 each<br>[Product link](https://www.adafruit.com/product/3923) | - Compact shape fits a handheld body.<br><br>- 1 W rating offers more margin than the mini metal option. | - Supplier page currently says out of stock.<br><br>- Short lead and enclosure opening require mechanical planning. |
| **Option 2: Adafruit 1890 - mini metal**<br>![Adafruit 1890 - mini metal](1890-06.png){ width="150" }<br>$1.95 each<br>[Product link](https://www.adafruit.com/product/1890) | - Small, shallow package is easy to place.<br><br>- Attached wires simplify prototype connections. | - Lower continuous rating requires stricter volume limiting.<br><br>- Listed out of stock; title and detailed power ratings differ, so use 0.25 W rated. |
| **Option 3: Adafruit 1313 - 3-inch speaker**<br>![Adafruit 1313 - 3-inch speaker](1313-06.png){ width="150" }<br>$1.95 each<br>[Product link](https://www.adafruit.com/product/1313) | - Mounting tabs provide a secure attachment method.<br><br>- Compatible impedance and power class for the mono amplifier. | - Large diameter and depth consume handheld space.<br><br>- Heavier than the oval option and currently listed out of stock. |

**Choice:** Adafruit 3923 mini oval speaker

**Rationale:** The oval speaker fits the handheld enclosure better than the larger round option and has a higher power rating than the mini metal speaker. It is the preferred design choice, but its listed stock shortage must be resolved before ordering.

*Product photos and specifications: linked supplier pages.*

## Vibration motor driver

| Solution | Pros | Cons |
|---|---|---|
| **Option 1: Adafruit 2305 - DRV2605L**<br>![Adafruit 2305 - DRV2605L](2305-07.png){ width="150" }<br>$7.95 each<br>[Product link](https://www.adafruit.com/product/2305) | - Built-in effects help distinguish warning states.<br><br>- Two I2C signals reduce timing work in the PIC. | - Requires register initialization and motor calibration/settings.<br><br>- Costs more than the generic H-bridge and changes the earlier PWM interface. |
| **Option 2: Adafruit 3297 - DRV8833**<br>![Adafruit 3297 - DRV8833](3297-08.png){ width="150" }<br>$5.95 each<br>[Product link](https://www.adafruit.com/product/3297) | - Low-voltage operation suits a roughly 3 V motor.<br><br>- Protection and current-limiting capability simplify experiments. | - No built-in haptic effect sequencing.<br><br>- Second bridge is unused; default current limit is far above this small motor load. |
| **Option 3: Adafruit 2448 - TB6612**<br>![Adafruit 2448 - TB6612](2448-06.png){ width="150" }<br>$6.95 each<br>[Product link](https://www.adafruit.com/product/2448) | - Separate motor and logic rails can suit larger actuators.<br><br>- Supports direction and speed control with standard digital signals. | - Supplier recommends 4.5-13.5 V motors; poor fit for the selected 3 V ERM.<br><br>- Extra control pins and unused bridge add complexity; rejected for this design. |

**Choice:** Adafruit 2305 / TI DRV2605L

**Rationale:** The DRV2605L provides built-in vibration effects and reduces the software needed to create distinct alerts. Use I2C instead of the earlier PWM-only interface and configure the driver for the selected ERM motor.

*Product photos and specifications: linked supplier pages.*

## Vibration motor

| Solution | Pros | Cons |
|---|---|---|
| **Option 1: Adafruit 1201 - vibrating disc**<br>![Adafruit 1201 - vibrating disc](1201-01.png){ width="150" }<br>$1.95 each<br>[Product link](https://www.adafruit.com/product/1201) | - Enclosed mechanism avoids exposed rotating mass.<br><br>- Low price and compact disc suit grip mounting. | - Requires a driver and controlled motor voltage.<br><br>- Mounting stiffness strongly affects feedback; supplier sheet/model consistency needs checking. |
| **Option 2: Pololu 1637 - shaftless 8 mm**<br>![Pololu 1637 - shaftless 8 mm](pololu1637.png){ width="150" }<br>$6.95 each<br>[Product link](https://www.pololu.com/product/1637) | - Smaller diameter fits a narrow grip.<br><br>- Adhesive backing and specified startup current aid integration. | - Higher price than the selected disc.<br><br>- Supplier shows backorder availability; smaller force needs grip testing. |
| **Option 3: Pololu 2265 - cylindrical ERM**<br>![Pololu 2265 - cylindrical ERM](pololu2265.png){ width="150" }<br>$6.95 each<br>[Product link](https://www.pololu.com/product/2265) | - Flat-sided sleeve helps secure the motor.<br><br>- Narrow profile can fit along the grip wall. | - Exposed eccentric mass needs clearance.<br><br>- Backorder availability and higher price make it less attractive. |

**Choice:** Adafruit 1201 vibrating disc

**Rationale:** The enclosed disc is small, inexpensive, and easy to mount inside the grip. Drive it through the DRV2605L at a nominal 3 V motor setting, then test the strength of the vibration in the enclosure.

*Product photos and specifications: linked supplier pages.*

## Local power regulation

| Solution | Pros | Cons |
|---|---|---|
| **Option 1: Adafruit 2164 - 7805 TO-220**<br>![Adafruit 2164 - 7805 TO-220](2164-00.png){ width="150" }<br>$0.75 each<br>[Product link](https://www.adafruit.com/product/2164) | - Through-hole package is practical for a custom student PCB.<br><br>- Low unit cost and fixed output avoid adjustment errors. | - Needs input headroom, capacitors and thermal design.<br><br>- Heat reduces battery efficiency; verify actual manufacturer/marking before purchase. |
| **Option 2: Adafruit 184 - MIC2941 kit**<br>![Adafruit 184 - MIC2941 kit](184-02.png){ width="150" }<br>$14.95 each<br>[Product link](https://www.adafruit.com/product/184) | - Lower dropout increases input-voltage flexibility.<br><br>- Kit includes heatsink and prototyping connections. | - Large assembled kit and higher cost hurt handheld integration.<br><br>- Listed out of stock; linear heat loss remains despite lower dropout. |
| **Option 3: Pololu 5433 - D45V5F5**<br>![Pololu 5433 - D45V5F5](pololu5433.png){ width="150" }<br>$5.75 each<br>[Product link](https://www.pololu.com/product/5433) | - Switching conversion can reduce battery losses.<br><br>- Very small board with simple VIN/GND/VOUT connections. | - Switching-only solution does not meet the stated linear-regulator direction.<br><br>- Current capability depends on input and temperature; rejected as sole local regulator. |

**Choice:** 7805-based local linear regulator circuit

**Rationale:** The 7805 is inexpensive, easy to solder, and supports the required local linear-regulator approach. The current schematic assumes a 9-12 V input from Jose. Confirm the voltage under load and use the power budget to size the heatsink.

*Product photos and specifications: linked supplier pages.*

## Controller and product requirements

The PIC18F57Q43 Curiosity Nano provides the controller and programming interface for this subsystem. The speaker and vibration motor support nonvisual obstacle alerts, and the small modules fit the handheld concept. The DRV2605L uses I2C; the rotating LiDAR motor is not driven by this board.

The selected Adafruit 2305 is the QT revision with onboard I2C pull-ups. The amplifier and haptic module are powered from the local 5 V rail. The motor's nominal 3 V setting is configured in the driver. The speaker power target for the estimated budget is 0.25 W, below its 1 W rating.

## Proposed MCC configuration

**Planning configuration only.** An MCC project has not been generated or tested. Match these signals in the PIC18F57Q43 MCC pin manager and verify peripheral pin selection before generating code.

| Function | PIC port | Nano connector pin | Proposed configuration |
|---|---|---:|---|
| UART receive from collection board | RC3 | 8 | UART RX, digital input; proposed 9600 baud, 8 data bits, no parity, 1 stop bit. Agree with Khun. |
| Optional UART forwarding | RC2 | 7 | UART TX, digital output; same framing. No destination assigned yet. |
| Haptic clock | RB1 | 10 | I2C SCL, proposed 100 kHz, open-drain configuration. |
| Haptic data | RB2 | 9 | I2C SDA, bidirectional/open-drain configuration. |
| Audio output | RB0 | 46 | PWM output; proposed carrier at least 62.5 kHz with audio duty-cycle modulation. |
| Amplifier enable | RB3 | 47 | Digital output, start low to mute amplifier. |
| Status LED | RD0 | 20 | Digital output, start low. |
| Board power | VTG | 51 | External regulated 5 V. |
| Disable onboard regulator | VOFF | 55 | Grounded in the schematic. |
| Ground | GND | 15, 24, 33, 42, 52 | Common ground. |

Propose a 32 MHz internal system clock and a timer for alert scheduling. Disable analog input mode on digital signal pins. Configure UART, I2C, PWM and GPIO through MCC, checking that each selected peripheral can route to the required pin. The ADC is not required by this design. Leave the board's USB VBUS carrier pin unused.

Initialize the DRV2605L at I2C address 0x5A for the 3 V ERM motor and calibrate it. Receive and validate range packets, choose an alert state, then update audio and vibration. Detect missing or invalid data separately from a clear path; timeout and distance thresholds must be agreed and tested.

[Microchip Nano hardware guide](https://ww1.microchip.com/downloads/aemDocuments/documents/MCU08/ProductDocuments/UserGuides/PIC18F57Q43-Curiosity-Nano-HW-UserGuide-DS40002186B.pdf) |
[DRV2605L pinout](https://learn.adafruit.com/adafruit-drv2605-haptic-controller-breakout/pinouts) |
[Estimated power budget](../05-Power-Budget/Power-Budget.md)

## Purchased substitutions - November 2, 2026

The purchased speaker is Same Sky CMS-30204-18L250 (8 ohm, 1 W), replacing backordered Adafruit 3923. The purchased regulator is ST L7805CV, replacing backordered TI LM7805CT/NOPB. These purchased choices supersede the earlier selections above. See the [BOM](../03-BOM/BOM.md).
