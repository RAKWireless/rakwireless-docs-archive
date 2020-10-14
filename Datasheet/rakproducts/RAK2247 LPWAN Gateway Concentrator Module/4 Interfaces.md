---
type: page
title: Interfaces
listed: false
slug: interfaces-rak2247
---published

## Block Diagram

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1586178247\/17458\/fzfomotctdmmo2me4cpl.jpg",
        "mode": "responsive",
        "width": 3088,
        "height": 785,
        "caption": "**Figure 1:** RAK2247 LPWAN Gateway Concentrator Module Block Diagram"
    }
}]$

RAK2247 LPWAN Gateway Concentrator Module integrates one SX1301 chip and two SX1255/7. The other chip is for RF signal, which represents the core of the device. This provides the related LoRa® modem and processing functionalities. Additional signal conditioning circuitry is implemented for PCI Express Mini Card compliance, and one uFL connectors are available for external antennas integration.

## Power Supply

RAK2247 LPWAN Gateway Concentrator Module must be supplied through the **3.3Vaux** pins by a **DC power supply**. The voltage must be stable, because during this operation the current drawn from 3.3Vaux can vary significantly, based on the power consumption profile of the SX1301 chip (please refer to **SX1301 [datasheet](https://www.semtech.com/uploads/documents/sx1301.pdf)**).

## SPI Interface

SPI interface is provided on the PCIe_SCK, PCIe_  MISO, PCIe_MOSI, PCIe_ CSN pins of the system connector. The SPI interface gives access to the configuration register of SX1301 via a synchronous full-duplex protocol. Only the slave side is implemented.

$plugin[{
    "type": "callout",
    "data": {
        "text": "RAK2247-USB version does not have this interface.",
        "type": "info",
        "title": "Note:"
    }
}]$

## USB Interface

RAK2247 LPWAN Gateway Concentrator Module can support the high speed USB to SPI by FT2232HL, it includes a USB 2.0 compliant interface with maximum 480 Mb/s data rate, representing the interface for any communication with an external host application processor. The module itself acts as a USB device and can be connected to any USB host equipped with compatible drivers. For more information, please refer to the [datasheet](https://www.ftdichip.com/Support/Documents/DataSheets/ICs/DS_FT2232H.pdf) of FT2232HL.

$plugin[{
    "type": "callout",
    "data": {
        "text": "RAK2247-SPI version does not have this interface.",
        "type": "info",
        "title": "Note:"
    }
}]$

## GPS_PPS

RAK2247 LPWAN Gateway Concentrator Module includes the GPS_PPS input for received packets time-stamped.

## RESET

RAK2247 LPWAN Gateway Concentrator Module includes the RESET active-high input signal to reset the radio operations as specified by the SX1301 Specification.

## LEDs

Three (3) Green LED for indicating the status of **PWR**, **TX**, **RX**.

## Antenna RF Interface

The modules have one RF interfaces over a standard uFL connectors (Hirose U. FL-RSMT) with a characteristic impedance of **50Ω**. The RF port (J1) supports both Tx and Rx, providing the antenna interface.

