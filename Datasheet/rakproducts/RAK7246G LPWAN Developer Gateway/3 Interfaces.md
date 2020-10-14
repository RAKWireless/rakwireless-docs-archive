---
type: page
title: Interfaces
listed: true
slug: interfaces-rak7246g
---published

### External Module Interfaces

### SPI

The PINs on the connector provide an SPI connection, which allows direct access to the SX1308 SPI interface. This gives the target system the possibility to use existing SPI interfaces to communicate.

$plugin[{
    "type": "callout",
    "data": {
        "text": "After powering up RAK2246, it is required to reset\nSX1308 via PIN 11.",
        "type": "info",
        "title": "Note"
    }
}]$

### UART and I2C

The PINs on the bottom side provide a UART connection and I2C connection, which allows direct access to the GPS module. The 1PPS has been connected to the SX1308 internally.

### Digital IOs

There are two digital IO PINs, which give the user an interface to reset the GPS module or set it into standby mode.

