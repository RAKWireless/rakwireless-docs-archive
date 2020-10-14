---
type: page
title: Connect the LoRa Gateway with LoRaServer
listed: true
slug: connect-the-lora-gateway-with-loraserver
---published

The LoRa Server project provides open-source components for building LoRaWAN networks. You can learn more about LoRaServer here : [https://www.loraserver.io/](https://www.loraserver.io/)

For RAK7243C Pilot Gateway, there are 2 ways to use the LoRaServer:

### Using the built-in LoRaServer

There is a built-in LoRaServer in every RAK RPi LoRa gateway if you use the latest firmware.

- When you use it for the first time after burning the latest firmware, the LoRa Gateway will work in the  EU868 Band and use the built-in LoRaServer as its default LoRa Server. If you don't want to change the frequency or LoRa Server, you don't have to do anything as this will be configured automatically when the LoRa Gateway starts.
- However if it is not the first time and you want to use the built-in LoRaServer as the LoRa Server, just do the steps discussed in [auto$](/rak2245-pi-hat/configuring-the-gateway) section.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1560838422\/-1\/frynfaetjadrs5lwukvs.png",
        "mode": "responsive",
        "width": 949,
        "height": 474,
        "caption": "**Figure 1:** Server - plan configuration window"
    }
}]$

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1560838438\/-1\/pialrh081yvnj5w88pxh.png",
        "mode": "responsive",
        "width": 934,
        "height": 461,
        "caption": "**Figure 2:** LoRaServer IP Address"
    }
}]$

That's it! If you want to check  transferred data on the built-in LoRaServer, just open a browser and enter "IP Address of LoRaServer:8080", then enter the default **username: "admin"** and the default **password : "admin"**

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1560838460\/-1\/zihuuaozsjmf3c4gzmbd.png",
        "mode": "600",
        "width": 857,
        "height": 497,
        "caption": "**Figure 3:** LoRaServer Home Page"
    }
}]$

### Using an Independent LoRa Server

There are 2 ways that you can get an independent LoRaServer:

1. Use RAK's Cloud Testing LoRaServer.
2. Setup an Independent LoRaServer by yourself.

If you want to use RAK's Cloud Testing LoRaServer, contact RAK's Technical Support in the Forum: [https://forum.rakwireless.com/](https://forum.rakwireless.com/)

If you want to setup an Independent LoRaServer by yourself, download the image [here](https://www.rakwireless.com/en/download/LoRa/LoRa-Server-OS#image) and install it on a computer (this tutorial uses an x86 PC).

$plugin[{
    "type": "callout",
    "data": {
        "text": "This is a whole Ubuntu OS and it will erase all of the old data on your drive. Remember to run the \"sudo gateway-config\" command in the CLI and point the Gateway to the IP address of the machine you just installed LoRaServer on. This can be done in item 2 in the menu \"Setup RAK Gateway LoRa concentrator\"!",
        "type": "warning",
        "title": "Warning"
    }
}]$

- Login to your LoRaServer to register your LoRa Gateway by opening the LoRaServer's web page in a browser by entering "IP Address of LoRaServer:8080".

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1560838559\/13907\/dbj9ideuxbsgzztrf3sl.png",
        "mode": "responsive",
        "width": 771,
        "height": 385,
        "caption": "**Figure 4:** LoRaServer Login Page"
    }
}]$

- The default username is "admin" and the password is also "admin"

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1560838577\/13907\/iwsmrt7jlrbdahknymnh.png",
        "mode": "responsive",
        "width": 857,
        "height": 497,
        "caption": "**Figure 5:** LoRaServer Home Page"
    }
}]$

- Click "Gateway"

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1560838653\/13907\/wljechyh7enzt2fbicef.png",
        "mode": "responsive",
        "width": 857,
        "height": 497,
        "caption": "**Figure 6:** LoRaServer Registered Gateways"
    }
}]$

- Click "Create" to register our LoRa Gateway and fill up the necessary information.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1560838703\/13907\/sqbjk56wzrd0upvcnsor.png",
        "mode": "responsive",
        "width": 635,
        "height": 432,
        "caption": "**Figure 7:** Registering your own Gateway"
    }
}]$

- Fill in the Gateway ID that we got from the last section ([auto$](/rak2245-pi-hat/configuring-the-gateway)), also called Geteway EUI.
- If you have properly configured your LoRa Gateway and there is a network connection between the external LoRaServer and your LoRa Gateway, you should see the following page and status:

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1560838747\/13907\/hzfjaxqewzyhzkafce07.png",
        "mode": "responsive",
        "width": 634,
        "height": 441,
        "caption": "**Figure 8:** Successfully Registered the Gateway"
    }
}]$

- Congratulations! You have connected your LoRa Gateway to an external LoRaServer Successfully!

