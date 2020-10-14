---
type: page
title: Interfacing with RAK4200 LPWAN Breakout Module
listed: true
slug: interfacing-with-rak4200-lpwan-breakout-module
---published

In order for you to be able to interface with the RAK4200 LPWAN Evaluation Board with your Windows Machine, you need to download the RAK Serial Port Tool **[here](https://downloads.rakwireless.com/en/LoRa/Tools/RAK_SERIAL_PORT_TOOL_V1.2.1.zip).**

$plugin[{
    "type": "callout",
    "data": {
        "text": "Before powering the RAK4200 LPWAN Breakout Module, make sure you have installed the included LoRa\u00ae Antenna. Not doing so might damage the board.",
        "type": "warning",
        "title": "Warning"
    }
}]$

- Connect your USB to UART converter to the pin header on the RAK4200 via a set of 4 dupont lines. Use **Figure 1** for reference on wiring the device properly.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1588235235\/28884\/a6qkw8rluttf89wrzwum.jpg",
        "mode": "responsive",
        "width": 1278,
        "height": 521,
        "caption": "**Figure 1**: Powering up and interfacing with the board"
    }
}]$

- Go to your Device Manager by pressing: Windows + R and typing devmgmt.msc or search in the Start Menu.

$plugin[{
    "type": "callout",
    "data": {
        "text": "Windows 10 should recognize the board and automatically install drivers, however if it is missing in the COM & LP ports list you need to manually install the CH340 Drivers.",
        "type": "info",
        "title": "Note:"
    }
}]$

- Look for Ports (COM & LPT) and Find the name USB-SERIAL CH340 and take note of the COM Port Number as you will need it to connect with the board. You might have another model number but the wording “USB-SERIAL” should be present in some form.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1588235908\/28884\/tvkkkqpdpkszdf4ioyg6.png",
        "mode": "responsive",
        "width": 769,
        "height": 630,
        "caption": "**Figure 2**: COM Port settings"
    }
}]$

-  Open the RAK Serial Port Tool. Select the COM Port number (the one you noted in the previous step) and set the **Baud Rate to 115200**. Click “**OPEN**” and you should be connected to the board and be able to send commands.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1588236136\/28884\/ybo1fczw8uhagao2io7h.png",
        "mode": "responsive",
        "width": 922,
        "height": 604,
        "caption": "**Figure 3**: Configuring the RAK Serial Port Tool"
    }
}]$

