# BreakoutPack

BreakoutPack is an open-source collection of breakout boards for ICs, connectors, sensors, and other components, designed in KiCad to support easy integration and rapid electronics development.

## 📦 BreakoutPack Summary

| Folder Name                      | Category | Description                                                                                                         |
| -------------------------------- | -------- | ------------------------------------------------------------------------------------------------------------------- |
| `conn-audio35-3p`                | `conn`   | 3.5mm 3-conductor audio jack breakout                                                                               |
| `conn-combo-rca2-audio35-5p-2sw` | `conn`   | Dual RCA + 3.5mm combo jack with 5 pins, 2 switches                                                                 |
| `conn-dsub-db9-da15-de15`        | `conn`   | Breakout for multiple D-sub connectors (DB9, DA15, DE15)                                                            |
| `conn-rca`                       | `conn`   | Single RCA audio connector breakout                                                                                 |
| `conn-uart-matrix-6p`            | `conn`   | UART signal matrix breakout for re-routing FTDI-style 6-pin headers (DTR, RX, TX, VCC, CTS, GND) via solder jumpers |
| `conn-usb-b`                     | `conn`   | USB Type-B (standard) 4-pin breakout to header                                                                      |
| `conn-usb-b-mini`                | `conn`   | USB Mini-B 4-pin breakout to header                                                                                 |
| `conn-usb-b-micro`               | `conn`   | USB Micro-B 4-pin breakout to header                                                                                |
| `conn-usb-ab-micro-vusb`         | `conn`   | USB Micro-B breakout with AVR VUSB support, zener protection, and optional 3.3V/5V regulator                        |
| `conn-usb-c-cc`                  | `conn`   | USB Type-C breakout with CC resistor selection, LED, header, and breadboard rail jumper                             |
| `ic-soic16-tssop16-adapter`      | `ic`     | Generic adapter for SOIC-16 and TSSOP-16 ICs                                                                        |
| `ic-soic16-tssop16-combo`        | `ic`     | SOIC/TSSOP-16 adapter with prototyping area                                                                         |
| `ic-soic16-tssop16-proto`        | `ic`     | Prototyping board for SOIC-16/TSSOP-16 ICs                                                                          |
| `ic-soic20-tssop20-adapter`      | `ic`     | Adapter for SOIC-20 and TSSOP-20 ICs                                                                                |
| `ic-soic20-tssop20-proto`        | `ic`     | Prototyping board for SOIC-20/TSSOP-20 ICs                                                                          |
| `ic-tsopii44-adapter`            | `ic`     | Generic TSOP-II-44 adapter                                                                                          |
| `ic-tsopii44-cy7c1021bv33`       | `ic`     | TSOP-II-44 adapter for CY7C1021BV33 SRAM chip                                                                       |
| `ic-tsopii44-e6.6`               | `ic`     | TSOP-II-44 adapter with 6.6mm body width                                                                            |
| `input-button-led-smd`           | `input`  | SMD button and LED input board                                                                                      |
| `input-button-rail`              | `input`  | Inline button breakout (likely for chaining/buttons rail)                                                           |
| `led-0805-1x`                    | `led`    | Single 0805 SMD LED breakout with onboard current-limiting resistor                                                 |
| `led-0805-5x`                    | `led`    | Array of five 0805 SMD LEDs with individual resistors for easy prototyping                                          |
| `led-ws2812b`                    | `led`    | Breakout board for WS2812B addressable RGB LED with power, data, and chaining pads                                  |
| `prog-atmega328-attiny-isp`      | `prog`   | ISP breakout for ATmega328 and classic ATtiny MCUs                                                                  |
| `prog-attiny-isp`                | `prog`   | ISP programmer for ATtiny (e.g. ATtiny85)                                                                           |
| `pwr-mcp16252-boost-sot23`       | `pwr`    | Boost converter breakout using MCP16252 in SOT-23                                                                   |
| `pwr-mosfet-dpak-pwm`            | `pwr`    | DPAK/SOT-223 MOSFET breakout for PWM load driving                                                                   |
| `pwr-relay-g2rl-1`               | `pwr`    | SPDT 5V relay breakout for Omron G2RL-1{-E/A-E} (SPDT-NO or SPDT)                                                   |
| `pwr-voltage-inverter-icl7660`   | `pwr`    | Voltage inverter breakout using ICL7660 charge pump to generate a negative voltage from a positive supply           |

### Naming Convention

All breakout board directories and files in this repository follow a standardized, lowercase, dash-separated naming scheme for clarity, scalability, and consistency.

### Format

```bash
[type]-[footprint]-[variant or feature]
```

---

### Components

- **type** – General category of component:

  - `conn` – Connectors (e.g., USB, audio jacks, headers, terminal blocks)
  - `pwr` – Power components (e.g., regulators, converters, relays)
  - `mcu` – Microcontrollers (bare MCU breakouts)
  - `prog` – Programming/debug adapters (e.g., ISP, UPDI, SWD)
  - `ic` – Integrated circuits (op-amps, logic ICs, memory, etc.)
  - `sensor` – Sensors (temperature, pressure, IMUs, etc.)
  - `disp` – Displays (OLED, LCD, 7-segment, etc.)
  - `passive` – Passive components (resistors, capacitors, inductors, pots)
  - `input` – Input components (switches, buttons, DIP switches)
  - `led` – LEDs and indicators (discrete, RGB, arrays)
  - `misc` – Miscellaneous or special-purpose components
  - _(More categories like `rf` or `oscil` can be added as needed)_

- **footprint** – Physical package or interface style:

  - For ICs: `soic8`, `tssop14`, `dip16`, `qfn32`, etc.
  - For connectors: `usb-c`, `usb-micro`, `rca`, `audio35`, `jst-xh-2p`, etc.

- **variant or feature** _(optional)_ – Additional detail for function, layout, or configuration:

  - Examples: `3p` (3-pin), `5x` (5 units), `dual`, `combo`, `proto`, `sw`, `pwm`, `vusb`, `cc`, `matrix`

- **chip or device name** _(optional)_ – Use when a breakout is tailored to a specific part (e.g., `icl7660`, `mcp16252`, `ws2812b`, `g2rl-1e`)

---

### Examples

```text
conn-audio35-3p                 → 3.5mm audio jack (3-conductor, 3-pin)
conn-combo-rca2-audio35-5p-2sw  → Dual RCA + 3.5mm combo jack (5-pin, 2 switches)
ic-tssop14-dual                 → Dual TSSOP-14 IC breakout
pwr-mcp16252-boost-sot23        → MCP16252 boost converter breakout
```
