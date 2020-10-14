---
type: page
title: Interfaces
listed: true
slug: interfaces-rak831
---published

### External Module Connector

### SPI

The connector on the bottom side provides an SPI connection, which allows direct access to the Sx1301 SPI interface. This gives the target system the possibility to use existing SPI interfaces to communicate.

After powering up RAK831 ,it is required to **reset** SX1301 via **PIN 19.** If the HAL driver from Github is used this functionality is already implemented.

### GPS PPS

In case of available PPS signals in the target system, it is possible to connect this available signal to the appropriate pin at the connector.

### Digital IOs

There are five GPIOs of the Sx1301 available, which gives the user some possibilities to get information about the system status. Theses pins are the same, as they are used for the LEDs on the RAK831 .

Default setting of the LEDs:

1. Backhaul packet
2. TX packet
3. RX Sensor packet
4. RX FSK packet
5. RX buffer not empty
6. Power

