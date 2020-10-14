---
type: page
title: Interfaces
listed: true
slug: interfaces---rak7431-rs485-to-lorawan-converter
---published

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1579189643\/-1\/cvxvqwja7hv9bguzkbha.jpg",
        "mode": "responsive",
        "width": 564,
        "height": 300,
        "caption": "**Figure 1**: RAK7431 bottom panel"
    }
}]$

### Power Supply and Configuration Interface

RAK7431 can be powered by its DC terminal or via its Micro USB port.

The
DC terminal accepts 8-48V DC input, and the rated power of the device is 1W. Pay attention to the positive and negative pole directions when crimping the terminal. Vin
is connected to the positive pole of the power supply, and GND is connected to
the negative pole of the power supply.

The Micro USB port can also be used for powering the device (5V / 500mA DC). At
the same time, the Micro USB port can be used as the configuration interface of
the device.

Connect
it to a PC and use the [**RAK
Serial Port Tool**](https://downloads.rakwireless.com/en/LoRa/Tools/RAK_SERIAL_PORT_TOOL_V1.2.1.zip) to
open a COM port. The default baud rate is 115200. There is a standard set of AT
commands that can be used to configure the RAK7431.

### Data Interface

When connecting to RS485 nodes, please connect 485A and 485B on the data interface of RAK7431 with the A and B lines of the RS485 bus. Connect the GND terminal to the GN line of the RS485 devices The RS485 bus carrying capacity of RAK7431 goes up to 16 RS485 terminals at the same time.

The Vout on the data interface can supply power to the RS485 terminals.

$plugin[{
    "type": "callout",
    "data": {
        "text": "Only valid when using the DC input interface power supply, USB power\nsupply is invalid.",
        "type": "warning",
        "title": "Warning!"
    }
}]$

Also, the Vout output voltage is the same as DC input voltage Vin.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1579196687\/-1\/wqofcnztdwgsn77u8rpo.jpg",
        "mode": "responsive",
        "width": 584,
        "height": 247,
        "caption": "**Figure 2**: RAK7431 ModBus connection diagram"
    }
}]$

### Reset key and indicator LED

| **Reset<br>Key** | Press<br>the reset key shortly to restart the system | 
| ---- | ---- | 
| **Red<br>LED** | Power<br>indicator (Only valid when using the USB power) | 
| **Green<br>LED** | System<br>working indicator, flashing when there is data transmission | 


