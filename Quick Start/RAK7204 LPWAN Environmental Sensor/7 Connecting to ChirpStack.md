---
type: page
title: Connecting to ChirpStack
listed: true
slug: connecting-to-chirpstack
---published

The ChirpStack or previously known as LoRaServer project provides open-source components for building LoRaWAN® networks. You can learn more about ChirpStack [**here**](https://www.chirpstack.io/).

You can use RAK7204 LPWAN Environmental Sensor to connect with ChirpStack according to the following steps:

$plugin[{
    "type": "callout",
    "data": {
        "text": "In this document, it is assumed that you are using RAK Gateway and its built-in ChirpStack or RAK cloud testing ChirpStack.\n\nIt is also assumed that a Gateway with the ChirpStack has been configured successfully. If not, please have a look at RAK\u2019s documents for more details about RAK LPWAN Gateway and [**RAK cloud testing**](https:\/\/forum.rakwireless.com\/t\/rak-free-cloud-loraserver-for-testing\/344).",
        "type": "info",
        "title": "Note:"
    }
}]$

**1.** Open the web page of the ChirpStack which you want to connect with and login.

**2.** By default, there is already one or more items in this page, you can use it or create a new item. Now, let’s create a new item by clicking the “**CREATE**” button, then filling them in.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1582559496\/18995\/n8zf82nwrfdiagwbsulm.png",
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
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1582559503\/18995\/phryjvt9x6l3vcrqpi8x.png",
        "mode": "responsive",
        "width": 1934,
        "height": 1094,
        "caption": "**Figure 2:** Creating the Application"
    }
}]$

**4.** Click the new item name “**RAKwireless_Test_Application**”:

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1582559699\/18995\/bns2vokqwwbw9hfrm2nh.png",
        "mode": "responsive",
        "width": 1934,
        "height": 1093,
        "caption": "**Figure 3:** Applications page in ChirpStack"
    }
}]$

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1582559711\/18995\/b7ewcpfbgexv5qrflppx.png",
        "mode": "responsive",
        "width": 1934,
        "height": 1094,
        "caption": "**Figure 4:** RAKwireless Test Application"
    }
}]$

**5. Add** a Node device into ChirpStack by clicking the “**CREATE**” button:

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1582559727\/18995\/c6qdrxzhdr1npyclwhom.png",
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
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1582559739\/18995\/aqesyqoiauvcbnqhiytt.png",
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

