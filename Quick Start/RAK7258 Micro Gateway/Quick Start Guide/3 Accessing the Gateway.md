---
type: page
title: Accessing the Gateway
listed: true
slug: accessing-the-gateway
---published

In this document, several ways in accessing the gateway are provided to have different alternatives for you to choose depending on the availability of the requirements needed.

$plugin[{
    "type": "callout",
    "data": {
        "text": "Do not power the device if the LoRa\u00ae Antenna port has been left open to avoid potential damage in the RAK7258 Micro Gateway.",
        "type": "warning",
        "title": "Warning:"
    }
}]$

### Wi-Fi AP Mode

By default, the gateway will work in Wi-Fi AP Mode which means that you can find an SSID named like "**RAK7258_XXXX**" on your PC's Wi-Fi Network List. "**XXXX**" is is the last two bytes of the Gateway MAC address.

$plugin[{
    "type": "callout",
    "data": {
        "text": "The WEB management platform can be accessed through the IP address of the gateway LAN interface provided below through the use of a browser.\n\n1. No password is required to connect via WiFi\n2. IP Address: **192.168.230.1**\n3. WEB Management Platform username and password: **root**",
        "type": "info",
        "title": "Notes:"
    }
}]$

### WAN Port DHCP IP

When DHCP Server is in the network where the gateway WAN interface is located, the WAN interface can automatically get the IP address. After inquiring the IP address of the gateway through DHCP Server, the WEB management platform of the gateway can be accessed through the DHCP IP address of WAN interface.

