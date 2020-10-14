---
type: page
title: Connect the Gateway with Chirpstack
listed: true
slug: connect-the-gateway-with-chirpstack
---published

The ChirpStack or previously known as LoRaServer project provides open-source components for building LoRaWAN® networks. You can learn more about ChirpStack [here](https://www.chirpstack.io/).

### Using an Independent ChirpStack

Since the RAK7246G LPWAN Developer Gateway does not include a built-in Chirpstack, choose in the ways provided below so you can get an independent ChirpStack:

1. Use RAK's Cloud TestingChirpStack - If you want to use RAK's Cloud Testing ChirpStack, contact RAK's Technical Support in the Forum: [RAK Free Cloud Server for Testing](https://forum.rakwireless.com/t/rak-free-cloud-loraserver-for-testing/344)
2. Setup an Independent ChirpStack by yourself.

This is a lot more complicated having to deploy a remote ChirpStack by yourself but Chirpstack provided a detailed guide on how to do it **[here](https://www.chirpstack.io/guides/debian-ubuntu/)[:](https://www.chirpstack.io/gateway-bridge/overview/)**

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1576948724\/13868\/vn6fioh16k6zjdplr0it.png",
        "mode": "responsive",
        "width": 1380,
        "height": 681,
        "caption": "**Figure 1:** Chirpstack Getting Started Guide on Ubuntu"
    }
}]$

$plugin[{
    "type": "callout",
    "data": {
        "text": "Remember to run the \"`sudo gateway-config`\" command in the CLI and point the Gateway to the IP address of the machine you just installed Chirpstack on. This can be done in item 2 in the menu \"**Setup RAK Gateway LoRa\u00ae concentrator**\"!",
        "type": "warning",
        "title": "Warning"
    }
}]$

Assuming you have set it up correctly, Login to your ChirpStack to register your Gateway by opening the ChirpStack's web page in a browser by entering "**IP Address of ChirpStack:8080**". 

If you are using an **Independent Chirpstack**, use the IP Address you have set in the **Configuring the Gateway** document. If you are using the **RAK Free Cloud Server Chirpstack 209.250.251.9**

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1591344328\/24748\/tursjpvg5juf1parh0rv.png",
        "mode": "responsive",
        "width": 1934,
        "height": 1048,
        "caption": "**Figure 2:** ChirpStack Login Page"
    }
}]$

- The default username is "**admin**" and the password is also "**admin**"

$plugin[{
    "type": "callout",
    "data": {
        "text": "If you are using the RAK Cloud Testing ChirpStack, input the account and password you have asked in the forum provided beforehand.",
        "type": "info",
        "title": "Note:"
    }
}]$

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1576944634\/13868\/pxxn6cq9hox9mtjzqxep.png",
        "mode": "responsive",
        "width": 1380,
        "height": 681,
        "caption": "**Figure 3:** ChirpStack Home Page"
    }
}]$

- Click "**Gateways**" in the left menu  and Press "**+ CREATE**" to register your Gateway

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1591629574\/24748\/m58gxcus4e5lp8uqabdb.png",
        "mode": "responsive",
        "width": 1934,
        "height": 943,
        "caption": "**Figure 4:** ChirpStack Registered Gateways"
    }
}]$

- Click "Create" to register your Gateway and fill up the necessary information.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1591628848\/24748\/iifujar241wlupxohaur.png",
        "mode": "responsive",
        "width": 1910,
        "height": 946,
        "caption": "**Figure 5:** Registering your own Gateway"
    }
}]$

- Fill in the Gateway ID which is also called Geteway EUI same in the image shown below:

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1591629145\/24748\/oxsfyxk4hp2d31tv7hgh.png",
        "mode": "responsive",
        "width": 1373,
        "height": 684,
        "caption": "**Figure 6**: RAK7246G LPWAN Developer Gateway Gateway ID in SSH"
    }
}]$

- If you have properly configured your Gateway and there is a network connection between the external ChirpStack and your Gateway, you should see the following page and status:

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1591628460\/24748\/svxgkb2ozspffqofi9qz.png",
        "mode": "responsive",
        "width": 1909,
        "height": 943,
        "caption": "**Figure 7:** Successfully Registered the Gateway"
    }
}]$

- By clicking the Live LORAWAN FRAMES tab, you can check the LoRa® packets sent by the LoRa® nodes into your RAK7246G LPWAN Developer Gateway

Congratulations! You have connected your Gateway to an external ChirpStack Successfully!

