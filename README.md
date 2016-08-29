# Energy-Monitor-FeatherWing-ATSAMD21
Energy Monitor FeatherWing for Adafruit Feather M0 (ATSAMD21)

## Features

* 3 phases of 3.5mm TRS jacks for YHDC SCT-013-000 100A current transformer
* 3 phases of ≤12VAC input pins for real power monitoring

## Prerequisites/Caveats

* Only works with ATSAMD21 FeatherWing because this uses all 6 analog inputs
* Relies on ATSAMD21 internal ADCs
* Currently no circuitry included to power the Feather off the AC-AC supply
* Other wings cannot be stacked on top of this, as the TRS jacks obstructs the headers

## BOM

* SMD 3.5mm jack - Suntech ST-PJ-312
* 3-phase bridge rectifier - Diodes Inc. SDA006-7
* Everything else are generic jelly bean parts - 0.1" headers, 0204 resistors, capacitors
