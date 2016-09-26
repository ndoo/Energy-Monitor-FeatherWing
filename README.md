# Energy Monitor FeatherWing

Eagle sources for an Energy Monitor FeatherWing PCB for Adafruit Feather M0 (ATSAMD21)

## Features

* 3 3.5mm jacks for current transformers (R3=R6=R9=22Ω burden resistor for YHDC SCT-013-000)
* 3 pairs of screw terminals (J1) (≤9VAC) for real power/power factor readings

## Software

An Arduino sketch that publishes MQTT feeds can be found at [ndoo/Energy-Monitor-ATSAMD21](https://github.com/ndoo/Energy-Monitor-ATSAMD21)

## Prerequisites/Caveats

* Designed for [Adafruit M0 Feather](https://www.adafruit.com/product/3010)
* Uses 6 analog pins (won't work with other Adafruit Feathers with fewer analog pins)
* Uses ATSAMD21 internal 12-bit ADC
* No built-in rectifier/regulator to power itself from 9VAC terminals
* Must be top FeatherWing in a stack as the TRS jacks obstruct some Feather pins

Note: While I have tried to use ≥10mil design rules, I may have left some 6mil tolerance parts in because Seeed Studios' Fusion PCB service has 6mil tolerances. If you use a different PCB fab, you should run an Eagle DRU check against your chosen fab's tolerances!

## BOM

### PCB BOM

* See "Seeed Fusion PCBA BOM.csv" for a CSV file that can be used with [Seeed Studio's Fusion PCBA service](https://www.seeedstudio.com/fusion_pcb.html)
* 2.54mm pin header strips: 16-pin + 4-pin
* 2.54mm screw terminal: 6-pin

### Transformers

* Current transformer:  YHDC SCT-013-000 100A split core current transformer ([OpenEnergyMonitor](http://shop.openenergymonitor.com/100a-max-clip-on-current-sensor-ct/) [Seeed Studio](https://www.seeedstudio.com/Noninvasive-AC-Current-Sensor-100A-max-p-547.html) [DX.com](http://www.dx.com/p/sct013-0-100a-non-invasive-ac-current-sensor-split-core-current-transformer-blue-359292))
* Voltage transformer:  Ideal Power 77DB-06-09 9VAC transformer ([OpenEnergyMonitor](https://shop.openenergymonitor.com/ac-ac-power-supply-adapter-ac-voltage-sensor-uk-plug/) [element14](http://sg.element14.com/ideal-power/77db-06-09/power-supply-ac-ac-10w-9v-0-67a/dp/2368014))

## Assembly

1. Solder SMD passives (I suggest using a PCBA service as I used 0402 parts)
 * If you solder the AC voltage divider wrongly, you may blow up the 0402 passives or destroy your Feather's LDO!
2. Solder 2.54mm screw terminal
3. Solder 2.54mm pin headers
4. Connect AC monitoring input(s)
5. Connect current transformer(s)
6. Configure and upload sketch to Feather M0
7. Stack FeatherWing and power up
