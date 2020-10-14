---
type: page
title: Interfacing with RAK4600 LPWAN Breakout Module
listed: true
slug: interfacing-with-rak4600-lpwan-breakout-module
---published

To interface with the RAK4600 LPWAN Breakout Module with your Windows Machine, you need to download the RAK Serial Port Tool **[here](https://downloads.rakwireless.com/en/LoRa/Tools/RAK_SERIAL_PORT_TOOL_V1.2.1.zip).**

$plugin[{
    "type": "callout",
    "data": {
        "text": "Before powering the RAK4600 Breakout Module, make sure you have installed the included LoRa\u00ae  and BLE antennas. Not doing so might damage the board.",
        "type": "warning",
        "title": "Warning"
    }
}]$

- Connect your USB to UART converter to the pin header on the RAK4600 via a set of 4 dupont lines. Use Figure 1 for reference on wiring the device properly.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1588246818\/28892\/rfziidlqd9cxgmtmu746.jpg",
        "mode": "responsive",
        "width": 1209,
        "height": 493,
        "caption": "**Figure 1**: Powering up and interfacing with the board"
    }
}]$

- Go to your Device Manager by pressing: Windows + R and typing devmgmt.msc or search in the Start Menu.
- Look for Ports (**COM & LPT**) and find the name **USB-SERIAL CH340** and take note of the COM Port Number as you will need it to connect with the board.

$plugin[{
    "type": "callout",
    "data": {
        "text": "Windows 10 should recognize the board and automatically install drivers, however if it is missing in the COM & LP ports list you need to manually install the CH340 Drivers.",
        "type": "info",
        "title": "Note:"
    }
}]$

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1588246979\/28892\/gok1zmycficjlo2wamj3.png",
        "mode": "responsive",
        "width": 769,
        "height": 630,
        "caption": "**Figure 2**: COM Port settings"
    }
}]$

- Open the RAK Serial Port Tool. Select the COM Port number (the one you noted in the previous step) and set the **Baud Rate to 115200**. Click “**OPEN**” and you should be connected to the board and be able to send commands.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1588247052\/28892\/decfkp71gjl8mixzdvzs.png",
        "mode": "responsive",
        "width": 922,
        "height": 604,
        "caption": "**Figure 3**: Configuring the RAK Serial Port Tool"
    }
}]$

