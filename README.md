# Energy Monitor FeatherWing

Eagle sources for an Energy Monitor FeatherWing PCB for Adafruit Feather M0 (ATSAMD21)

## Features

* 3 3.5mm jacks for current transformers (R3=R6=R9=22Ω burden resistor for YHDC SCT-013-000)
* 3 pairs of screw terminals (J1) (≤12VAC) for real power/power factor readings

## Software

An Arduino sketch that publishes MQTT feeds can be found at [ndoo/Energy-Monitor-ATSAMD21](https://github.com/ndoo/Energy-Monitor-ATSAMD21)

## Prerequisites/Caveats

* Designed for [Adafruit M0 Feather](https://www.adafruit.com/product/3010)
* Uses 6 analog pins (won't work with other Adafruit Feathers with fewer analog pins)
* Uses ATSAMD21 internal 12-bit ADC
* No built-in rectifier/regulator to power itself from 12VAC terminals
* Must be top FeatherWing in a stack as the TRS jacks obstruct some Feather pins

## BOM

* See "Seeed Fusion PCBA BOM.csv" for a CSV file that can be used with [Seeed Studio's Fusion PCBA service](https://www.seeedstudio.com/fusion_pcb.html)
* 2.54mm pin header strips: 16-pin + 4-pin
* 2.54mm screw terminal: 6-pin

## Assembly

1. Solder SMD passives (I suggest using a PCBA service as I used 0204 parts)
2. Solder 2.54mm screw terminal
3. Solder 2.54mm pin headers
4. Connect 12VAC input(s)
5. Connect current transformer(s)
6. Configure and upload sketch to Feather M0
7. Stack FeatherWing and power up
