---
type: page
title: Configuring the RAK5010-M WisTrio NB-IoT Tracker
listed: false
slug: configuring-the-rak5010m-wistrio-nb-iot-tracker
---published

You can configure your RAK5010-M WisTrio NB-IoT Tracker by sending AT Commands either through UART or through Micro USB.

$plugin[{
    "type": "callout",
    "data": {
        "text": "For the full list of AT Commands available for configuring your RAK5010-M, kindly check [AT Commands for RAK5010-M WisTrio NB-IoT Tracker](\/quick-start\/rak5010m-wistrio-nb-iot-tracker\/at-commands-for-rak5010m).",
        "type": "info",
        "title": "Note"
    }
}]$

### Through Micro USB

- To begin with, connect your RAK5010-M with your PC through microUSB/USB as shown in the image below:

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1580439043\/20385\/ehzpnpgveqdplcndqwc7.jpg",
        "mode": "responsive",
        "width": 3544,
        "height": 2020,
        "caption": "**Figure 1**: MicroUSB Interface for RAK5010-M"
    }
}]$

- Open the serial port tool in your PC.

$plugin[{
    "type": "callout",
    "data": {
        "text": "Any serial tool will work, but it is recommended to use the **RAK Serial Port Tool** that can be downloaded from [here](https:\/\/downloads.rakwireless.com\/en\/LoRa\/Tools\/RAK_SERIAL_PORT_TOOL_V1.2.1.zip).",
        "type": "info",
        "title": "Note:"
    }
}]$

- Configure the serial communication tool by selecting the proper port of the computer and configure the link as: 115200 bauds, 8 bits, No parity bit and 1 stop bit.
- After pushing the RST button on RAK5010-M, you can see the following contents in the serial port tool, shown in the Figure 5.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1595244468\/32192\/okevqggiyfh9z7lsvvyt.jpg",
        "mode": "300",
        "width": 540,
        "height": 661,
        "caption": "**Figure 2**: RAK serial port tool connected to RAK5010-M"
    }
}]$

### Through UART

- If you want to use RAK5010-M WisTrio NB-IoT Tracker through UART, you should connect the RAK5010-M in your machine through UART as shown in the image below:

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1580438878\/20385\/g1rz6rigcuznvqtlfcb5.jpg",
        "mode": "responsive",
        "width": 6264,
        "height": 2151,
        "caption": "**Figure 3**: RAK5010-M WisTrio NB-IoT Tracker to UART"
    }
}]$

- Try to send a simple AT command to RAK5010-M to get the current firmware’s version by sending the command below using the RAK Serial Port Tool. Similarly, you can send other AT commands of RAK5010-M in the same way.

$plugin[{
    "type": "code-block",
    "data": {
        "languageBlocks": [
            {
                "code": "at+version",
                "language": "none"
            }
        ]
    }
}]$

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1569641409\/20385\/viskdhazv9uu3yxhotid.jpg",
        "mode": "300",
        "width": 538,
        "height": 654,
        "caption": "**Figure 4**: RAK Serial Port Tool, get firmware version"
    }
}]$

