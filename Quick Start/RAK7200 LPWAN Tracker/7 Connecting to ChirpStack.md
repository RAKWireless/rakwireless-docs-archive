---
type: page
title: Connecting to ChirpStack
listed: true
slug: connect-to-chirpstack
---published

The ChirpStack or previously known as LoRaServer project provides open-source components for building LoRaWAN® networks. You can learn more about ChirpStack [**here**](https://www.chirpstack.io/).

You can use RAK7200 LPWAN Tracker to connect with ChirpStack by following this steps:

$plugin[{
    "type": "callout",
    "data": {
        "text": "In this section, it is an assumed that you have already connected your gateway with TTN correctly. If not, please have a look at the document of RAK Gateway.",
        "type": "info",
        "title": "Note"
    }
}]$

OK! Let’s get started!

1.Open the web page of the ChirpStack which you want to connect with and login. 

2.By default, there is already one or more item in this page, you can use it or create a new item. Now, let’s create a new item by clicking the “**CREATE**” button.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1580631719\/17852\/mhxpxv152iy2zc2h7jyv.png",
        "mode": "responsive",
        "width": 1934,
        "height": 1093,
        "caption": "**Figure 1**: ChirpStack Applications"
    }
}]$

3.Fill up the necessary information then Click "**CREATE APPLICATION**"

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1580631730\/17852\/aehocrv1kdgmfw5i9ncm.png",
        "mode": "responsive",
        "width": 1934,
        "height": 1094,
        "caption": "**Figure 2**: Creating the Application"
    }
}]$

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1580631745\/17852\/shwsznjugdm6epmh5r2o.png",
        "mode": "responsive",
        "width": 1934,
        "height": 1093,
        "caption": "**Figure 3**: Applications page in ChirpStack"
    }
}]$

4.Click the new Item name "RAKwireless_Test_Application"

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1580631796\/17852\/eh9bkvu5uwlrn10jojvr.png",
        "mode": "responsive",
        "width": 1934,
        "height": 1094,
        "caption": "**Figure 4**: RAK7200 Application"
    }
}]$

5.**Add** a Node device into ChirpStack by clicking the “**CREATE**” button:

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1580631808\/17852\/znvzmk7sz4vrhgqmfx4x.png",
        "mode": "responsive",
        "width": 1934,
        "height": 1094,
        "caption": "**Figure 5**: Adding a Node Device"
    }
}]$

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1580631822\/17852\/mphgt1imzsn2pf67bhnq.png",
        "mode": "responsive",
        "width": 1909,
        "height": 1094,
        "caption": "**Figure 6**: Filling the Device Parameters"
    }
}]$

6.Fill them in. You can generate a **Device EUI** automatically by clicking the Device EUI icon, or you can write the correct Device EUI in the edit box.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1580632042\/17852\/doqbh3y9oiyjxu6ixjwn.png",
        "mode": "responsive",
        "width": 1934,
        "height": 1094,
        "caption": "**Figure 7**: Generating Device EUI Automatically"
    }
}]$

$plugin[{
    "type": "callout",
    "data": {
        "text": "If you want to join in OTAA mode, select \u201c**DeviceProfile_OTAA**\u201d in the \u201cDevice-profile\u201d item. If you want to join in ABP mode and CN470 frequency, then, select \u201c**DeviceProfile_ABP_CN470**\u201d in the \u201cDevice-Profile\u201d item. If you want to join in ABP mode and other frequencies except AS923 and CN470, you should select \u201c**DeviceProfile_ABP**\u201d in the \u201cDevice-profile\u201d item.",
        "type": "info",
        "title": "Note"
    }
}]$

