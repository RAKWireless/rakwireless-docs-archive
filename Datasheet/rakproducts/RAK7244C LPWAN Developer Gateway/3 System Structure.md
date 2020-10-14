---
type: page
title: System Structure
listed: true
slug: system-structure-rak7244c
---published

The following figure shows the basic concept for LoRaWAN® system. The RAK2245 is the central hardware solution for all LoRa® based radio communication. It receives and transmits radio messages and acts as modem to signals among others. The processing of radio messages as well as the protocol related tasks is done by embedded host system (Raspberry Pi). Received and processed radio messages are being sent to a LoRaWAN® server. The concrete segmentation of the protocol related tasks is outside the scope of this document.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1575652216\/-1\/wmishmfyonwnd31mgbph.png",
        "mode": "responsive",
        "width": 1201,
        "height": 725,
        "caption": "**Figure 1:** RAK7244C Gateway System Structure"
    }
}]$

