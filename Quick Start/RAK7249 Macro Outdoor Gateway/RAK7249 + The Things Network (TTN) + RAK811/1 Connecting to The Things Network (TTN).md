---
type: page
title: Connecting to The Things Network (TTN)
listed: true
slug: connecting-to-the-things-network--ttn-
---published

The Things Network is about enabling low power devices to use long range gateways to connect to an open-source, decentralized network to exchange data with Application. Learn more about the Things Network [here](https://www.thethingsnetwork.org/docs/).

**1**.First, you should have connected your LoRaWAN® Gateway to the router in order to access the internet by choosing any option in the [auto$](/rak7249-macro-outdoor-gateway/network) documentation.

**2**.Now go to the TTN Website: [https://www.thethingsnetwork.org/](https://www.thethingsnetwork.org/) and Login. You will then see the following page:

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1583409575\/26710\/gnbwh3mrsjkz9suov42o.png",
        "mode": "responsive",
        "width": 1380,
        "height": 681,
        "caption": "**Figure 1:** The Things Network Home Page"
    }
}]$

**3**.Choose **Console**, then Click **Gateways**.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1583409681\/26710\/xv81wesmf2eviot0nsjy.png",
        "mode": "responsive",
        "width": 1380,
        "height": 681,
        "caption": "**Figure 2:** The Things Network Console Page"
    }
}]$

**4**.All of your Registered Gateways will be displayed here in this page. Click "**register gateway**".

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1583409728\/26710\/bnr2nwzzjceyr4pomoon.png",
        "mode": "responsive",
        "width": 1380,
        "height": 681,
        "caption": "**Figure 3:** Adding a Gateway to TTN"
    }
}]$

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1583409861\/26710\/fivw78r3vatwcitkdrol.png",
        "mode": "responsive",
        "width": 1380,
        "height": 681,
        "caption": "**Figure 4:** Registering your Gateway"
    }
}]$

- **Gateway EUI** - refers to the Gatway ID you obtained in the [LoRaWAN® Gateway Configuration](quick-start/rak7249-macro-outdoor-gateway/lora-gateway-configuration#1lora%C2%AE-packet-forwarder) document.

$plugin[{
    "type": "callout",
    "data": {
        "text": "Make sure to select the \"**I'm using the legacy packet forwarder**\" check box.",
        "type": "info",
        "title": "Note:"
    }
}]$

- **Description** - A human readable description of your LoRaWAN® Gateway.
- **Frequency Plan** - This is the frequency you want to use and it must be the same with LoRaWAN® Gateway and the LoRaWAN® Node.
- **Router** - The router this gateway will connect to. To reduce latency, pick a router that is in a region which is close to the location of the gateway.
- **Location** - Choose the location of the Gateway by entering its coordinates. This is reflected on the Gateway World Map.
- **Antenna Placement** - Where is your antenna placed? Is it placed indoors or outdoors?

Click Register Gateway and wait for a couple of minutes . If the status of your gateway is **Connected**, Congratulations! Your LoRaWAN® Gateway is now connected to the The Things Network (TTN).

