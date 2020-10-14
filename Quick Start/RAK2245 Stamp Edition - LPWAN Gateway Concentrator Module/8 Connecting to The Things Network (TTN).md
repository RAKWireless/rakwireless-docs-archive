---
type: page
title: Connecting to The Things Network (TTN)
listed: true
slug: connecting-to-the-things-network--ttn-
---published

The Things Network is about enabling low power devices to use long range [g](https://www.thethingsnetwork.org/docs/gateways/)ateways to connect to an open-source, decentralized network to exchange data with Application. Learn more about the Things Network [here](https://www.thethingsnetwork.org/docs/).

- First, you should have connected your  gateway to the router in order to access the internet according to the method which has been introduced in the [auto$](/rak2245-stamp-edition-lorawan-gateway-concentrator-module/accessing-the-internet) section of this document.
- Second, config your  gateway and choose TTN as the LoRa® Server and choose a correct frequency according to the method which has been introduced in the [Configuring the Gateway](/quick-start/rak2245-stamp-edition-lorawan-gateway-concentrator-module/configuring-the-gateway#server-is-ttn) section.
- Now go to the TTN Website: [https://www.thethingsnetwork.org/](https://www.thethingsnetwork.org/) and Login. You will then see the following page:

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1591360516\/16406\/eqsmruy8ncketxqm685w.png",
        "mode": "responsive",
        "width": 1934,
        "height": 945,
        "caption": "**Figure 1:** The Things Network Home Page"
    }
}]$

- Choose Console then Click Gateways.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1591360531\/16406\/wd1fieiwcjzk6blw1xfz.png",
        "mode": "responsive",
        "width": 1914,
        "height": 943,
        "caption": "**Figure 2:** The Things Network Console Page"
    }
}]$

- All of your Registered Gateways will be displayed here in this page. Click "**register gateway**"

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1591360593\/16406\/iroytffzaumicgvq8rr0.png",
        "mode": "responsive",
        "width": 1934,
        "height": 943,
        "caption": "**Figure 3:** Adding a Gateway to TTN"
    }
}]$

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1591360613\/16406\/lnxotnqxwttn6dlqigcc.png",
        "mode": "responsive",
        "width": 1915,
        "height": 945,
        "caption": "**Figure 4:** Registering your Gateway"
    }
}]$

- **Gateway EUI** - refers to the Gatway ID you obtained from the previous steps. In case you forgot, just type "**gateway-version**" in the command line. This must be the same with the  gateway's True Gateway ID otherwise you will fail to register your  gateway on TTN.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1579422745\/24747\/qwotkxwnrkvbc9de76ri.png",
        "mode": "responsive",
        "width": 1605,
        "height": 828,
        "caption": "**Figure 5**: RAK2245 Stamp Edition - LPWAN Gateway ID in SSH"
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

- **Description** - A human readable description of your  gateway.
- **Frequency Plan** - This is the frequency you want to use and it must be the same with  Gateway and the Node.
- **Router** - The router this gateway will connect to. To reduce latency, pick a router that is in a region which is close to the location of the gateway.
- **Location** - Choose the location of the Gateway by entering its coordinates. This is reflected on the Gateway World Map.
- **Antenna Placement** - Where is your antenna placed? Is it placed indoors or outdoors?

Click Register Gateway and wait for a couple of minutes . If the status of your gateway is **Connected**, Congratulations! Your gateway is now connected to the The Things Network (TTN).

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1591360635\/16406\/ilijxfhv2xo9simhic67.jpg",
        "mode": "responsive",
        "width": 1896,
        "height": 928,
        "caption": "**Figure 6**: RAK2245 Stamp Edition - LPWAN Gateway TTN Connection Success"
    }
}]$

