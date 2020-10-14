---
type: page
title: Assembly Guide
listed: true
slug: assembly-guide
---published

For the RAK8213 module to function as an extension for the Raspberry Pi, you need to assemble several components:

### SIM card

Insert the SIM card in the slot that sits on the back of the RAK8213. Best do this now as later on, it will be more difficult to access.

### Mount the RAK8213 Module

Insert your **RAK8213 module** into the mPCIe slot on the **RAK8213 Pi HAT**. Make sure the card fits snugly into the connector. It should end up sticking out at an **angle of 45°**. Gently press it down and fasten it with two (2) screws. If you have positioned the card right, the screw holes on the RAK8213 will match the ones on the RAK8213 HAT. Use figure 1 below as a reference.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1593139112\/31134\/aour6oafhcyhrjcsvls2.jpg",
        "mode": "600",
        "width": 827,
        "height": 827,
        "caption": "**Figure 1**: Assembly of the NB-IoT Module and the HAT"
    }
}]$

### Antennas

The module comes with two (2) antennas: **Cellular** and **GPS**. Both have pigtail cables that have uFL connectors, which fit onto the corresponding ports on the RAK8213. The GPS antenna is **on the left** when looking at the module from the side where the BG96 is. Match each antenna to its port and gently press it until the connectors fit one to the other.

$plugin[{
    "type": "callout",
    "data": {
        "text": "Do not power on the device when the antennas are detached to avoid damage in the circuitry.",
        "type": "warning",
        "title": "Warning"
    }
}]$

### Mount the HAT

Take the RAK8213 HAT, which now has the RAK8213 securely sitting on top, and insert it over the Raspberry Pi. Both the Pi and the HAT have a **40-pin connector** that should fit together snugly when pressed on top of each other.

### Power the RAK8213

$plugin[{
    "type": "callout",
    "data": {
        "text": "The RAK8213 requires additional power via the Micro USB port on the RAK8213 Pi HAT.",
        "type": "info",
        "title": "Info"
    }
}]$

For the above-noted purpose, attach a standard Micro USB to USB cable connecting one of the Raspberry’s USB ports to the Micro USB port on the RAK8213 HAT.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1593051257\/31134\/qwrvj1r9h0w9etzkiku4.png",
        "mode": "300",
        "width": 1275,
        "height": 1653,
        "caption": "**Figure 2**: Assembly of the NB-IoT Module and the HAT"
    }
}]$

### SD card

Insert the SD card with the Firmware you flashed in the previous step into the SD card slot on the bottom of the Raspberry Pi.

### Boot

Power the raspberry Pi via the **Micro USB port (Pi3) / USB type c port (Pi4)**. As this is going to be the first time to boot the OS, wait for a couple of minutes for everything to set up.

$plugin[{
    "type": "callout",
    "data": {
        "text": "It is recommended to use at least a **2A power supply**.",
        "type": "info",
        "title": "Info"
    }
}]$

