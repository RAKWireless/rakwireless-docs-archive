---
type: page
title: Configuration of Gateway-A
listed: true
slug: configuration-of-gateway-a
---published

In this section, we will go through the configuration setup for Gateway-A.

## Packet Forwarder Setup

- Go to the LoRa®  Gateway tab -> LoRa® Packet Forwarder -> General Setup. In the drop down menu for Protocol select: **Built-in LoRa® Server**

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1580549485\/22611\/ml3wdtuydns6btvjuj4e.jpg",
        "mode": "responsive",
        "width": 810,
        "height": 418,
        "caption": "**Figure 1**: Gateway Protocol Mode (Built-in LoRa\u00ae Server)"
    }
}]$

You can leave the rest of the settings with their default values. Remember to **Save & Apply**.

## LoRa® Server General Configuration Setup

- Go to the **LoRa® Network Server tab  > >  General**. Make sure the **Enable switch** is **on**.
- Select your region (LoRa® Band), we are going to use EU863-870 in this example.
- The rest of the settings you can use with their default values. You can change them is you like, however this is dependent on your particular case. You can look up what each setting is referring to in the [auto$](/rak7249-macro-outdoor-gateway/lora-network-server) document. 

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1580551321\/22611\/yreltwbhzucsbpwx933r.jpg",
        "mode": "responsive",
        "width": 812,
        "height": 415,
        "caption": "**Figure 2**: LoRa\u00ae Server Enabling and General Configuration"
    }
}]$

## Registering the Gateway with the Built-in LoRa® Server

- Go to the LoRa® Network Server tab -> Gateway. Enter the Gateway EUI in the field as in the figure below:

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1580551547\/22611\/ndfsfhmj6q9xs62igjny.jpg",
        "mode": "responsive",
        "width": 818,
        "height": 426,
        "caption": "**Figure 3**: Adding a Gateway into LoRa\u00ae Server"
    }
}]$

$plugin[{
    "type": "callout",
    "data": {
        "text": "The Latitude, Longitude and Altitude parameters are not mandatory. You can leave them for later, or leave them empty if the gateway is not stationary.",
        "type": "info",
        "title": "Note:"
    }
}]$

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1580551595\/22611\/l45ao64sskdfpkxnawoe.jpg",
        "mode": "responsive",
        "width": 809,
        "height": 420,
        "caption": "**Figure 4**: Gateway Description parameters"
    }
}]$

- If everything is set up correctly, you will see an image similar tothe figure below:

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1580552500\/22611\/mzwldlotlmjlsqzyhmgw.jpg",
        "mode": "responsive",
        "width": 804,
        "height": 420,
        "caption": "**Figure 5**: Gateway Description parameters"
    }
}]$

