---
type: page
title: Device Firmware Setup
listed: true
slug: device-firmware-setup
---published

An easy and quick way to have a fully functional gateway is by using a Precompiled Firmware Image provided. In this document, is the step by step instructions on how to install the Image into your SD Card used for the gateway.

### Burn the latest Firmware

1. Download the latest firmware **[here](https://downloads.rakwireless.com/en/LoRa/Pilot-Gateway-Pro-RAK7243/Firmware/)**, which is based on the Raspbian OS.
2. You need to use an image writing tool to install the firmware on the SD Card. For this, You will be using **[Etcher](https://www.balena.io/etcher/),** which is an open source utility used for burning image files.
3. Insert your SD Card into the SD Card reader and plug it into your Computer.
4. Open the Etcher Software, and select the downloaded image file thru the ( **Label - 1** ) button in the image below.

$plugin[{
    "type": "callout",
    "data": {
        "text": "Your SD Card should be automatically detected by the Etcher software in the Label - 2 of the\nimage below. If not, kindly ensure proper connection.",
        "type": "info",
        "title": "Note:"
    }
}]$

Click Flash and wait for a couple of minutes until it displays "**Flash Complete.**"

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1580824114\/13873\/htym80ccfx3xe5ycormf.png",
        "mode": "responsive",
        "width": 1210,
        "height": 732,
        "caption": "**Figure 1**: Balena Etcher Software"
    }
}]$

