---
type: page
title: Connecting to ChirpStack
listed: true
slug: connecting-to-chirpstack
---published

The ChirpStack or previously known as LoRaServer project provides open-source components for building LoRaWAN® networks. You can learn more about ChirpStack [**here**](https://www.chirpstack.io/).

You can use RAK811 LPWAN Breakout Module to connect with ChirpStack according to the following steps:

$plugin[{
    "type": "callout",
    "data": {
        "text": "This section assumed that you had already connected your gateway with TTN correctly. If not, please take a look at our [RAK Document Center](https:\/\/doc.rakwireless.com\/) to view the different Gateway documentations.",
        "type": "info",
        "title": "Note:"
    }
}]$

**1.** Open the web page of the ChirpStack which you want to connect with and login.

**2.** By default, there is already one or more items in this page, you can use it or create a new item. Now, let’s create a new item by clicking the “**CREATE**” button.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1582540007\/17094\/xlubsj8qfhs9o1wqg3ao.png",
        "mode": "responsive",
        "width": 1934,
        "height": 1093,
        "caption": "**Figure 1:** ChirpStack Applications"
    }
}]$

**3.** Fill up the necessary information then Click "**CREATE APPLICATION**”.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1582540020\/17094\/jjfxkdc14hrwxavqnejk.png",
        "mode": "responsive",
        "width": 1934,
        "height": 1094,
        "caption": "**Figure 2:** Creating the Application"
    }
}]$

**4.** Click the new item name “**RAK811**”:

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1582540032\/17094\/huqfi7q0iuvj3peoerje.png",
        "mode": "responsive",
        "width": 1934,
        "height": 1093,
        "caption": "**Figure 3:** Applications page in ChirpStack"
    }
}]$

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1582540042\/17094\/zvda6jcwtxr1ci2fvdqc.png",
        "mode": "responsive",
        "width": 1934,
        "height": 1094,
        "caption": "**Figure 4:** RAK811 Application"
    }
}]$

**5** .**Add** a Node device into ChirpStack by clicking the “**CREATE**” button:

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1582540054\/17094\/o86hkpxcz88w3gtgq3rr.png",
        "mode": "responsive",
        "width": 1934,
        "height": 1094,
        "caption": "**Figure 5:** Adding a Node Device"
    }
}]$

**6.** Fill them in. You can generate a **Device EUI** automatically by clicking the Device EUI icon, or you can write the correct Device EUI in the edit box.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1582540063\/17094\/kdmfb9lhoygt8lxczsew.png",
        "mode": "responsive",
        "width": 1909,
        "height": 1094,
        "caption": "**Figure 6:** Filling the Device Parameters"
    }
}]$

$plugin[{
    "type": "callout",
    "data": {
        "text": "If you want to join in OTAA mode, select \u201c**DeviceProfile_OTAA**\u201d in the \u201cDevice-profile\u201d item. If you want to join in ABP mode and CN470 frequency, then, select \u201c**DeviceProfile_ABP_CN470**\u201d in the \u201cDevice-Profile\u201d item. If you want to join in ABP mode and other frequencies except AS923 and CN470, you should select \u201c**DeviceProfile_ABP**\u201d in the \u201cDevice-profile\u201d item.",
        "type": "info",
        "title": "Note:"
    }
}]$

