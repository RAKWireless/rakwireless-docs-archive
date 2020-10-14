---
type: page
title: Interfaces
listed: false
slug: interfaces-rak7258
---published

## Block Diagram

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1586178842\/17516\/d9fyq7zu1ucr8tauk1on.jpg",
        "mode": "responsive",
        "width": 1634,
        "height": 1255,
        "caption": "**Figure 1:** RAK7258 Micro Gateway Block Diagram"
    }
}]$

## Hardware Interfaces

The hardware interfaces of RAK7258 Micro Gateway include DC 12V, ETH interface, Console interface, Reset key, USB port, Nano SIM slot, TF Card slot, six (6) Status indicator LEDs, LoRa® Antenna connector etc. as shown in the following figure.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1590750593\/17516\/hwj9nsnlberfvgtx5wwy.jpg",
        "mode": "responsive",
        "width": 4729,
        "height": 2784,
        "caption": "**Figure 2**: RAK7258 Micro Gateway Hardware Interfaces"
    }
}]$

The function of the Reset key is as follows:

- **Short press**: Restart the Gateway;
- **Long press** (5 seconds and above) : Restore Factory

The status of the LEDs is described as below:

| **LEDs** | **Status Indication Description** | 
| ---- | ---- | 
| PWR | Power Indicator, Led on when device power on | 
| ETH | **ON** - linkup<br><br>**OFF** - linkdown<br><br>**Flash** - Data Transmitting and Receiving | 
| LoRa® | **ON** - LoRa1 is working<br><br>**OFF** - LoRa1 is not working<br><br>**Flash** - Indicate that LoRa1 Packet receiving and sending | 
| ACT | Expanded Led indicator, useless | 
| STAT | Expanded Led indicator, useless | 
| WLAN | **AP Mode** :<br><br>**ON** - WLAN is working;<br><br>**Flash** - Data Transmitting and Receiving<br><br>**STA Mode** :<br><br>**Slow Flash** (1Hz) - Connection Disconnected;<br><br>**ON** - Connection Successful;<br><br>**Flash** - Data Receiving and Sending; | 


## Software Features and UI

| **LoRa**® | **Back-haul** | **Management** | 
| ---- | ---- | ---- | 
| Class A, C device support | WiFi AP/Client mode | WEB UI | 
| Built-in LoRaServer | Multi back-haul backup | Supports SSH2 | 
| MQTT Bridge mode | Supports 802.1q | Firmware update | 
| Real Time logger | NAT | Back-up and recovery | 
|  | Firewall | NTP | 


