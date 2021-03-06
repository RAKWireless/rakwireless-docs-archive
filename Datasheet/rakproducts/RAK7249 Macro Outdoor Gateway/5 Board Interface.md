---
type: page
title: Board Interface
listed: false
slug: board-interface
---published

The figure below shows the components integrated in our RAK7249 Macro Outdoor Gateway.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1590750888\/19284\/fbugplstwspc6hftmlln.jpg",
        "mode": "responsive",
        "width": 1369,
        "height": 606,
        "caption": "**Figure 1:** Circuit Board Interface"
    }
}]$

### Reset Key Functions

The RAK7249 Macro Outdoor Gateway's mainboard provides a Reset key and 6 x LEDs for status indication.The
The function of the Reset key is as follows:

- **Short press**: Restarts the Gateway
- **Long press (5s and above)**: Restore Factory Settings;

### LED Indicators

The status of the LEDs is described as below. Please refer to the printing of the LEDs
on the mainboard.

| **LEDs** | **Status Indication Description** | 
| ---- | ---- | 
| **LED1 (PWR)** | Power Indicator, Led ON when device power on | 
| **LED2 (ETH)** | - **ON** - linkup <br>- **OFF** - linkdown <br>- **Flash** - Data Transmitting and Receiving | 
| **LED3 (LoRa1)** | - **ON** - LoRa1 is working <br>- **OFF** - LoRa1 is not working <br>- **Flash** - Indicate that LoRa1 Packet<br>receiving and sending | 
| **LED4 (LTE)** | - Slow Flash 1 (200ms Bright/1800ms Dark)<br>- Unregistered network (in search) <br>- Slow Flash 2 (200ms Dark/1800ms Bright)<br>- Idle status (online) <br>- Flash - Data Transmitting and Receiving <br>- ON - Voice is working | 
| **LED5 (LoRa2 for 16 channel)** | - **ON** - LoRa2 is working <br>- **OFF** - LoRa2 is not working <br>- **Flash** - Indicate that LoRa2 Packet <br>receiving and sending | 
| **LED6 (WLAN)** | - **AP Mode** : **ON** - WLAN is working **Flash** - Data Transmitting and Receiving<br>- **STA Mode** : **Slow Flash (1Hz)** - Connection Disconnected **ON** - Connection Successful **Flash** - Data Receiving and Sending; | 


