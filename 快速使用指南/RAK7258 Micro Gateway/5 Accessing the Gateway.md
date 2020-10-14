---
type: page
title: Accessing the Gateway
listed: true
slug: accessing-the-gateway
---published

## 1. Via WiFi

By default the Gateway is configured to work in **Access Point** (AP) mode. The default SSID format is "**RAKxxxx_xxxx**” such as "**RAK7258_  D3BD**", “**D3BD**” is the last two bytes of the Gateway **MAC address.**  The WEB management platform can be accessed through the IP address **192.168.230.1** of the gateway LAN interface thru the use of a browser.

$plugin[{
    "type": "callout",
    "data": {
        "text": "1. No password is required to connect via WiFi\n2. UI user & password : root",
        "type": "info",
        "title": "Notes:"
    }
}]$

## 2. Via IP Alias of WAN Port

The WAN interface of the gateway has a **static IP** (Auto IP Alias) generated automatically according to the MAC address. The format of the IP address is **169.254.x.x/255.255.0.0**. The 3 and 4 bytes of IP correspond to the decimal representation of the fifth and sixth bytes of the MAC address, respectively. For example, the MAC address is xx: xx: xx: xx: D3: BD, and the Alias IP is 169.254.211.189/255.255.0.0. Connecting your PC's Ethernet interface to gateway WAN interface, and adding 169.254.x.x/255.255.0.0 IP address to PC's Ethernet interface, then we can access gateway's WEB management platform through Alias IP.

## 3. Via WAN Port DHCP IP

When DHCP Server is in the network where the gateway WAN interface is located, the WAN interface can automatically get the IP address. After inquiring the IP address of the gateway through DHCP Server, the WEB management platform of the gateway can be accessed through the DHCP IP address of WAN interface.

