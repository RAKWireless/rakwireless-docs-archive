---
type: page
title: System Structure
listed: false
slug: system-structure---rak7243c
---published

The following figure shows the basic concept for LoRaWAN® system. RAK7243 Pilot
Gateway is the central hardware solution for all LoRa® based radio communication.
It receives and transmits radio messages. The processing of radio messages as well as
the protocol related tasks is done by embedded host system (Raspberry Pi). Received
and processed radio messages are being sent to a LoRaWAN® server. The concrete
segmentation of the protocol related tasks is outside the scope of this document

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1562511767\/17428\/git8ngad50mdpz96lox8.png",
        "mode": "responsive",
        "width": 1152,
        "height": 634,
        "caption": "**Figure 1:** Pilot Gateway System Structure"
    }
}]$

