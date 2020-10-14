---
type: page
title: Schematic Diagram
listed: false
slug: rak2305-schematic-diagram
---draft

The following sections will describe the schematic of the RAK2305 module.

### Power Supply

Figure 1 shows the schematic of the power supply of the RAK2305 module. In the diagram, VBAT is the battery voltage supplied from the WisBlock base board RAK5005.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1595397326\/32333\/qrgmovlw6lzifjuycbfs.jpg",
        "mode": "responsive",
        "width": 772,
        "height": 283,
        "caption": "**Figure 1:** Power Supply"
    }
}]$

### WisIO Connector

Figure 2 shows the pin definition of WisIO connector. 

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1595398181\/32333\/yaltqjbblcbthdmb4rka.jpg",
        "mode": "responsive",
        "width": 597,
        "height": 592,
        "caption": "**Figure 2:** WisIO Connector"
    }
}]$

| **Name** | **Description** | **Comment** | 
| ---- | ---- | ---- | 
| VBAT | Battery Output Voltage | Max 4.2V | 
| 3V3_R | WisBlock Base Board 3.3V | By Default, No Connected | 
| VDD | 3.3V | By Default, No Connected | 
| TXD0/RXD0 | UART0 interface | Interface for firmware download and log output | 
| TXD1/RXD1 | UART1 interface | Main serial communication interface | 
| LED1/LED2 | LED interface | To control the base board’s LED | 
| EN | ESP32 module Enable | Active High | 


### WisIO Connector Pin Order

Figure 3 shows WisIO connector and its pin order. This connector is located on the bottom side of the module.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1595399028\/32333\/qyituj9fz57evbrjnxaq.jpg",
        "mode": "300",
        "width": 788,
        "height": 676,
        "caption": "**Figure 3:** WisIO Connector Pin Order"
    }
}]$

### Core Module

The core components inside of the RAK2305 module is the ESP32-WROVER-B, which comes with a PCB antenna. The module is designed to work with 3.3V supplied by the base board. In order to prevent any instability on EN (Enable pin), a RC delay circuit is added to this pin, and the EN pin is pulled up to 3.3V by default. The Figure 4 shows the section of the schematic that involves the ESP32-WROVER-B component.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1595399565\/32333\/xvomaaxlfgfgajbvm3yn.jpg",
        "mode": "responsive",
        "width": 1269,
        "height": 660,
        "caption": "**Figure 4:** RAK2305 Core Component's Schematic"
    }
}]$

| **Name** | **Description** | **Comment** | 
| ---- | ---- | ---- | 
| 3.3V | Power Supply | 3.3V | 
| GND | Ground |  | 
| TXD1/RXD1 | UART1 interface | Main communication interface | 
| TXD0/RXD0 | UART0 interface | Interface for firmware update or log output | 
| LED1/LED2 | LED interface | Baseboard LED control | 
| EN | ESP32 Module Enable | Active High | 
| STATUS_LED | LED on module | Active Low | 
| GPIO0 | BOOT0 | Low: UART Download Mode<br><br>High: FLASH Operation<br>Mode | 


