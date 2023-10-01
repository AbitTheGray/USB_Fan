# USB Fan

Single-cell USB Fan with voltage selection and USB-C Charger built around `TP4056`+`DW01A` and `TPS61170`.

![PCB Preview](Preview.png)

**This board is untested.**

Designed to be manufactured by [JLCPCB](https://jlcpcb.com/) as 4layer PCB.
*It is not possible to manufacture as 2layer PCB.*

## Features

- 4 fan voltages (5V / 9V / 12V / 24V)
  - Select **before** turning the SW1 on
- USB-C charging
  - 5V 1.5A max (5.1k resistors)
  - `TP4056` charger
    - Status LEDs
      - Red = Charging
      - Blue = Standby
    - 1S 1A charging (1 cell in series, unlimited in parallel)
  - 1.5A discharge (`DW01A`)
- Power-on switch
  - Only affects the output, battery can still charge
  - **Do not turn on when charging**
  - Minimum current runs through the switch
    - No special switch needed
    - It is not a toggle!

### Warnings

- There are no reverse-polarity protections
  - Not on battery or USB-C
- `D3`+`D4` don't have JLCPCB part number, pick any `1206` LEDs you like
- Default component placement has to be tweaked on JLCPCB online editor
  - `J1` shifted to right position
  - `L1` rotated 90deg
  - `U1`, `U2`, `U3` and `U4` must be rotated so 1st pin is in the corner with long line on Stencil layer
    - `U1` = top right, `U2` = top left, `U3` = bottom right, `U4` = top left

## TODO

- Power LED (white) ?
- Add assembly tooling holes
