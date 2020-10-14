---
type: page
title: Web Management Platform
listed: true
slug: web-management-platform
---published

This document describes in detail the functionality of the Web Management UI and how to use it for configuration and management of the Gateway. The interface builds on top of OpenWRT and all Gateway products of the RAK72xx line share it.

The document gives instructions on configuring the WAN interface, the LoRa® Packet Forwarder and Gateway MQTT Bridge and more. It explains how to do system-monitoring, update of the firmware and reset the device. Last, but not least it provides information on using the built-in LoRa® Server.

This guide functions as reference for several products with similar functionality. Thus, some sections will apply to certain products and not others. When the word “Gateway” is used it will refer to all three devices when the functionality is the same. In case there is a specific feature or difference the name of the specific device will be mentioned.

$plugin[{
    "type": "callout",
    "data": {
        "text": "This document assumes you have already gone through the Quick Start Guide and you know how to power on and connect to the Gateway and connect it to your network.",
        "type": "info",
        "title": "Note:"
    }
}]$

## Accessing the Web Management Platform

To get started open the browser, enter the IP address of the gateway, and open the login page of the WEB Management Platform. Type-in **root** as the username and password and click login. You can choose in the options provided in this section to access the platform.

### Wi-Fi AP Mode

By default, the Gateway will work in Wi-Fi AP Mode which means that you can find an SSID named like "**RAK7258_XXXX**" on your PC's Wi-Fi Network List. "XXXX" is the last two bytes of the Gateway MAC address. To access the Web Management Platform, input the IP Address: **192.168.230.1** in your Web browser.

$plugin[{
    "type": "callout",
    "data": {
        "text": "No password is required to connect via Wi-Fi.",
        "type": "info",
        "title": "Note:"
    }
}]$

Using your preferred Web browser, input the aforementioned IP Address and you should see the same Log-in Page shown in the following image. Login the credentials provided below:

- **Username**: root
- **Password**: root

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1585451901\/27237\/gdvfil8sxofrfxhw8gqu.jpg",
        "mode": "responsive",
        "width": 1315,
        "height": 610,
        "caption": "**Figure 1**: Web User Interface Log-in"
    }
}]$

### WAN Port DHCP IP

### 
When DHCP Server is in the network where the gateway WAN interface is located, the WAN interface can automatically get the IP address. After inquiring the IP address of the gateway through DHCP Server, the WEB management platform of the gateway can be accessed through the DHCP IP address of WAN interface.

