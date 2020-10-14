---
type: page
title: Connecting to The Things Network (TTN)
listed: true
slug: connecting-to-the-things-network--ttn-
---published

The Things Network is about enabling low power devices to use long range gateways to connect to an open-source, decentralized network to exchange data with Applications. Learn more about The Things Network [here](https://www.thethingsnetwork.org/docs/).

- First, you should have connected your RAK7240 Outdoor LPWAN Gateway to the router in order to access the internet according to the method which has been introduced in the [auto$](/rak7240-outdoor-lpwan-gateway/access-the-internet) section of this document.

$plugin[{
    "type": "callout",
    "data": {
        "text": "If your Gateway uses one of the bands **RU864\/IN865\/EU868**, it will by default be configured to work in the **EU868** band.\n\nIf your Gateway uses one of the bands **US915\/AU915\/KR920\/AS923**, it will by default be configured to work in the **US915** band.\n\nExample: A Gateway purchased to work in the IN865 band will by default be configured to work in the EU868 band.\n\nThus, please make sure you select the proper band before continuing.",
        "type": "info",
        "title": "Note"
    }
}]$

- Now go to the TTN Website: [https://www.thethingsnetwork.org/](https://www.thethingsnetwork.org/) and Login. You will then see the following page:

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1591340359\/27385\/jqxljthxqc7pqr0gtxqc.png",
        "mode": "responsive",
        "width": 1934,
        "height": 945,
        "caption": "**Figure 1:** The Things Network Home Page"
    }
}]$

**1.**In the **Register Gateway** menu, select the “**I’m using the legacy packet forwarder**” option, and fill-in the Gateway EUI.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1591340431\/27385\/l5mmcllh5sdmzloeybmd.png",
        "mode": "responsive",
        "width": 1915,
        "height": 945,
        "caption": "**Figure 2:** Registering your Gateway"
    }
}]$

$plugin[{
    "type": "callout",
    "data": {
        "text": "The Gateway EUI can be found either on the sticker on the casing or via the LoRa\u00ae Packet Forwarder page in the Gateway menu once you log via the Web UI.",
        "type": "info",
        "title": "Note:"
    }
}]$

2.Select your [Frequency Plan](https://www.thethingsnetwork.org/docs/lorawan/frequency-plans.html) depending on your location. This should populate the Router field. Optionally you can choose to enter the Gateway coordinates in the map’s upper right corner and select if the gateway is indoor or outdoor via the Antenna placement field below the map.

3.Upon successful registration you should see the following screen:

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1591340463\/27385\/mt51ntjjep7hy2syxsgo.jpg",
        "mode": "responsive",
        "width": 1896,
        "height": 928,
        "caption": "**Figure 3**: Gateway successfully connected to The Things Network (TTN)"
    }
}]$

$plugin[{
    "type": "callout",
    "data": {
        "text": "By default, the Gateway is set to connect to TTN. For detailed information about advanced configuration options refer to the [LoRaWAN\u00ae Gateway Configuration](\/quick-start\/rak7240-outdoor-lpwan-gateway\/lorawan-gateway-configuration#1lora%C2%AE-packet-forwarder) section.",
        "type": "info",
        "title": "Note:"
    }
}]$

