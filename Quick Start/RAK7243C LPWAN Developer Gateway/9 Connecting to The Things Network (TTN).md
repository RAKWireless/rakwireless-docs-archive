---
type: page
title: Connecting to The Things Network (TTN)
listed: true
slug: connecting-to-the-things-network--ttn-
---published

The Things Network is about enabling low power devices to use long range gateways to connect to an open-source, decentralized network to exchange data with Application. Learn more about the Things Network [here](https://www.thethingsnetwork.org/docs/).

- First, you should have connected your gateway to the router in order to access the internet according to the method which has been introduced in the [auto$](/rak7243c-lorawan-developer-gateway/accessing-the-internet) section of this document.
- Second, config your gateway and choose TTN as the LoRa® Server and choose a correct frequency according to the method which has been introduced in the [Configuring the Gateway](/quick-start/rak7243-lorawan-developer-gateway/configuring-the-gateway#server-is-ttn) section.
- Now go to the TTN Website: [https://www.thethingsnetwork.org/](https://www.thethingsnetwork.org/) and Login. You will then see the following page:

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1591359079\/13904\/gktuz4nt1demsyiyongx.png",
        "mode": "responsive",
        "width": 1934,
        "height": 945,
        "caption": "**Figure 1:** The Things Network Home Page"
    }
}]$

- Choose Console then Click Gateway.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1591359097\/13904\/og8oo9luzunouuoofkbu.png",
        "mode": "responsive",
        "width": 1914,
        "height": 943,
        "caption": "**Figure 2:** The Things Network Console Page"
    }
}]$

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1591359112\/13904\/sepw7lzg7vxnctaw3b8q.png",
        "mode": "responsive",
        "width": 1934,
        "height": 943,
        "caption": "**Figure 3:** Adding a Gateway to TTN"
    }
}]$

- All of your Registered Gateways will be displayed here in this page. Click "register gateway"

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1591359157\/13904\/bmxxaau3bgmpgj2kedyf.png",
        "mode": "responsive",
        "width": 1915,
        "height": 945,
        "caption": "**Figure 4:** Registering your Gateway"
    }
}]$

$plugin[{
    "type": "callout",
    "data": {
        "text": "Make sure to select the \"**I'm using the legacy packet forwarder**\" check box.",
        "type": "info",
        "title": "Note:"
    }
}]$

- **Gateway EUI** - refers to the Gatway ID you obtained from the previous step. In case you forgot, just type "**gateway-version**" in the command line. This must be the same with the gateway's True Gateway ID otherwise you will fail to register your gateway on TTN.
- **Description** - A human readable description of your gateway.
- **Frequency Plan** - This is the frequency you want to use and it must be the same with gateway and the node.
- **Router** - The router this gateway will connect to. To reduce latency, pick a router that is in a region which is close to the location of the gateway.
- **Location** - Choose the location of the gateway by entering its coordinates. This is reflected on the Gateway World Map!
- **Antenna Placement** - refers to the location of your antenna whether indoor or outdoor.

Click Register Gateway and wait for a couple of minutes . If the status of your gateway is **Connected**, Congratulations! Your gateway is now connected to the The Things Network (TTN).

