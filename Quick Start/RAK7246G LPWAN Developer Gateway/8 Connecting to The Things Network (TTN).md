---
type: page
title: Connecting to The Things Network (TTN)
listed: true
slug: connecting-to-the-things-network
---published

The Things Network is about enabling low power devices to use long range [g](https://www.thethingsnetwork.org/docs/gateways/)ateways to connect to an open-source, decentralized network to exchange data with Application. Learn more about the Things Network [here](https://www.thethingsnetwork.org/docs/).

- First, you should have connected your Gateway to the router in order to access the internet according to the method which has been introduced in the [auto$](/rak7246g-lorawan-developer-gateway/accessing-the-internet) section of this document.
- Second, config your Gateway and choose TTN as the LoRa® Server and choose a correct frequency according to the method which has been introduced in the [Configuring the Gateway](/quick-start/rak7246g-lorawan-developer-gateway/configuring-the-gateway#server-is-ttn) section.
- Now go to the TTN Website: [https://www.thethingsnetwork.org/](https://www.thethingsnetwork.org/) and Login. You will then see the following page:

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1591343667\/24747\/f4vtum982q4k5emmjclm.png",
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
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1591343722\/24747\/z8urqqc6kixxyg8tjiyh.png",
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
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1591343734\/24747\/bjqjnokwr2til8tnglut.png",
        "mode": "responsive",
        "width": 1934,
        "height": 943,
        "caption": "**Figure 3:** Adding a Gateway to TTN"
    }
}]$

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1591344289\/24747\/soldxflr57mgxu7pv1sc.png",
        "mode": "responsive",
        "width": 1915,
        "height": 945,
        "caption": "**Figure 4:** Registering your Gateway"
    }
}]$

- **Gateway EUI** - refers to the Gatway ID you obtained from the previous steps. In case you forgot, just type "**gateway-version**" in the command line. This must be the same with the Gateway's True Gateway ID otherwise you will fail to register your Gateway on TTN.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1584346056\/24747\/w0jvwm45rcfwsyktmnqm.png",
        "mode": "responsive",
        "width": 1373,
        "height": 684,
        "caption": "**Figure 5**: RAK7246G LPWAN Developer Gateway -  Gateway ID in SSH"
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

- **Description** - A human readable description of your Gateway.
- **Frequency Plan** - This is the frequency you want to use and it must be the same with Gateway and your Node.
- **Router** - The router this gateway will connect to. To reduce latency, pick a router that is in a region which is close to the location of the gateway.
- **Location** - Choose the location of the Gateway by entering its coordinates. This is reflected on the Gateway World Map.
- **Antenna Placement** - Where is your antenna placed? Is it placed indoors or outdoors?

Click Register Gateway and wait for a couple of minutes . If the status of your gateway is **Connected**, Congratulations! Your Gateway is now connected to the The Things Network (TTN).

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1591344275\/24747\/pewakglzlh8yru0uqzsz.png",
        "mode": "responsive",
        "width": 1912,
        "height": 943,
        "caption": "**Figure 6**:RAK7246G LPWAN Developer Gateway TTN Connection Success"
    }
}]$

