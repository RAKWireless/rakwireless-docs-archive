---
type: page
title: Interfacing with RAK4260 LPWAN Breakout Module
listed: true
slug: interfacing-with-rak4260-lpwan-breakout-module
---published

$plugin[{
    "type": "callout",
    "data": {
        "text": "Before powering the RAK4260 Breakout Module, make sure you have installed the included LoRa\u00ae Antenna. Not doing so might damage the board.",
        "type": "warning",
        "title": "Warning:"
    }
}]$

### USB to UART

- Connect your USB to UART converter to the pin header on the RAK4260 via a set of 4 dupont lines. Use Figure 1 for reference on wiring the device properly.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1588942650\/29200\/khx1xylkxamtxnrdr4hc.png",
        "mode": "responsive",
        "width": 3183,
        "height": 1306,
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
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1588908184\/29200\/tevmcgckmbihsvnqwwnc.png",
        "mode": "600",
        "width": 769,
        "height": 630,
        "caption": "**Figure 2**: COM Port settings"
    }
}]$

- Open the RAK Serial Port Tool. Select the COM Port number (the one you noted in the previous step) and set the **Baud Rate to 115200**. Click “**OPEN**” and you should be connected to the board and be able to send commands.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1588908238\/29200\/makiakve6dqflaz12brg.png",
        "mode": "600",
        "width": 922,
        "height": 604,
        "caption": "**Figure 3**: Configuring the RAK Serial Port Tool"
    }
}]$

### J-Link Connection

Connect the tool in accordance with the diagram shown in Figure 4.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1588942673\/29200\/r2er8e0macfohhb6z50h.png",
        "mode": "600",
        "width": 2945,
        "height": 1536,
        "caption": "**Figure 4**: J-Link to RAK4260 LPWAN Breakout Module"
    }
}]$

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1588942690\/29200\/ibgqirlimomzqgey0g5g.png",
        "mode": "600",
        "width": 4770,
        "height": 1898,
        "caption": "**Figure 5**: J-link connection"
    }
}]$

