---
type: page
title: Connect the LoRa Gateway with ChirpStack
listed: false
slug: connect-the-lora-gateway-with-chirpstack
---published

The ChirpStack or previously known as LoRaServer project provides open-source components for building LoRaWAN networks. You can learn more about ChirpStack [**here**](https://www.chirpstack.io/).

For RAK2245 LoRa Pi Gateway, there are 2 ways to use the ChirpStack:

### Using the built-in ChirpStack

There is a built-in ChirpStack in every RAK RPi LoRa gateway if you use the latest firmware.

- When you use it for the first time after burning the latest firmware, the LoRa Gateway will work in the EU868 Band and use the built-in ChirpStack as its default LoRa Server. If you don't want to change the frequency or LoRa Server, you don't have to do anything as this will be configured automatically when the LoRa Gateway starts.
- However if it is not the first time and you want to use the built-in ChirpStack as the LoRa Server, just do the steps discussed in [auto$](/rak2245-pi-hat-edition-lorawan-gateway-concentrator-module/configuring-the-gateway) section.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1561019845\/14823\/zjuczsc22wwtlplluuuy.png",
        "mode": "responsive",
        "width": 949,
        "height": 474,
        "caption": "**Figure 1:** Server - plan configuration window"
    }
}]$

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1561019896\/14823\/mghicbccbybgkicybj8r.png",
        "mode": "responsive",
        "width": 934,
        "height": 461,
        "caption": "**Figure 2:** ChirpStack IP Address"
    }
}]$

That's it! If you want to check transferred data on the built-in ChirpStack, just open a browser and enter "IP Address of ChirpStack:8080", then enter the default **username: "admin"** and the default **password : "admin"**

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1561019999\/14823\/y2mhs4ib3rapiza3yeab.png",
        "mode": "responsive",
        "width": 726,
        "height": 472,
        "caption": "**Figure 3:** ChirpStack Home Page"
    }
}]$

### Using an Independent ChirpStack

There are 2 ways that you can get an independent ChirpStack:

1. Use RAK's Cloud Testing ChirpStack.
2. Setup an Independent ChirpStack by yourself.

If you want to use RAK's Cloud Testing ChirpStack, contact RAK's Technical Support in the Forum: [https://forum.rakwireless.com/](https://forum.rakwireless.com/)

If you want to setup an Independent ChirpStack by yourself, download the image [here](https://www.rakwireless.com/en/download/LoRa/LoRa-Server-OS#image) and install it on a computer (this tutorial uses an x86 PC).

$plugin[{
    "type": "callout",
    "data": {
        "text": "This is a whole Ubuntu OS and it will erase all of the old data on your drive. Remember to run the \"sudo gateway-config\" command in the CLI and point the Gateway to the IP address of the machine you just installed ChirpStack on. This can be done in item 2 in the menu \"Setup RAK Gateway LoRa concentrator\"!",
        "type": "warning",
        "title": "Warning"
    }
}]$

- Login to your ChirpStack to register your LoRa Gateway by opening the ChirpStack's web page in a browser by entering "IP Address of ChirpStack:8080".

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1561020204\/14823\/vqegqjq0zgwz8aglvomy.png",
        "mode": "responsive",
        "width": 771,
        "height": 385,
        "caption": "**Figure 4:** ChirpStack Login Page"
    }
}]$

- The default username is "admin" and the password is also "admin"

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1561020293\/14823\/wbutedmgfbik9nfoyf7v.png",
        "mode": "responsive",
        "width": 857,
        "height": 497,
        "caption": "**Figure 5:** ChirpStack Home Page"
    }
}]$

- Click "Gateway"

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1561020446\/14823\/x9gblgjc7sl6qekpfugl.png",
        "mode": "responsive",
        "width": 857,
        "height": 497,
        "caption": "**Figure 6:** ChirpStack Registered Gateways"
    }
}]$

- Click "Create" to register our LoRa Gateway and fill up the necessary information.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1561020580\/14823\/q7c9w7mvr21o6zfp4d6t.png",
        "mode": "responsive",
        "width": 635,
        "height": 432,
        "caption": "**Figure 7:** Registering your own Gateway"
    }
}]$

- Fill in the Gateway ID that we got from the last section ([auto$](/rak2245-pi-hat-edition-lorawan-gateway-concentrator-module/configuring-the-gateway)), also called Geteway EUI.
- If you have properly configured your LoRa Gateway and there is a network connection between the external ChirpStack and your LoRa Gateway, you should see the following page and status:

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1561020698\/14823\/ffbvuxom4zebkgrzgyc3.png",
        "mode": "responsive",
        "width": 634,
        "height": 441,
        "caption": "**Figure 8:** Successfully Registered the Gateway"
    }
}]$

- Congratulations! You have connected your LoRa Gateway to an external ChirpStack Successfully!

