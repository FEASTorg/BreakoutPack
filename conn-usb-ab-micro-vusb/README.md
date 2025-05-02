# Conn: USB Micro-AB with VBUS Circuitry

## info

Main functionality is to provide "VUSB circuitry" for AVR microcontrollers. Can also be used as generic uUSB breakout by shorting 68R resistor footprints or as breadboard power supply (supplying 5V).

Allows for supplying different voltages by populating the bottom side with desired regulator. The following modes are possible:

- Supply rail and Vcc pin with 5V directly from USB (regulator not populated, short all 3 pads of solder jumper)
- Supply regulator with 5V from USB which in turn supplies rail and Vcc pin (short center and top pad)
- Supply regulator from rail and get regulated voltage on Vcc pin (short center and bottom pad)

## parts dump

-
