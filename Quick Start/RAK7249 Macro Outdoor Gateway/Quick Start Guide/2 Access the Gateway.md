---
type: page
title: Access the Gateway
listed: true
slug: access-the-gateway
---published

### Wi-Fi AP Mode

By default, the Gateway will work in Wi-Fi AP Mode which means that you can find an SSID named like "**RAK7249_XXXX**" on your PC's Wi-Fi Network List. "XXXX" is the last two bytes of the Gateway MAC address. To access the Web Management Platform, input the IP Address: **192.168.230.1** in your Web browser.

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
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1586512083\/27672\/okvqxiyqxijphxovxdtu.jpg",
        "mode": "responsive",
        "width": 4170,
        "height": 3257,
        "caption": "**Figure 1:** Accessing the Gateway via Wi-Fi AP Mode"
    }
}]$

### WAN Port (Ethernet)

Connect the Ethernet cable to the port marked “ETH” on the Gateway and the other end to the PoE port of the PoE injector. Connect the LAN port of the PoE injector to your PC.

The default IP is **169.254.X.X**. The last two segments(X.X) are mapped from the last four bits of the MAC address of your gateway. For example, the last four bits of the MAC address are 0F:01, and the IP address is 169.254.15.1. Make sure to manually set the address of your PC to one in the same network (for example 169.254.15.100). Use the same credentials for the Web UI as for AP mode.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1586512126\/27672\/cjrru7khtd2gvgcwsxdi.jpg",
        "mode": "responsive",
        "width": 4170,
        "height": 3257,
        "caption": "**Figure 2:** Accessing the Gateway via Ethernet"
    }
}]$

