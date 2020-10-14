---
type: page
title: OTAA Mode
listed: true
slug: ttn-otaa-mode
---published

When setting up a new device in TTN, its default mode is **OTAA** or **Over-the-Air Activation**. For configuring it you need the following three parameters: **Device EUI, Application EUI** and **App Key**. You can get them all from the **Overview page**.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1582558465\/17326\/s5ezrnlxr9qbwfbtssne.png",
        "mode": "responsive",
        "width": 1934,
        "height": 1094,
        "caption": "**Figure 1:** Device OTAA Parameters"
    }
}]$

Now, let us configure the RAK5205 to work in OTAA mode in the EU868 band, as an example.

$plugin[{
    "type": "callout",
    "data": {
        "text": "The default LoRa\u00ae working mode for the RAK5205 is LoRaWAN\u00ae 1.0.2, while the default LoRa\u00ae join mode is OTAA, and the default LoRa\u00ae class is Class A.",
        "type": "info",
        "title": "Info"
    }
}]$

1. Set mode to OTAA, device class to Class A and your LoRaWAN® region to your correct frequency band, with the following set of commands below. Remember to replace XXX with the your LoRaWAN® region, see this **[link](https://www.thethingsnetwork.org/docs/lorawan/frequencies-by-country.html) **for your frequency plan.

$plugin[{
    "type": "code-block",
    "data": {
        "languageBlocks": [
            {
                "code": "at+set_config=lora:join_mode:0",
                "language": "none"
            }
        ]
    }
}]$

$plugin[{
    "type": "code-block",
    "data": {
        "languageBlocks": [
            {
                "code": "at+set_config=lora:class:0",
                "language": "none"
            }
        ]
    }
}]$

$plugin[{
    "type": "code-block",
    "data": {
        "languageBlocks": [
            {
                "code": "at+set_config=lora:region:XXX",
                "language": "none"
            }
        ]
    }
}]$

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1579449073\/17642\/okwyucipaed3fnrarkso.png",
        "mode": "responsive",
        "width": 1375,
        "height": 898,
        "caption": "**Figure 2:** Setting up the RAK5205 operation mode"
    }
}]$

**2**. Now that the modes are set, enter the parameters: : **Device EUI, Application EUI** and **App Key**. Use the commands below. Remember to replace the **"XXXX"** with the corresponding parameter value for your particular case:

$plugin[{
    "type": "code-block",
    "data": {
        "languageBlocks": [
            {
                "code": "at+set_config=lora:dev_eui:XXXX",
                "language": "none"
            }
        ]
    }
}]$

$plugin[{
    "type": "code-block",
    "data": {
        "languageBlocks": [
            {
                "code": "at+set_config=lora:app_eui:XXXX",
                "language": "none"
            }
        ]
    }
}]$

$plugin[{
    "type": "code-block",
    "data": {
        "languageBlocks": [
            {
                "code": "at+set_config=lora:app_key:XXXX",
                "language": "none"
            }
        ]
    }
}]$

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1579449211\/17642\/jttmbmkhm0ac0duvap94.png",
        "mode": "responsive",
        "width": 1375,
        "height": 901,
        "caption": "**Figure 3:** Setting up the RAK5205 OTAA parameters"
    }
}]$

You should end up with a window as the one in **Figure 3** above  with **a series of OK messages**.

**3**. Finally, execute the join command:

$plugin[{
    "type": "code-block",
    "data": {
        "languageBlocks": [
            {
                "code": "at+join",
                "language": "none"
            }
        ]
    }
}]$

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1579449302\/17642\/eevf8jgjt1p48i17vugw.png",
        "mode": "responsive",
        "width": 1375,
        "height": 898,
        "caption": "**Figure 4:** Join command"
    }
}]$

**4.** You can test the connection by sending an uplink frame. Use the following as an example:

$plugin[{
    "type": "code-block",
    "data": {
        "languageBlocks": [
            {
                "code": "at+send=lora:1:12345678",
                "language": "none"
            }
        ]
    }
}]$

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1579449436\/17642\/tsyls5mfkzctes7lh1jg.png",
        "mode": "responsive",
        "width": 1374,
        "height": 899,
        "caption": "**Figure 5:** Sending an uplink frame"
    }
}]$

If you get a response in your TTN live data feed as in Figure 6, then you are all set!

$plugin[{
    "type": "callout",
    "data": {
        "text": "Be sure to have this window opened prior to sending data through the RAK Serial Port or you will not be able to receive the packet sent. Logging out your The Things Network acccount would also clear all the data sent and not being able to receive packets sent.",
        "type": "info",
        "title": "Note:"
    }
}]$

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1582558490\/17326\/vab3mt37t1tozvj2bg0i.png",
        "mode": "responsive",
        "width": 1910,
        "height": 886,
        "caption": "**Figure 6:** Sending Data to TTN from RAK5205"
    }
}]$

