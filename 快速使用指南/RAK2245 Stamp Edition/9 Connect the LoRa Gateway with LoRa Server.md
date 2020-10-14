---
type: page
title: Connect the LoRa Gateway with LoRa Server
listed: true
slug: connect-the-lora-gateway-with-lora-server
---published

The LoRa Server project provides an open-source components for building LoRaWAN networks. You can learn more about LoRa Server here : [https://www.loraserver.io/](https://www.loraserver.io/)

For RAK2245 LoRa Pi Gateway, there are 2 ways to use the LoRaServer:

### Using the built-in LoRa Server

There is a built-in LoRaServer in every RAK RPi LoRa gateway if you use the latest firmware.

- When you use it for the first time after burning the latest firmware, the LoRa Gateway will work in EU868 Frequency and use the built-in LoRaServer as its default LoRa Server. If you don't want to change the frequency or LoRa Server, you don't have to do any configurations as this will be configured automatically when the LoRa Gateway starts.
- However if it is not the first time and you want to use the built-in LoRaServer as the LoRa Server, just do the steps discussed in [Configuring the Gateway](https://doc.rakwireless.com/rak2245-stamp-edition/configuring-the-gateway) section.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1561095975\/16411\/pu5xkc9ccryhakeaf1kl.jpg",
        "mode": "responsive",
        "width": 949,
        "height": 474,
        "caption": "Figure 1: Server - plan configuration window"
    }
}]$

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1561095993\/16411\/grkkclahal29uxttlpxa.jpg",
        "mode": "responsive",
        "width": 949,
        "height": 474,
        "caption": "Figure 2: LoRaServer IP Address"
    }
}]$

That's it! If you want to check data on the built-in LoRaServer, just open a browser and enter "IP Address:8080", then enter the default **username: "admin"** and the default **password : "admin"**

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1561096097\/16411\/yhyqi9rjxjjdbwyjsv22.jpg",
        "mode": "responsive",
        "width": 726,
        "height": 472,
        "caption": "Figure 3: LoRaServer Home Page"
    }
}]$

### Using an Independent LoRa Server

There are 2 ways that you can get an independent LoRaServer:

1. Use RAK's Cloud Testing LoRa Server
2. Setup an Independent LoRa Server by yourself

If you want to use RAK's Cloud Testing LoRaServer, contact RAK's Technical Support in the Forum: [https://forum.rakwireless.com/](https://forum.rakwireless.com/)

If you want to setup an Independent LoRaServer by yourself, download the image [here](https://www.rakwireless.com/en/download/LoRa/LoRa-Server-OS#image) and install it on a x86 PC

$plugin[{
    "type": "callout",
    "data": {
        "text": "This is a whole Ubuntu OS and it will erase all of the old data on this your disk of this PC.",
        "type": "info",
        "title": "Warning"
    }
}]$

- Login to your LoRaServer to register your LoRa Gateway, open the LoRaServer's web page on a browser by entering "IP Address:8080".

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1561096339\/16411\/hs2kamebcrjas3rv16ts.jpg",
        "mode": "responsive",
        "width": 771,
        "height": 385,
        "caption": "Figure 4: LoRaServer Login Page"
    }
}]$

- The default username is "admin" and the password is also "admin"

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1561096378\/16411\/chuj15uuoertzvi7uupp.jpg",
        "mode": "responsive",
        "width": 857,
        "height": 497,
        "caption": "Figure 5: LoRaServer Home Page"
    }
}]$

- Click "Gateway"

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1561096410\/16411\/pwgg5ivnrzc9vwuiylh4.jpg",
        "mode": "responsive",
        "width": 857,
        "height": 497,
        "caption": "Figure 6: LoRaServer Registered Gateways"
    }
}]$

- Click "Create" to register our LoRa Gateway and fill up the necessary information.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1561097586\/16411\/dgpuh7qvfzmxw5e6xjda.jpg",
        "mode": "responsive",
        "width": 635,
        "height": 432,
        "caption": "Figure 7: Registering your own Gateway"
    }
}]$

- Fill up the Gateway ID that we got from the last section ([Configuring the Gateway](https://doc.rakwireless.com/rak2245-stamp-edition/configuring-the-gateway))
- If you have done the correct configuration on your LoRa Gateway and the network between the independent LoRaServer and your LoRa Gateway works well, you should see the following page and status:

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1561097694\/16411\/r4mudepqajnjrrcoepj2.jpg",
        "mode": "responsive",
        "width": 634,
        "height": 441,
        "caption": "Figure 8: Successfully Registered the Gateway"
    }
}]$

- Great! You have connected your LoRa Gateway to an independent LoRaServer Successfully!

