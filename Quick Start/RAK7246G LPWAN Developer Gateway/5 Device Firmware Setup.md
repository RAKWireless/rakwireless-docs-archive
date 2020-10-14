---
type: page
title: Device Firmware Setup
listed: true
slug: device-firmware-setup
---published

An easy and quick way to have a fully functional gateway is by using a Precompiled Firmware Image provided. In this document, is the step by step instructions on how to install the Image into your SD Card used for the gateway.

### Burn the latest Firmware

$plugin[{
    "type": "callout",
    "data": {
        "text": "If your RAK7246G LPWAN Developer Gateway has the latest firmware image in the SD card, you can\nskip this section.",
        "type": "info",
        "title": "Note:"
    }
}]$

1. Download the latest firmware **[here](https://doc.rakwireless.com/rak7246---rpi-lora-gateway/downloads#rak7246g-firmware)**, which is based on the Raspbian OS.
2. You need to use an image writing tool to install the firmware on the SD Card. For this, You will be using **[Etcher](https://doc.rakwireless.com/rak7246---rpi-lora-gateway/downloads#balena-etcher),** which is an open source utility used for burning image files.
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

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1579345860\/24739\/rlab9zkj4uaytqh8gk6u.png",
        "mode": "responsive",
        "width": 1210,
        "height": 732,
        "caption": "**Figure 1:** Balena Etcher Software"
    }
}]$

Click "**Flash!**" and wait until the process completes automatically.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1579345755\/24739\/qixt8gdfngs0cbstycdo.png",
        "mode": "responsive",
        "width": 1210,
        "height": 732,
        "caption": "**Figure 2**: Firmware Burning Progress"
    }
}]$

A "**Flash Complete!**" prompt is then shown in Balena once the burning is complete.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1579345979\/24739\/kpkps157t1wvwdmdydm0.png",
        "mode": "responsive",
        "width": 1210,
        "height": 732,
        "caption": "**Figure 3**: Firmware Burning Complete"
    }
}]$

You can now then close the Balena software and insert the SD card into your RAK7246G LPWAN Developer Gateway

