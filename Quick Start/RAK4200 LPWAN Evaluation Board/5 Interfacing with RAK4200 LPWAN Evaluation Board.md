---
type: page
title: Interfacing with RAK4200 LPWAN Evaluation Board
listed: true
slug: interfacing-with-rak4200-lora-evaluation-board
---published

In order for you to be able to interface with the RAK4200 LPWAN Evaluation Board with your Windows Machine, you need to download the RAK Serial Port Tool **[here](https://downloads.rakwireless.com/en/LoRa/Tools/RAK_SERIAL_PORT_TOOL_V1.2.1.zip).**

$plugin[{
    "type": "callout",
    "data": {
        "text": "Before powering the RAK4200 LPWAN Evaluation Board , you should install the LoRa\u00ae antenna. Not doing so might damage the board",
        "type": "warning",
        "title": "Warning"
    }
}]$

- Connect your RAK4200 LPWAN Evaluation Board to your Windows Machine using the provided Micro USB cable.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1579836701\/24364\/kq51hnmw5xoquykfd1dw.png",
        "mode": "300",
        "width": 6824,
        "height": 4931,
        "caption": "**Figure 1:** RAK4200 LPWAN Evaluation Board to Laptop Connection"
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
        "caption": "**Figure 2:** RAK Serial Port Tool"
    }
}]$

- In choosing the correct COM Port number for your device. Go to your Device Manager by pressing : Windows + R and type `devmgmt.msc` or search in the Start Menu

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1578838608\/24364\/cj2yhkexwphkmkscqoxb.png",
        "mode": "responsive",
        "width": 769,
        "height": 630,
        "caption": "**Figure 3:** Device Manager"
    }
}]$

- Look for Ports (COM & LPT) and Find the name **USB-SERIAL CH340** and take note of the COM Port Number. 

$plugin[{
    "type": "callout",
    "data": {
        "text": "If you didn't find any Port with the name USB-Serial CH340, make sure you have downloaded the CH340 Drivers in your Machine.",
        "type": "info",
        "title": "Note"
    }
}]$

- Choose the Correct Port Number from the device manager and the Correct Baudrate then click Open:

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1578839204\/24364\/gqq1izhoofyqj6ecrgaa.png",
        "mode": "responsive",
        "width": 922,
        "height": 604,
        "caption": "**Figure 4:** Correct Port Number and Correct Baud rate"
    }
}]$

