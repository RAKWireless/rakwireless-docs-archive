---
type: page
title: Accessing the Gateway
listed: true
slug: accessing-the-gateway
---published

## 1. Via WiFi

By default the Gateway is configured to work in **Access Point** (AP) mode. The default SSID format is "**RAKxxxx_xxxx**” such as "**RAK7258_ D3BD**", “**D3BD**” is the last two bytes of the Gateway **MAC address.** The WEB management platform can be accessed through the IP address **192.168.230.1** of the gateway LAN interface thru the use of a browser.

$plugin[{
    "type": "callout",
    "data": {
        "text": "1. No password is required to connect via WiFi\n2. UI user & password : root",
        "type": "info",
        "title": "Notes:"
    }
}]$

## 2. Via WAN Port DHCP IP

When DHCP Server is in the network where the gateway WAN interface is located, the WAN interface can automatically get the IP address. After inquiring the IP address of the gateway through DHCP Server, the WEB management platform of the gateway can be accessed through the DHCP IP address of WAN interface.

