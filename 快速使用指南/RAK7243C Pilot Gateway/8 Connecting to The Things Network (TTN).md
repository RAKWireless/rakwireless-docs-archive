---
type: page
title: Connecting to The Things Network (TTN)
listed: true
slug: connecting-to-the-things-network--ttn-
---published

The Things Network is about enabling low power devices to use long range [g](https://www.thethingsnetwork.org/docs/gateways/)ateways to connect to an open-source, decentralized network to exchange data with Application. Learn more about the Things Network [here](https://www.thethingsnetwork.org/docs/).

- First, you should have connected your LoRa Gateway to the router in order to access the internet according to the method which has been introduced in the “Configure your LoRa Gateway” section of this document.
- Second, config your LoRa Gateway and choose TTN as the LoRa Server and choose a correct frequency according to the method which has been introduced in the Configuring the Gateway section.
- Now go to the TTN Website: [https://www.thethingsnetwork.org/](https://www.thethingsnetwork.org/) and Login. You will then see the following page:

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1560836057\/13904\/wjdwcqng7os883rpwpzu.png",
        "mode": "responsive",
        "width": 1350,
        "height": 634,
        "caption": "**Figure 1:** The Things Network Home Page"
    }
}]$

- Choose Console then Click Gateway.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1560836082\/13904\/jrybbsojhlo0xhays1bh.png",
        "mode": "responsive",
        "width": 1350,
        "height": 634,
        "caption": "**Figure 2:** The Things Network Console Page"
    }
}]$

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1560836100\/13904\/cicfhavekd9uxgixocfh.png",
        "mode": "responsive",
        "width": 1350,
        "height": 634,
        "caption": "**Figure 3:** Adding a Gateway to TTN"
    }
}]$

- All of your Registered Gateways will be displayed in this page. Click "register gateway"

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1561493928\/13904\/vujqq2tu83iheduk5lok.jpg",
        "mode": "responsive",
        "width": 1350,
        "height": 634,
        "caption": "**Figure 4:** Registering your Gateway"
    }
}]$

- **Gateway EUI** - this is your Gateway ID that you obtained in the previous step. If you forgot, just type "gateway-version" in the command line. This must be the same with the LoRa Gateway's True Gateway ID otherwise you will fail to register your LoRa Gateway on TTN. **Make sure to select the "I'm using the legacy packet forwarder" check box.**
- **Description** - A human readable description of your LoRa Gateway.
- **Frequency Plan** - This is the frequency you want to use and it must be the same with LoRa Gateway and the LoRa Node.
- **Router** - The router this gateway will connect to. To reduce latency, pick a router that is in a region which is close to the location of the gateway.
- **Location** - Choose the location of the Gateway by entering its coordinates. This is reflected on the Gateway World Map!
- **Antenna Placement** - Where is your antenna placed? Is it placed indoors or outdoors?

Click Register Gateway and wait for a couple of minutes . If the status of your gateway is **Connected**, Congratulations! Your LoRa Gateway is now connected to the The Things Network (TTN).

