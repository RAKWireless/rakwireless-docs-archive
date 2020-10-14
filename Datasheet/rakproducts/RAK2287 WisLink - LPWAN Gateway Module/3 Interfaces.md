---
type: page
title: Interfaces
listed: true
slug: interfaces-rak2287
---published

### Power Supply

RAK2287 card must be supplied through the **3.3Vaux** pins by a DC power supply. The voltage needs to be stable since the current drawn can vary significantly during operation based on the power consumption profile of the SX1302 chip. (Check the official datasheet on the [Semtech SX1302](https://www.semtech.com/products/wireless-rf/lora-gateways/sx1302) page).

### SPI Interface

SPI interface mainly provides for the **Host_SCK**, **Host_ MISO**, **Host_MOSI**, **Host_CSN** pins of the system connector. The SPI interface gives access to the configuration register of SX1302 via a synchronous full-duplex protocol. Only the slave side is implemented.

### UART and I2C Interface

RAK2287 integrates the **ZOE-M8Q GPS module** which has **UART** and **I2C** interface. The PINs on the golden finger provide a UART connection and an I2C connection, which allows direct access to the GPS module. The PPS signal is not only connected to SX1302 internally but also connected to the golden finger which can be used by the host board.

### GPS_PPS

RAK2287 card includes
the GPS_PPS input for received packets time-stamped.

### RESET

RAK2287 card includes the RESET active-high input signal to reset the radio operations as specified by the SX1302 Specification[.](#_bookmark73)

### Antenna RF Interface

The module has two RF interfaces over a standard UFL connectors (Hirose U. FL-R-SMT) with a characteristic impedance of **50Ω**. The LoRa® RF port (J1) supports both Tx and Rx, whereas the GNSS RF port (J2) is only RX.

