---
type: page
title: Connecting to The Things Network (TTN)
listed: true
slug: connecting-to-the-things-network--ttn-
---published

The Things Network is about enabling low power devices to use long range gateways to connect to an open-source, decentralized network to exchange data with Application. Learn more about The Things Network [here](https://www.thethingsnetwork.org/docs/).

- First, you should have connected your RAK7249 Macro Outdoor Gateway to the router in order to access the internet according to the method which has been introduced in the [auto$](/rak7240-outdoor-lpwan-gateway/access-the-internet) section of this document.
- Now go to the TTN Website: [https://www.thethingsnetwork.org/](https://www.thethingsnetwork.org/) and Login. You will then see the following page:

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1591344878\/27674\/m1tjf5bhhiyls0morlo3.png",
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
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1591344877\/27674\/k2worqkie8hch5skusiz.png",
        "mode": "responsive",
        "width": 1915,
        "height": 945,
        "caption": "**Figure 2:** Registering your Gateway"
    }
}]$

$plugin[{
    "type": "callout",
    "data": {
        "text": "The Gateway EUI can be found either on the sticker on the casing or via the LoRa\u00ae Packet Forwarder page in the LoRa\u00ae Gateway menu once you log via the Web UI.",
        "type": "info",
        "title": "Note:"
    }
}]$

2.Select your [Frequency Plan](https://www.thethingsnetwork.org/docs/lorawan/frequency-plans.html) depending on your location. This should populate the Router field. Optionally you can choose to enter the Gateway coordinates in the map’s upper right corner and select if the gateway is indoor or outdoor via the Antenna placement field below the map.

3.Upon successful registration you should see the following screen:

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1591344908\/27674\/tbcobt37pia4xrrxvidd.jpg",
        "mode": "responsive",
        "width": 1896,
        "height": 928,
        "caption": "**Figure 3**: Gateway successfully connected to The Things Network (TTN)"
    }
}]$

$plugin[{
    "type": "callout",
    "data": {
        "text": "By default, the Gateway is set to connect to TTN. For detailed information about advanced configuration options refer to the [LoRaWAN\u00ae Gateway Configuration](\/quick-start\/rak7249-macro-outdoor-gateway\/lora-gateway-configuration#1lora%C2%AE-packet-forwarder) section.",
        "type": "info",
        "title": "Note:"
    }
}]$

