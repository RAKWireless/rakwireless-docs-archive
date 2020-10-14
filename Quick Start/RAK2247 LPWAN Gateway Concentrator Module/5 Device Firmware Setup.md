---
type: page
title: Device Firmware Setup
listed: false
slug: device-firmware-setup
---published

An easy and quick way to have a fully functional gateway is by using a Precompiled Firmware Image provided. In this document, is the step by step instructions on how to install the Image into your SD Card used for the gateway.

## Burn the latest Firmware

1. Download the latest firmware **[here](https://downloads.rakwireless.com/en/LoRa/RAK2245-Pi-HAT/Firmware/)**, which is based on the Raspbian OS.
2. You need to use an image writing tool to install the firmware on the SD Card. For this, You will be using **[Etcher](https://www.balena.io/etcher/),** which is an open source utility used for burning image files.
3. Insert your SD Card into the SD Card reader and plug it into your Computer.
4. Open the Etcher Software, and select the downloaded image file thru the ( **Label - 1** ) button in the image below.

$plugin[{
    "type": "callout",
    "data": {
        "text": "Your SD Card should be automatically detected by the Etcher software in the Label - 2 of the image below. If not, kindly ensure proper connection.",
        "type": "info",
        "title": "Note"
    }
}]$

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1579871067\/16436\/vyjxepzwfdwympdjef42.jpg",
        "mode": "responsive",
        "width": 1010,
        "height": 634,
        "caption": "Figure 1: Balena Etcher Software"
    }
}]$

- Click "**Flash!**" and wait until the process completes automatically.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1579871098\/16436\/ggkhrwviovuskdlltqoz.png",
        "mode": "responsive",
        "width": 1005,
        "height": 645,
        "caption": "**Figure 2**: Firmware Burning Progress"
    }
}]$

- A "**Flash Complete!**" prompt is then shown in Balena once the burning is complete.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1579871138\/16436\/llab6gdoodtkgcdq9jpy.png",
        "mode": "responsive",
        "width": 1011,
        "height": 646,
        "caption": "**Figure 3**: Firmware Burning Complete"
    }
}]$

You can now then close the Balena software and insert the SD card into your RAK2247 LoRaWAN™ Gateway Concentrator Module.

