---
type: page
title: Interfacing with the RAK7205/RAK5205 WisTrio LPWAN Tracker
listed: true
slug: interfacing-with-the-rak7205-rak5205-wistrio-lora-tracker
---published

In order for you to be able to interface with the RAK7205/RAK5205 WisTrio LPWAN Tracker with your Windows Machine, you need to download the RAK Serial Port Tool **[here](https://downloads.rakwireless.com/en/LoRa/Tools/RAK_SERIAL_PORT_TOOL_V1.2.1.zip).**

$plugin[{
    "type": "callout",
    "data": {
        "text": "Before powering the RAK5205 , you should install the LoRa\u00ae and GPS antenna first . Not doing so might damage the board",
        "type": "warning",
        "title": "Warning"
    }
}]$

- Connect your RAK5205 WisTrio LPWAN Tracker in your Windows Machine using the provided micro-usb cable.
- Open the RAK Serial Port Tool :

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1580363969\/25063\/teufuzsi3aykwmda4un2.png",
        "mode": "responsive",
        "width": 922,
        "height": 604,
        "caption": "**Figure 1:** RAK Serial Port Tool"
    }
}]$

- In choosing the correct COM Port number for your device. Go to your Device Manager by pressing : Windows + R and type devmgmt.msc or search in the Start Menu

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1580364531\/25063\/jnsaeljcwqk3gnxjvgum.png",
        "mode": "600",
        "width": 1041,
        "height": 912,
        "caption": "**Figure 2:** Device Manager"
    }
}]$

- Look for Ports (COM & LPT) and Find the name Silicon Labs CP210X USB to UART Bridge and take note of the COM Port Number.

$plugin[{
    "type": "callout",
    "data": {
        "text": "If you didn't find any Port with the name Silicon Labs CP210X , make sure you have downloaded the CP210X Drivers in your Machine.",
        "type": "info",
        "title": "Info"
    }
}]$

- Choose the Correct Port Number from the device manager and the Correct BaudRate then click Open:

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1580364780\/25063\/ipc7wkiipcbsfrgvtm9e.png",
        "mode": "responsive",
        "width": 922,
        "height": 604,
        "caption": "**Figure 3:** Correct COM Port and Baudrate"
    }
}]$

