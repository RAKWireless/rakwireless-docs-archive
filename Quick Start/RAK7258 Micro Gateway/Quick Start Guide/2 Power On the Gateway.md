---
type: page
title: Power On the Gateway
listed: true
slug: power-on-the-gateway
---published

1.Attach the LoRa® Antenna

First and foremost screw on the antenna to the SMA connector back panel of the RAK7258 Micro Gateway

$plugin[{
    "type": "callout",
    "data": {
        "text": "Do not power the device if the LoRa\u00ae Antenna port has been left open to avoid potential damage in the RAK7258 Micro Gateway.",
        "type": "warning",
        "title": "Warning:"
    }
}]$

2.**Power** the Gateway **ON**

It is recommended to use the **12V DC adapter** that comes with the RAK7258 Micro Gateway. Optionally, you can use your own **PoE cable** and **injector** since the device supports PoE.

## Casing and Ports

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1561434219\/13908\/tryhhofzndj3pevwrhho.png",
        "mode": "responsive",
        "width": 597,
        "height": 644,
        "caption": "**Figure 1**: RAK7258 Micro Gateway Back Panel"
    }
}]$

### Status LED Indicators

| **LEDs** | **Status Indication** | 
| ---- | ---- | 
| **PWR** | Power Indicator, LED is on when the device is powered | 
| **ETH** | **ON**– link is up<br><br>**OFF** – link is down<br>**Flashing** – Data is being transferred | 
| **LoRa**® | **ON** - LoRa® module status is up<br><br>**OFF** – LoRa® module status is down <br><br>**Flashing** – LoRa® module data is being transferred | 
| **ACT** | Reserved for future use | 
| **STAT** | Reserved for future use | 
| **WLAN** | AP Mode :<br><br>**ON** - WLAN status is up<br><br>**Flashing** - Data is being transferred<br><br>STA Mode :<br><br>**Slow Flashing (1Hz)** - Disconnected<br><br>**ON** - Connected<br>**Flashing** - Data is being transferred | 


### Reset Key Functions

The function of the **Reset** key is as follows:

1. **Short press**: Restarts the Gateway
2. **Long press** (**5 seconds and above**): Restore Factory Settings

