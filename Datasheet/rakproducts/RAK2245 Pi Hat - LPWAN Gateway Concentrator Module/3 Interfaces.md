---
type: page
title: Interfaces
listed: true
slug: interfaces-rak2245-pi-hat
---published

The SX1301 digital baseband chip contains **ten (10) programmable reception paths**. Those
paths have differentiated levels of programmability and allow different use cases. It is
important to understand the differences between those demodulation paths to make the
best possible use from the system.

### Power Supply

RAK2245 Pi HAT module is powered through **5V or 3.3V power pins**.

### SPI Interface

The pin connector provides an SPI connection which allows direct access to the
**Sx1301 SPI interface**. This gives the target system the possibility to use existing SPI
interfaces to communicate with the module.

$plugin[{
    "type": "callout",
    "data": {
        "text": "Reset SX1301 via PIN 11 after turning on RAK2245 Pi HAT.",
        "type": "info",
        "title": "Note"
    }
}]$

### UART and I²C

UART and I2C connections are also included on the pin connector. These connections
allow direct access to the GPS module. The 1PPS is connected internally to SX1301.

### Digital IOs

There are two digital IO PINs, which give the user an interface to reset the GPS module or set it into standby mode.

### LEDs

There are **three (3) Green LED** that indicates the status of PWR, TX, RX.

### Antenna RF Interface

The modules have two RF interfaces for LoRa® and GPS antennas over the standard UFL connectors (Hirose U. FL-R-SMT). It has a characteristic impedance of **50Ω** and supports both Tx and Rx via RF ports, providing the antenna interface.

