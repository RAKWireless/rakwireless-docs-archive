---
type: page
title: Interfaces
listed: true
slug: interfaces-rak2245-stamp-edition
---published

### The SX1301 digital baseband chip contains **10 programmable reception paths**. These
paths have different levels of programmability and has a variety of cases. It is
important to understand the differences between those demodulation paths to make the
best possible use from the system.

### Power Supply

RAK2245 Stamp Edition - LPWAN Gateway Concentrator Module is powered through **5V**. It integrates the **IOREF** for
Level Translator, which can communicate with **3.3V**, **1.8V** and other different voltage
interfaces.

### SPI Interface

The pin connector provides an SPI connection which allows direct access to the **Sx1301 SPI interface**. This gives the target system the possibility to use existing SPI interfaces to communicate with the module.

$plugin[{
    "type": "callout",
    "data": {
        "text": "Reset SX1301 via PIN A13 after turning on your RAK2245 Stamp Edition - LPWAN Gateway Concentrator Module",
        "type": "info",
        "title": "Note"
    }
}]$

### UART and I²C

UART and I²C connections are also included on the pin connector. These connections allow direct access to the GPS module. The **1PPS** is connected internally to SX1301.

### Digital IOs

There are two digital IO PINs, which give the user an interface to reset the GPS module or set it into standby mode.

### LEDs

There are three (3) Green LED that indicates the status of PWR, TX, RX.

### Antenna RF Interface

The modules have two RF interfaces for LoRa® and GPS antennas over the standard UFL connectors (Hirose U. FL-R-SMT). It has a characteristic impedance of **50Ω** and supports both Tx and Rx via RF ports, providing the antenna interface.

