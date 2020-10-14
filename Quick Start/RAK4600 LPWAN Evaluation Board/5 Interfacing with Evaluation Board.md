---
type: page
title: Interfacing with Evaluation Board
listed: true
slug: interfacing-with-rak4600
---published

In order for you to be able to interface with the Evaluation Board, using a Windows Machine, you need to download the RAK Serial Port Tool **[here](https://downloads.rakwireless.com/en/LoRa/Tools/RAK_SERIAL_PORT_TOOL_V1.2.1.zip).**

$plugin[{
    "type": "callout",
    "data": {
        "text": "Before powering the RAK4600 LPWAN Evaluation Board , you should install the LoRa\u00ae and BLE Antenna first. Not doing so might damage the board.",
        "type": "warning",
        "title": "Warning"
    }
}]$

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1580179366\/24946\/u9lgszijijydbyjkgwnx.png",
        "mode": "responsive",
        "width": 6531,
        "height": 2630,
        "caption": "**Figure 1:** LoRa\u00ae and BLE Antenna"
    }
}]$

- Connect your RAK4600 LPWAN Evaluation Board to your Windows Machine using the provided Micro USB cable.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1579846721\/24946\/rzolxz9ojiyg0lkqpkqz.png",
        "mode": "300",
        "width": 6868,
        "height": 4931,
        "caption": "**Figure 2:** RAK4600 LPWAN Evaluation Board to Laptop Connection"
    }
}]$

- Open the RAK Serial Port Tool :

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1578837631\/24364\/gnm0smmpj2hiaaxv65m2.png",
        "mode": "responsive",
        "width": 922,
        "height": 604,
        "caption": "**Figure 3:** RAK Serial Port Tool"
    }
}]$

- In order to choose the correct COM Port number for your device you need to go to your Device Manager by pressing : Windows + R and typing `devmgmt.msc` or search in the Start Menu

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1578838608\/24364\/cj2yhkexwphkmkscqoxb.png",
        "mode": "responsive",
        "width": 769,
        "height": 630,
        "caption": "**Figure 4:** Device Manager"
    }
}]$

- Look for Ports (COM & LPT) and Find the name **USB-SERIAL CH340** and take note of the COM Port Number.

$plugin[{
    "type": "callout",
    "data": {
        "text": "If you didn't find any Port with the name USB-Serial CH340, make sure you have instaalled the  the [CH340 Drivers](https:\/\/downloads.rakwireless.com\/LoRa\/RAK811\/Tools\/CH340%20Drive.rar) to your Machine.",
        "type": "info",
        "title": "Note"
    }
}]$

- Choose the Correct Port Number from the device manager and the Correct Baud Rate then click Open:

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1578839204\/24364\/gqq1izhoofyqj6ecrgaa.png",
        "mode": "responsive",
        "width": 922,
        "height": 604,
        "caption": "**Figure 5:** Correct Port Number and Correct Baud rate"
    }
}]$

