---
type: page
title: Interfaces
listed: true
slug: interfaces-rak7240
---published

The hardware interfaces of **RAK7240 Outdoor LPWAN Gateway** include five (5) antenna ports: **LoRa**, **LTE-DIV/LoRa2**, **LTE-MAIN**, **WiFi**, and **GPS**, six (6) status indicator LEDs, TF Card and nano-SIM sockets, a console port, an Ethernet Port (PoE), and a ground pad, as shown in figure 1 below:

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1585224166\/27257\/meirxjqlpl9mqo7vwmaz.jpg",
        "mode": "600",
        "width": 657,
        "height": 554,
        "caption": "**Figure 1**: RAK7240 Outdoor LPWAN Gateway Hardware Interfaces"
    }
}]$

### [LED Indicators](https://doc.rakwireless.com/datasheet/rakproducts/board-interface#led-indicators)

The status of the LEDs is described as below. Refer to the printing of the LEDs on the main board.

| **LEDs** | **Status Indication Description** | 
| ---- | ---- | 
| **PWR** | Power Indicator, LED is **ON** when the device is powered | 
| **ETH** | - **ON** – link is up<br>- **OFF** – link is down<br>- **Flashing** – Data is being transferred | 
| **LoRa**® | - **ON** - LoRa® module 1 status is up<br>- **OFF** – LoRa® module 1 status is down<br>- **Flashing** – LoRa® module 1 data is being transferred | 
| **ACT**<br><br>_(LTE)_ | - **Slow Flashing** (_200ms Bright/1800ms Dark)_ - searching for network<br>- **Slow Flashing** (200ms Dark/1800ms Bright) - idle status (online)<br>- **Fast Flashing** - Data is being transferred | 
| **STAT**<br><br>_(16 channels only)_ | - **ON** - LoRa® module 2 status is up<br>- **OFF** – LoRa® module 2 status is down<br>- **Flashing** – LoRa® module 2 data is being transferred | 
| **WLAN** | - **AP Mode**: **ON** - WLAN status is up, **Flashing** - Data is being transferred<br>- **STA Mode**: **Slow Flashing**(1Hz) - Disconnected, **ON** - Connected, **Lashing** - Data is being transferred | 


