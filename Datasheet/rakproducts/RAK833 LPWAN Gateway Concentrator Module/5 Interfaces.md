---
type: page
title: Interfaces
listed: false
slug: interfaces-rak833
---published

### GPS_PPS

RAK833 LPWAN Gateway Concentrator Module includes the GPS_PPS input for received packets time-stamped.

The RAK833 LPWAN Gateway Concentrator Module integrates one SX1301 chip, two SX1255/7 and other chip for RF signal, which represents the core of the device, providing the related LoRa® modem and processing functionalities. Additional signal conditioning circuitry is implemented for PCI Express Mini Card compliance, and one u.FL connectors are available for external antennas integration.

### Module supply input

RAK833 LPWAN Gateway Concentrator Module must be supplied through the **3.3Vaux** pins by a DC power supply. The voltage must be stable, because during this operation the current drawn from 3.3Vaux can vary significantly based on the power consumption profile of the SX1301 chip (see [SX1301 DS](https://www.semtech.com/uploads/documents/sx1301.pdf) datasheet).

### Antenna RF interfaces

The modules have one RF interface over a standard **UFL connectors** (Hirose U. FL-R-SMT) with a characteristic impedance of 50 Ω. The RF port (ANT1) supports both Tx and Rx, providing the antenna interface.

### SPI interface

An SPI interface is provided on the PCIe_SCK, PCIe_  MISO, PCIe_MOSI, PCIe_ CSN pins of the system connector. The SPI interface gives access to the configuration register of SX1301 via a synchronous full-duplex protocol. Only the slave side is implemented.

### USB interface

$plugin[{
    "type": "callout",
    "data": {
        "text": "This feature is not available for RAK833-SPI version",
        "type": "warning",
        "title": "Note:"
    }
}]$

RAK833 LPWAN Gateway Concentrator Module can support the high speed USB to SPI by **FT2232H**, it includes a high-speed USB 2.0 compliant interface with maximum 480 Mb/s data rate, representing the interface for any communication with an external host application processor. The module itself acts as a USB device and can be connected to any USB host equipped with compatible drivers. For more information, please refer to the data sheet of [FT2232H](https://www.ftdichip.com/Support/Documents/DataSheets/ICs/DS_FT2232H.pdf).

### RESET

RAK833 LPWAN Gateway Concentrator Module includes the RESET active-high input signal to reset the radio operations as specified by the SX1301 Specification.

### SPDT_SEL

RAK833 LPWAN Gateway Concentrator Module includes the SPDT_SEL input for selecting SPI or USB interface.

- SPDT_SEL="H", USB Port Enable, 
- SPDT_SEL="L", SPI Port Enable.

