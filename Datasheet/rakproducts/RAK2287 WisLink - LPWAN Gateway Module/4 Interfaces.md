---
type: page
title: Interfaces
listed: false
slug: interfaces-rak2287-lora-gateway
---published

### Block Diagram

RAK2287 card is equipped with one SX1302 chip and two SX1250 chips. The first chip is utilized for RF signal processing and is the core of the device. The other two chips provide the related LoRa® front-end functionality and are specifically designed to work in conjunction with the SX1302. Additional signal conditioning circuitry is implemented for PCI Express Mini Card compliance, and there are two UFL connectors for the antennas.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1590171295\/23911\/joksadvxu8hyehstvhlm.jpg",
        "mode": "responsive",
        "width": 2074,
        "height": 1003,
        "caption": "**Figure 1**: RAK2287 Block Diagram"
    }
}]$

### Power Supply

RAK2287 card must be supplied through the 3.3Vaux pins by a DC power supply. The voltage needs to be stable since the current drawn can vary significantly during operation based on the power consumption profile of the SX1302 chip (check the official datasheet on the [Semtech SX1302](https://www.semtech.com/products/wireless-rf/lora-gateways/sx1302) page).

### SPI Interface

SPI interface mainly provides for the Host_SCK, Host_ MISO, Host_MOSI, Host_CSN pins of the system connector. The SPI interface gives access to the configuration register of SX1302 via a synchronous full-duplex protocol. Only the slave side is implemented.

### UART and I2C Interface

RAK2287 integrates ZOE-M8Q GPS module which has UART and I2C interface. The PINs on golden finger provide an UART connection and an I2C connection, which allows direct access to the GPS module. The PPS signal is not only connected to SX1302 internally, but also connected to golden finger which can be used by host board.

### GPS_PPS

RAK2287 card includes
the GPS_PPS input for received packets time-stamped. 

### RESET

RAK2287 card includes the RESET active-high input signal to reset the radio operations as specified by the SX1302 Specification[.](#_bookmark73)

### Antenna RF Interface

The module has two RF interfaces over a standard UFL connectors (Hirose U. FL-R-SMT) with a characteristic impedance of 50Ω. The LoRa® RF port (J1) supports both Tx and Rx, whereas the GNSS RF port (J2) is only RX.

