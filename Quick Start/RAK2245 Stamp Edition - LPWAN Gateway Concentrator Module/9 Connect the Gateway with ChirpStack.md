---
type: page
title: Connect the Gateway with ChirpStack
listed: true
slug: connect-the-lora-gateway-with-chirpstack
---published

The ChirpStack or previously known as LoRaServer project provides open-source components for building LoRaWAN® networks. You can learn more about ChirpStack [**here**](https://www.chirpstack.io/)

For the RAK2245 Stamp Edition - LPWAN Gateway Concentrator Module, there are 2 ways to use the ChirpStack:

### 1. Using the built-in ChirpStack

There is a built-in ChirpStack in every RAK Developer gateway if you use the latest firmware.

- When you use it for the first time after burning the latest firmware, the gateway will work in the EU868 Band and use the built-in ChirpStack as its default LoRa®  Server. If you don't want to change the frequency or LoRa® Server, you don't have to do anything as this will be configured automatically when the gateway boots.
- However if it is not the first time and you want to use the built-in ChirpStack as the LoRa® Server, follow the steps discussed in [Configuring the Gateway](https://doc.rakwireless.com/rak2245-stamp-edition---lorawan----gateway-concentrator-module/configuring-the-gateway) section.
- **Optional:** If ever you disabled the AP Mode and you have connected it to your own Wifi network (Client Mode). You can search for your gateway’s IP Address via [**Advanced IP Scanner**](https://www.advanced-ip-scanner.com/). Copy the IP Address of your Gateway, it should have a Manufacturer name of **Raspberry Pi Foundation**:

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1576943872\/13868\/mtfxbfnu0pxildkxayzt.png",
        "mode": "responsive",
        "width": 925,
        "height": 610,
        "caption": "**Figure 1**: IP address of your RAK2245 Stamp Edition - LPWAN Gateway using IP Scanner"
    }
}]$

There is a Web-based UI that comes with the ChirpStack instance. Simply open a browser and enter the following credentials:

- **Browser Address**: "Gateway IP Address:8080" (**Example**: https:/192.168.254.176:8080)
- **Username**: admin
- **Password**: admin

$plugin[{
    "type": "callout",
    "data": {
        "text": "It is advisable to change your password to tighten the security of your account. You can change this by clicking the \"change password\" button at the user icon.",
        "type": "warning",
        "title": "Warning"
    }
}]$

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1591360656\/16411\/cuuf9tg7c4v2s2bkljbu.png",
        "mode": "responsive",
        "width": 1934,
        "height": 1048,
        "caption": "**Figure 2:** ChirpStack Web-based UI"
    }
}]$

- Everything should be pre-configured: Device profiles have been created, the Gateway has been registered with the server, etc. If you go to the Gateways tab and click on rak_gateway, you should see the Gateway details page.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1591360664\/16411\/rafhzxinen5lm6bh34yu.jpg",
        "mode": "responsive",
        "width": 1920,
        "height": 929,
        "caption": "**Figure 3**: Available Gateways in Chirpstack"
    }
}]$

- Go to the rak_gateway and see the "Last seen" status. It must be a few seconds ago which signifies that the Gateway is visible in the ChirpStack server.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1591360676\/16411\/srwvv10mg0wjlnc51ndh.jpg",
        "mode": "responsive",
        "width": 1896,
        "height": 930,
        "caption": "**Figure 4:** Last Seen Status"
    }
}]$

### 2. Using an Independent ChirpStack

There are 2 ways that you can get an independent ChirpStack:

1. Use RAK's Cloud TestingChirpStack - If you want to use RAK's Cloud Testing ChirpStack, contact RAK's Technical Support in the Forum: [https://forum.rakwireless.com/](https://forum.rakwireless.com/)
2. Setup an Independent ChirpStack by yourself.

This is a lot more complicated having to deploy a remote ChirpStack by yourself but Chirpstack provided a detailed guide on how to do it **[here](https://www.chirpstack.io/guides/debian-ubuntu/)[:](https://www.chirpstack.io/gateway-bridge/overview/)**

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1576948724\/13868\/vn6fioh16k6zjdplr0it.png",
        "mode": "responsive",
        "width": 1380,
        "height": 681,
        "caption": "**Figure 5:** Chirpstack Getting Started Guide on Ubuntu"
    }
}]$

$plugin[{
    "type": "callout",
    "data": {
        "text": "Remember to run the \"`sudo gateway-config`\" command in the CLI and point the Gateway to the IP address of the machine you just installed Chirpstack on. This can be done in item 2 in the menu \"**Setup RAK Gateway LoRa**\u00ae **concentrator**\"!",
        "type": "warning",
        "title": "Warning"
    }
}]$

- Assuming you have set it up correctly, Login to your ChirpStack to register your gateway by opening the ChirpStack's web page in a browser by entering "IP Address of ChirpStack:8080".

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1576944618\/13868\/rmibul5ouzluictf9zpq.png",
        "mode": "responsive",
        "width": 1380,
        "height": 681,
        "caption": "**Figure 6:** ChirpStack Login Page"
    }
}]$

- The default username is "**admin**" and the password is also "**admin**".

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1576944634\/13868\/pxxn6cq9hox9mtjzqxep.png",
        "mode": "responsive",
        "width": 1380,
        "height": 681,
        "caption": "**Figure 7:** ChirpStack Home Page"
    }
}]$

- Click "Gateways" and Press "**+ CREATE**" to register your Gateway.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1576944656\/13868\/tqyaaom3kzxbgj51eapl.png",
        "mode": "responsive",
        "width": 1380,
        "height": 681,
        "caption": "**Figure 8:** ChirpStack Registered Gateways"
    }
}]$

- Click "**Create**" to register your gateway and fill up the necessary information.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1591599582\/16411\/jqtc7k6ydggkl7ytpbts.png",
        "mode": "responsive",
        "width": 1910,
        "height": 942,
        "caption": "**Figure 9:** Registering your own Gateway"
    }
}]$

- Fill in the Gateway ID that we got from the last section ([Configuring the Gateway](https://doc.rakwireless.com/rak2245-stamp-edition---lorawan----gateway-concentrator-module/configuring-the-gateway)), also called Gateway EUI.
- If you have properly configured your gateway and there is a network connection between the external ChirpStack and your gateway, you should see the following page and status:

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1591599639\/16411\/lcmuegbyqqlakbk7u5uq.png",
        "mode": "responsive",
        "width": 1910,
        "height": 942,
        "caption": "**Figure 10:** Successfully Registered the Gateway"
    }
}]$

- Congratulations! You have connected your gateway to an external ChirpStack Successfully!

