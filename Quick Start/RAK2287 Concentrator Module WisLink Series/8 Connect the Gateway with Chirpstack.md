---
type: page
title: Connect the Gateway with Chirpstack
listed: true
slug: connecting-to-chirpstack
---published

The ChirpStack or previously known as LoRaServer project provides open-source components for building LoRaWAN® networks. You can learn more about ChirpStack [**here**](https://www.chirpstack.io/)

For the RAKwireless Developer Gateways, there are 2 ways to use the ChirpStack:

### 1. Using the built-in ChirpStack

There is a built-in ChirpStack in every RAK Developer gateway if you use the latest firmware.

- When you use it for the first time after burning the latest firmware, the gateway will work in the EU868 Band and use the built-in ChirpStack as its default LoRa®  Server. If you don't want to change the frequency or LoRa® Server, you don't have to do anything as this will be configured automatically when the gateway boots.
- However if it is not the first time and you want to use the built-in ChirpStack as the LoRa® Server, follow the steps discussed in [auto$](/rak2287-concentrator-module/configuring-the-gateway) section.
- **Optional:** If ever you disabled the AP Mode and you have connected it to your own Wifi network (Client Mode). You can search for your gateway’s IP Address via [**Advanced IP Scanner**](https://www.advanced-ip-scanner.com/). Copy the IP Address of your gateway, it should have a Manufacturer name of **Raspberry Pi Foundation**:

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1576943872\/13868\/mtfxbfnu0pxildkxayzt.png",
        "mode": "responsive",
        "width": 925,
        "height": 610,
        "caption": "**Figure 1**: IP address of your LPWAN Gateway using IP Scanner"
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
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1591359670\/13868\/isrr966quxranshgmexp.png",
        "mode": "responsive",
        "width": 1934,
        "height": 1048,
        "caption": "**Figure 2:** ChirpStack Web-based UI"
    }
}]$

- Everything should be pre-configured: Device profiles have been created, the gateway has been registered with the server, etc. If you go to the Gateways tab and click on rak_gateway, you should see the gateway details page.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1591359705\/13868\/tsogb6j6la0u9kcs8tcc.jpg",
        "mode": "responsive",
        "width": 1920,
        "height": 929,
        "caption": "**Figure 3**: Available Gateways in Chirpstack"
    }
}]$

- Go to the rak_gateway and see the "Last seen" status. It must be a few seconds ago which signifies that the gateway is visible in the ChirpStack server.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1591359736\/13868\/tsrhfn2plhbrwgc6vfvi.jpg",
        "mode": "responsive",
        "width": 1896,
        "height": 930,
        "caption": "**Figure 4:** Last Seen Status"
    }
}]$

### 2. Using a Remote ChirpStack

There are 2 ways that you can get a remote ChirpStack:

1. Use RAK's Cloud TestingChirpStack
2. Setup a remote ChirpStack instance by yourself.

If you want to use RAK’s cloud testing ChirpStack, you can contact the RAKwireless team on the[ forums](https://forum.rakwireless.com/) for support.

Deploying a remote instance by yourself is a little more complicated, however there is plenty on information on how to do so for a number of platforms/OS on the official [ChirpStack webpage](https://www.chirpstack.io/).

