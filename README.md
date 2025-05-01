# BreakoutPack

BreakoutPack is an open-source collection of breakout boards for ICs, connectors, sensors, and other components, designed in KiCad to support easy integration and rapid electronics development.

## 📦 BreakoutPack Summary

| Folder Name                      | Category | Description                                                                                  |
| -------------------------------- | -------- | -------------------------------------------------------------------------------------------- |
| `conn-audio35-3p`                | `conn`   | 3.5mm 3-conductor audio jack breakout                                                        |
| `conn-combo-rca2-audio35-5p-2sw` | `conn`   | Dual RCA + 3.5mm combo jack with 5 pins, 2 switches                                          |
| `conn-dsub-db9-da15-de15`        | `conn`   | Breakout for multiple D-sub connectors (DB9, DA15, DE15)                                     |
| `conn-rca`                       | `conn`   | Single RCA audio connector breakout                                                          |
| `conn-usb-b`                     | `conn`   | USB Type-B (standard) 4-pin breakout to header                                               |
| `conn-usb-mini`                  | `conn`   | USB Mini-B 4-pin breakout to 0.1" header                                                     |
| `conn-usb-micro`                 | `conn`   | USB Micro-B 4-pin breakout to header                                                         |
| `conn-usb-micro-vusb`            | `conn`   | USB Micro-B breakout with AVR VUSB support, zener protection, and optional 3.3V/5V regulator |
| `conn-usb-c-cc`                  | `conn`   | USB Type-C breakout with CC resistor selection, LED, header, and breadboard rail jumper      |
| `ic-soic16-tssop16-adapter`      | `ic`     | Generic adapter for SOIC-16 and TSSOP-16 ICs                                                 |
| `ic-soic16-tssop16-combo`        | `ic`     | SOIC/TSSOP-16 adapter with prototyping area                                                  |
| `ic-soic16-tssop16-proto`        | `ic`     | Prototyping board for SOIC-16/TSSOP-16 ICs                                                   |
| `ic-soic20-tssop20-adapter`      | `ic`     | Adapter for SOIC-20 and TSSOP-20 ICs                                                         |
| `ic-soic20-tssop20-proto`        | `ic`     | Prototyping board for SOIC-20/TSSOP-20 ICs                                                   |
| `ic-tsopii44-adapter`            | `ic`     | Generic TSOP-II-44 adapter                                                                   |
| `ic-tsopii44-cy7c1021bv33`       | `ic`     | TSOP-II-44 adapter for CY7C1021BV33 SRAM chip                                                |
| `ic-tsopii44-e6.6`               | `ic`     | TSOP-II-44 adapter with 6.6mm body width                                                     |
| `input-button-led-smd`           | `input`  | SMD button and LED input board                                                               |
| `input-button-rail`              | `input`  | Inline button breakout (likely for chaining/buttons rail)                                    |
| `led-0805-1x`                    | `led`    | Single 0805 SMD LED breakout with onboard current-limiting resistor                          |
| `led-0805-5x`                    | `led`    | Array of five 0805 SMD LEDs with individual resistors for easy prototyping                   |
| `led-ws2812b`                    | `led`    | Breakout board for WS2812B addressable RGB LED with power, data, and chaining pads           |
| `prog-atmega328-attiny-isp`      | `prog`   | ISP breakout for ATmega328 and classic ATtiny MCUs                                           |
| `prog-attiny-isp`                | `prog`   | ISP programmer for ATtiny (e.g. ATtiny85)                                                    |
| `pwr-mcp16252-boost-sot23`       | `pwr`    | Boost converter breakout using MCP16252 in SOT-23                                            |
| `pwr-mosfet-dpak-pwm`            | `pwr`    | DPAK/SOT-223 MOSFET breakout for PWM load driving                                            |
| `pwr-relay-spdt-g2rl-1e-5v`      | `pwr`    | SPDT 5V relay breakout using Omron G2RL-1-E DC5 (1 Form C, 16A rated)                        |
| `pwr-relay-spst-g2rl-1a-5v`      | `pwr`    | SPST-NO 5V relay breakout using Omron G2RL-1A-E DC5 (1 Form A, 16A rated)                    |

### Naming Convention

All breakout board directories and files in this repository use a standardized lowercase naming scheme with dashes for clarity and consistency.

### Format

```bash
[type]-[footprint]-[variant or feature]
```

### Components

- **type** – General category of component

  - `conn` – Connectors (audio, USB, headers, terminal blocks, etc.)
  - `pwr` – Power components (regulators, converters, power jacks)
  - `mcu` – Microcontrollers (bare MCU breakouts)
  - `prog` – Programming/debug adapters and headers (e.g. UPDI, JTAG, SWD)
  - `ic` – Integrated circuits (op-amps, logic ICs, etc.)
  - `sensor` – Sensors (temperature, pressure, IMUs, etc.)
  - `disp` – Displays (OLED, LCD, segmented, etc.)
  - `passive` – Passive components (resistors, capacitors, inductors, pots)
  - `input` – Input components (switches, buttons, DIP switches)
  - `led` – LEDs and indicators (discrete LEDs, RGBs, arrays)
  - `misc` – Miscellaneous or special-purpose components
  - More can be added as the library expands (e.g. `rf` or `oscil`)

- **footprint** – Package or physical format

  - Use descriptive terms such as:  
    `rca`, `audio35`, `usb-micro`, `sma`, `dip16`, `soic8`, etc.

- **variant or feature** _(optional)_ –  
  Adds detail on pin count, function, combo boards, or special features like:  
  `3p`, `5p`, `dual`, `combo`, `sw`, `groundplane`, etc.

### Examples

```text
conn-rca                        → Single RCA audio connector breakout
conn-audio35-3p                 → 3.5mm audio jack (3-conductor, 3-pin)
conn-combo-rca2-audio35-5p-2sw  → Dual RCA + 3.5mm combo jack (5-pin, 2 switches)
ic-tssop14-dual                 → Dual TSSOP-14 IC breakout
```
