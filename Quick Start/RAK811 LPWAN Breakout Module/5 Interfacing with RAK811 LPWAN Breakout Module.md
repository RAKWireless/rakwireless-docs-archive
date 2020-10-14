---
type: page
title: Interfacing with RAK811 LPWAN Breakout Module
listed: true
slug: interfacing-with-rak811-lora-breakout-module
---published

In order for you to be able to interface with the RAK811 LPWAN Breakout Module with your Windows Machine, you need to download the RAK Serial Port Tool **[here](https://downloads.rakwireless.com/en/LoRa/Tools/RAK_SERIAL_PORT_TOOL_V1.2.1.zip).**

$plugin[{
    "type": "callout",
    "data": {
        "text": "Before powering the RAK811 LPWAN Breakout Module , you should install the LoRa antenna first . Not doing so might damage the board",
        "type": "warning",
        "title": "Warning"
    }
}]$

- Connect your RAK811 LPWAN Breakout Board with the following diagram below. 
- **Figure 1** shows the Pinout Diagram of the Board and **Figure 2** shows how to connect the RAK811 LPWAN Breakout Board to the UART Module.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1588867819\/24855\/a7knovidcpugjawfmjmy.jpg",
        "mode": "responsive",
        "width": 6000,
        "height": 6000,
        "caption": "**Figure 1:** RAK811 LPWAN Breakout Module Pinout Diagram"
    }
}]$

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1579534207\/24855\/a5vvi5oofgnq7mwpiavn.jpg",
        "mode": "600",
        "width": 4167,
        "height": 2590,
        "caption": "**Figure 2:** RAK811 to USB Uart Module Connection"
    }
}]$

- Connect your USB - UART Module to your Windows Machine and Open RAK Serial Port Tool:

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1579534334\/24855\/ou15nrdveyhmrzo8byof.png",
        "mode": "responsive",
        "width": 922,
        "height": 604,
        "caption": "**Figure 3:** RAK Serial Port Tool"
    }
}]$

- In choosing the correct COM Port number for your device. Go to your Device Manager by pressing : Windows + R and type `devmgmt.msc` or search in the Start Menu

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1579534970\/24855\/siqhrem8xxxnvhj7vttn.png",
        "mode": "responsive",
        "width": 769,
        "height": 630,
        "caption": "**Figure 4:** Device Manager"
    }
}]$

- Look for Ports (COM & LPT) . Find the name of of your USB UART Module driver and take note of the COM Port Number.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1579535265\/24855\/rib8pvikbtggt9xryvxp.png",
        "mode": "responsive",
        "width": 922,
        "height": 604,
        "caption": "**Figure 5:** Correct Port Number and Correct Baud rate"
    }
}]$

