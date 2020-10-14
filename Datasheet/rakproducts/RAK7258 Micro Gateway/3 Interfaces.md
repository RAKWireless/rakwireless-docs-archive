---
type: page
title: Interfaces
listed: true
slug: interfaces-rak7258
---published

## Hardware Interfaces

The hardware interfaces of RAK7258 Micro Gateway include **DC 12V**, **ETH interface**, **Console interface**, **Reset key**, **USB port**, **Nano SIM slot**, **TF Card slot**, **six (6) Status indicator LEDs**, L**oRa® Antenna connector,** etc., as shown in figure 1.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1590750593\/17516\/hwj9nsnlberfvgtx5wwy.jpg",
        "mode": "600",
        "width": 4729,
        "height": 2784,
        "caption": "**Figure 1**: RAK7258 Micro Gateway Hardware Interfaces"
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


