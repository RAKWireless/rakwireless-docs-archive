---
type: page
title: Network Configuration
listed: true
slug: network-configuration
---published

## 1. WAN Interface

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1562446220\/17329\/rnht0yunpmswtjkl09ql.jpg",
        "mode": "responsive",
        "width": 2132,
        "height": 928,
        "caption": "**Figure 1.** WAN Interface Configuration"
    }
}]$

The user can check the Status (Uptime, IPv4 Address, etc.), or configure the protocol to be used for connecting to your provider’s network. The following options are available: [**DHCP**](https://en.wikipedia.org/wiki/Dynamic_Host_Configuration_Protocol)/[**PPPoE**](https://en.wikipedia.org/wiki/Point-to-Point_Protocol_over_Ethernet)/[**static IP**](https://www.lifewire.com/what-is-a-static-ip-address-2626012) address.

## 2. Cellular Network Configuration

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1562446346\/17329\/okg4w0bibmdve1atneoz.jpg",
        "mode": "responsive",
        "width": 2112,
        "height": 1012,
        "caption": "**Figure 2.** Cellular Interface Configuration"
    }
}]$

The same statistics as with the WAN Interface are available. It is here that you set the **APN**, **User**, and **Password**. The gateway metric determines the priority of this interface, compared with the other connectivity options. The lower the value the higher the priority.

## 3. Wi-Fi

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1562447740\/17329\/e8kxx5rmwcrfjbh8pvs9.jpg",
        "mode": "responsive",
        "width": 2122,
        "height": 1058,
        "caption": "**Figure 3.** Wi-Fi Configuration"
    }
}]$

Enabling/Disabling the Wi-Fi is done from this page via the blue button at the top. Additionally you can pick a radio channel or leave it on Auto configuration. The Wi-Fi can work in one of two modes:

**Access Point:**

By default, there is no password. One can access the Web UI via the IP address: 192.168.230.1 once connected to the AP. The SSID is RAK72xx_xxxx by default.

**Client:**

Choose this option to use Wi-Fi as a backhaul for the Gateway. You need to manually enter the SSID, Encryption method and the Key itself. 

$plugin[{
    "type": "callout",
    "data": {
        "text": "Make sure to click the \u201cSwitch mode\u201d button first in order to input the corresponding parameters, before saving and applying the changes.",
        "type": "info",
        "title": "Note:"
    }
}]$

## 4. Firewall

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1562447833\/17329\/fasgb99gtkidfufkkjsc.jpg",
        "mode": "responsive",
        "width": 2054,
        "height": 1326,
        "caption": "**Figure 4.** Firewall"
    }
}]$

You can configure a number of settings including, but not limited to: **Zones**, **Port Forwarding**, and the **Traffic** and **Custom Rules.**

## 5. Diagnostics

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1562448033\/17329\/km8rj9jrf91mkbjlih94.jpg",
        "mode": "responsive",
        "width": 2128,
        "height": 678,
        "caption": "**Figure 5.** Diagnostics"
    }
}]$

The connection diagnostic tools are in this section: **Ping**, **Traceroute**, **Nslookup**.

You can enter either an URL or an IP Address in the text box and execute the command with the button. Both IPv4 and IPv6 are supported. The results are conveniently displayed in a CLI box.

## 6. Ping Watchdog

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1562448207\/17329\/kot0plihb7jvil1s2bjq.jpg",
        "mode": "responsive",
        "width": 2118,
        "height": 1214,
        "caption": "**Figure 6.** Ping Watchdog"
    }
}]$

Ping Watchdog monitors the quality of network links by constantly pinging the specified IP Address or Domain name on the specified uplink network interface. When network link failures are detected, scheduled measures are taken automatically. Those include: Interface restart, Interface priority reduction, Device restart, etc.

$plugin[{
    "type": "callout",
    "data": {
        "text": "Reducing the priority of an uplink interface only works when the LoRa Gateway uses both Ethernet and Cellular as uplink methods at the same time.",
        "type": "info",
        "title": "Note:"
    }
}]$

WAN interface represents the Ethernet uplink interface and WWAN represents the LTE cellular network uplink interface.

For example if Ping Watchdog is enabled for both uplink interfaces at the same time and the response to degradation of the link quality is set as Increase Gateway Metric the two uplink interfaces work as backups for each other. In the event of significant degradation on one, the Gateway switches to the other.

The Gateway Metric determines the priority of interfaces. The default value can be adjusted in the Network menu for the corresponding interface. The lower the Gateway metric, the higher the priority of the link.

