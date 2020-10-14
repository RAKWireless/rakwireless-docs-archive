---
type: page
title: Connecting to The Things Network (TTN)
listed: true
slug: connecting-to-ttn
---published

The Things Network is about enabling low power devices to use long range gateways to connect to an open-source, decentralized network to exchange data with Application. Learn more about The Things Network [here](https://www.thethingsnetwork.org/docs/).

- First, you should have connected your RAK7258 Micro Gateway to the router in order to access the internet according to the method which has been introduced in the [auto$](/rak7258-micro-gateway/access-the-internet) section of this document.
- Now go to the TTN Website: [https://www.thethingsnetwork.org/](https://www.thethingsnetwork.org/) and Login. You will then see the following page:

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1585804640\/27646\/gwzjctrprhdrzbw3unnu.png",
        "mode": "responsive",
        "width": 1380,
        "height": 681,
        "caption": "**Figure 1**: The Things Network Home Page"
    }
}]$

1.In the **Register Gateway** menu, select the “**I’m using the legacy packet forwarder**” option, and fill-in the Gateway EUI.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1585804705\/27646\/pyabusneqkelp2hs1g8p.png",
        "mode": "responsive",
        "width": 1380,
        "height": 681,
        "caption": "**Figure 2**: Register the Gateway"
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
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1585804780\/27646\/kzhzepe1crs7xzhinmz7.png",
        "mode": "responsive",
        "width": 592,
        "height": 228,
        "caption": "**Figure 3**: Gateway successfully connected to The Things Network (TTN)"
    }
}]$

$plugin[{
    "type": "callout",
    "data": {
        "text": "By default, the Gateway is set to connect to TTN. For detailed information about advanced configuration options refer to the [auto$](\/rak7258-micro-gateway\/lora-gateway-configuration) section.",
        "type": "info",
        "title": "Note:"
    }
}]$

