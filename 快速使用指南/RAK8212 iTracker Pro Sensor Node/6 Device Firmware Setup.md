---
type: page
title: Device Firmware Setup
listed: false
slug: device-firmware-setup
---draft

The main objective of this document is to have the latest firmware of the RAK8212 burned for it to be fully functional. Follow into the steps and expect an enjoyable testing and usage of the device in the future. 

## Burn the latest Firmware

$plugin[{
    "type": "callout",
    "data": {
        "text": "The RAK8212 must be connected into the computer or laptop before going through the following steps. If not, kindly walk through the Device Interfacing document on how to interface the RAK8212 and the computer.",
        "type": "warning",
        "title": "Note:"
    }
}]$

1. Download the latest RAK8212 firmware **[here ](https://downloads.rakwireless.com/en/Cellular/RAK8212/Firmware/RAK8212_with_Hologram_based_on_RUI_V1.0.rar)**as provided by the service provider. 
2. Open the software, **nRFgo Studio** in your computer or laptop. If the software is not installed yet, kindly download and install it from provider's website **[here](https://www.nordicsemi.com/)**.
3. Select “nRF5x programing” in the Device Manager panel as shown in the screenshot below.
4. You can also click the **“Erase all”** button to erase the firmware which had been programmed into your RAK8212 module before. 

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1562040226\/17168\/w63vtrw8rgsrygtfxzdf.jpg",
        "mode": "responsive",
        "width": 840,
        "height": 767,
        "caption": null
    }
}]$

    5. Click browse and locate the firmware image file downloaded beforehand. The firmware file has a extension file of ".hex". A screenshot is provided below for proper guidance. 

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1562040744\/17168\/ixxctxnq1ecgbgom5hvm.jpg",
        "mode": "responsive",
        "width": 905,
        "height": 490,
        "caption": null
    }
}]$

    6. Click the"Program" button and wait until a pop-up displays which signifies that the firmware image has been burned into the RAK8212. A screenshot is provided below for proper guidance. 

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1562041053\/17168\/iyvxpwubru2kzbrl12yz.jpg",
        "mode": "full",
        "width": 713,
        "height": 463,
        "caption": null
    }
}]$

