---
type: page
title: Interfacing with the RAK7204 LPWAN Environmental Sensor
listed: true
slug: interfacing-with-the-rak7204-lora-environmental-sensor
---published

In order for you to be able to interface with the RAK7204 LPWAN Environmental Sensor with your Windows Machine, you need to download the RAK Serial Port Tool **[here](https://downloads.rakwireless.com/en/LoRa/Tools/RAK_SERIAL_PORT_TOOL_V1.2.1.zip).**

$plugin[{
    "type": "callout",
    "data": {
        "text": "The included battery is **non rechargeable**. Please do note that when configuring the device, you have to connect the battery first in order for it to work.",
        "type": "warning",
        "title": "Warning"
    }
}]$

- Connect your RAK7204 LPWAN Environmental Sensor in your Windows Machine using the provided micro-usb cable.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1590753721\/25196\/mpzggerv2neb86iwsoet.jpg",
        "mode": "responsive",
        "width": 10683,
        "height": 4990,
        "caption": "**Figure 1:** RAK7204 LPWAN Environmental Sensor to Laptop Connection"
    }
}]$

$plugin[{
    "type": "callout",
    "data": {
        "text": "The pin distance of the battery connector is **2.0mm**. Reverse connection or short circuit may damage the device and may cause overheating and combustion of the battery. Therefore, when replacing the battery, it is necessary to strictly confirm whether the positive and negative poles of the connector are correct.",
        "type": "warning",
        "title": "Warning"
    }
}]$

- Open the RAK Serial Port Tool :

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1580490964\/25196\/oju7ucgriixkmghcaqxy.png",
        "mode": "responsive",
        "width": 922,
        "height": 604,
        "caption": "**Figure 2:** RAK Serial Port Tool"
    }
}]$

- In choosing the correct COM Port number for your device. Go to your Device Manager by pressing : Windows + R and type `devmgmt.msc` or search in the Start Menu

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1580491000\/25196\/xjttdlmkzfsh5pg8vwcg.png",
        "mode": "600",
        "width": 1041,
        "height": 912,
        "caption": "**Figure 3:** Device Manager"
    }
}]$

- Look for Ports (COM & LPT) and Find the name Silicon Labs CP210x USB to UART Bridge and take note of the COM Port Number.

$plugin[{
    "type": "callout",
    "data": {
        "text": "If you didn't find any Port with the name Silicon Labs CP210x USB to UART Bridge, make sure you have downloaded the CP210x USB Drivers in your Machine.",
        "type": "info",
        "title": "Info"
    }
}]$

- Choose the Correct Port Number from the device manager and the Correct Baudrate then click Open:

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1580491121\/25196\/nujplxpattmmleoaaghm.png",
        "mode": "responsive",
        "width": 922,
        "height": 604,
        "caption": "**Figure 4:** Correct Port Number and Correct Baud rate"
    }
}]$

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1580908544\/25196\/w90quzm2ah5civgeojbx.png",
        "mode": "responsive",
        "width": 920,
        "height": 603,
        "caption": null
    }
}]$

