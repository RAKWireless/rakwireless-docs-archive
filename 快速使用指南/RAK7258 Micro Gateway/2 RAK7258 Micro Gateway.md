---
type: page
title: RAK7258 Micro Gateway
listed: true
slug: rak7258-micro-gateway
---published

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1560847218\/13906\/nxa0fcrgusewtyew9aii.png",
        "mode": "600",
        "width": 3105,
        "height": 2942,
        "caption": "**Figure 1:** RAK7258 Micro Gateway"
    }
}]$

## Product Background

The **RAK7258** is an indoor LoRaWAN Gateway. It comes standard with an Ethernet (PoE supported) connectivity option for a straightforward setup. Additionally there is on-board WiFi, allowing for easy configuration (initial setup can be done over WiFi in AP mode)

Advanced configuration options include LTE CAT 4 Cellular. Thus there are multiple connectivity option to fall back on to in case of a network outage.

The management and configuration software is based on OpenWRT. There is a built-in LoRa packet forwarder and a graphical user interface for ease of configuration. Additionally the Gateway can act as an MQTT Bridge and integrate with other Gateway forwarding application data.

Power over Ethernet (PoE) is supported, making it suitable for mounting on walls or ceilings without running any additional power lines in order to reduce deployment time.

It is a full 8 channel Gateway. It comes with the LoRa antennas included in the packet (together with mounting screws and anchors). With a Line of Sight range of up to 15 km and a 2+ km range in dense urban environments it is a perfect solution for any LoRaWAN use case scenario.

$plugin[{
    "type": "custom-html",
    "data": {
        "contents": "<div class=\"row\">\n\n\t<div class=\"col px-0 text-left\">\n\n\t\t<p><strong> Learn More <\/strong><\/p>\n\n                <ul>\n\n                      <li><a href = \"https:\/\/www.hackster.io\/search?q=RAK7258&i=projects\" >Projects Using the RAK7258<\/a><\/li>\n\n                      <li><a href =\"https:\/\/forum.rakwireless.com\/\" >Community <\/a><\/li>\n\n                      <li><a href=\"mailto:fomi@rakwireless.com\">Support<\/a><\/li>\n\n               <\/ul>  \n\n\t<\/div>\n\n\t<div class=\"col px-0 text-left\" >\n\n\t\t<p><strong> Resources <\/strong><\/p>\n\n                    <ul> \n\n <li><a href = \"https:\/\/downloads.rakwireless.com\/en\/LoRa\/Indoor-Gateway-RAK7258\/Hardware-Specification\/Indoor_Gateway_RAK7258_User_Manual_V1.3.pdf\">RAK7258 User Manual <\/a><\/li>\n\n                \n\n <li><a href = \"https:\/\/downloads.rakwireless.com\/en\/LoRa\/Indoor-Gateway-RAK7258\/Certification-Report\/RAK7258_FCC_Certificate.zip\">FCC Certification Report <\/a> <\/li>\n\n <li><a href = \"https:\/\/downloads.rakwireless.com\/en\/LoRa\/Indoor-Gateway-RAK7258\/Certification-Report\/RAK7258_CE_Certificate.zip\">CE Certification Report <\/a> <\/li>\n\n <li><a href = \"https:\/\/downloads.rakwireless.com\/en\/LoRa\/Indoor-Gateway-RAK7258\/\">RAK7258 Downloadable Files <\/a> <\/li>\n\n\t<\/div>\n\n<\/div>"
    }
}]$

$plugin[{
    "type": "custom-html",
    "data": {
        "contents": "<a href=\"https:\/\/doc.rakwireless.com\/rak7258-micro-gateway\/quick-start-guide\" target=\"_blank\" style=\"background-color: #0c419a; color: white; padding: 12px; border-radius: 3px;box-shadow: 2px 3px 5px 6px #ccc; text-decoration: none !important\">\n\n    Set up Your RAK7258\n\n<\/a>"
    }
}]$

## Product Features

- Full LoRaWAN Stack support (V 1.0.2)
- 100M base-T Ethernet with PoE (802.3 af)
- Multi back-haul backup with Ethernet, WiFi, Cellular (optional LTE Cat 4)
- OpenWRT software supports with Web UI for easy configuration and monitoring
- Can integrate with both private(LoRaServer) and public (TTN) Network Servers
- Built-in LoRaServer for easey deployment of applications and integration of Gateways
- TF card for log backup

## Software Features and UI

| LoRa | Back-haul | Management | 
| ---- | ---- | ---- | 
| Class A, C device support&nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; | WiFi AP/Client mode&nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp;&nbsp; | WEB UI&nbsp; &nbsp; &nbsp; | 
| Built-in LoRaServer | Multi back-haul backup | Supports SSH2 | 
| MQTT Bridge mode | Supports 802.1q | Firmware update | 
| Real Time logger | NAT | Back-up and recovery | 
|  | Firewall | NTP | 


