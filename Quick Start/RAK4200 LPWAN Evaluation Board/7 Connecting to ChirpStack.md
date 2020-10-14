---
type: page
title: Connecting to ChirpStack
listed: true
slug: connecting-to-chirpstack
---published

The **ChirpStack** or previously known as LoRaServer project provides open-source components for building LoRaWAN® networks. You can learn more about ChirpStack [**here**](https://www.chirpstack.io/).

$plugin[{
    "type": "callout",
    "data": {
        "text": "In this document, it is  assumed that you are using RAK Gateway and its built-in ChirpStack or RAK\ncloud testing ChirpStack. \n\nIt is also assumed that a Gateway\nwith the ChirpStack has been configured successfully. If not, please have a look at RAK\u2019s documents\nfor more details about RAK LPWAN Gateway and [**RAK cloud testing**](https:\/\/forum.rakwireless.com\/t\/rak-free-cloud-loraserver-for-testing\/344).",
        "type": "info",
        "title": "Note:"
    }
}]$

1. Open the web page of the ChirpStack which you want to connect with and login.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1580616278\/24041\/wgk31ykcgwp2gbzicmut.png",
        "mode": "responsive",
        "width": 1934,
        "height": 1093,
        "caption": "**Figure 1**: Chirpstack Default Window"
    }
}]$

$plugin[{
    "type": "callout",
    "data": {
        "text": "By default, there is\nalready one or more items in this page, you can use it or create a new item.",
        "type": "info",
        "title": "Note:"
    }
}]$

**2.** Create a new item by
click the “**CREATE**” button, and fill up the necessary items.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1580616290\/24041\/l8na6pcdsvjl0lrqznyr.png",
        "mode": "responsive",
        "width": 1934,
        "height": 1094,
        "caption": "**Figure 2**: Chirpstack Creating Application"
    }
}]$

**3.** Once done , click “**CREATE APPLICATION**”.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1580616315\/24041\/zcxqc0pe6vquherzw521.png",
        "mode": "responsive",
        "width": 1934,
        "height": 1093,
        "caption": "**Figure 3**: Chirpstack Applications Available"
    }
}]$

**4.** The list of items are then provided same with the image above. Click the new item created.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1580616329\/24041\/r2ikjxdaluvfxbqhaccc.png",
        "mode": "responsive",
        "width": 1934,
        "height": 1094,
        "caption": "**Figure 4**: Chirpstack Choosing  RAK4200 LPWAN Evaluation Board Application"
    }
}]$

**5.** Add a Node device into ChirpStack by clicking the “**CREATE**” button:

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1580616343\/24041\/sdrlazcgfseimitslo6u.png",
        "mode": "responsive",
        "width": 1934,
        "height": 1094,
        "caption": "**Figure 5**: Chirpstack Adding Node into the  RAK4200 LPWAN Evaluation Board Application"
    }
}]$

**6.** Once the Node is created, fill-in  the necessary data. You can generate a
Device EUI automatically by clicking the following icon, or you can write a correct
Device EUI in the edit box.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1580616355\/24041\/bx0hvot72klwrnznnbig.png",
        "mode": "responsive",
        "width": 1934,
        "height": 1094,
        "caption": "**Figure 6**: Chirpstack Adding Parameters in the Node"
    }
}]$

