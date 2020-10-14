---
type: page
title: Assembly Guide
listed: true
slug: assembly-guide
---published

In order to create a functioning Gateway built around the RAK2287 concentrator you need to put several components together. Once the whole process is finished you will have a Gateway that can take full use of the benefit a LoRAWAN® network provides.

### Mount the Concentrator

Insert your **RAK2287 mPCIe card** into the mPCIe slot on the **RAK2287 Pi HAT**. Make sure the card fits snugly into the connector, it should end up sticking out in a **45-degree angle**. Gently press it down and fasten with 2 screws. If you have positioned the card right, the screw holes on the RAK2287 will match the ones on the RAK2287 Pi HAT. Use **Figure 1** as reference.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1592208794\/30867\/lslgxwgse7rmg7mmqmws.jpg",
        "mode": "600",
        "width": 681,
        "height": 681,
        "caption": "**Figure 1**: Assembly of the Concentrator and the HAT"
    }
}]$

### Antennas

The module comes with **two antennas, GPS and LoRa®**. Both have pigtail cables that have uFL connectors, which fit onto the corresponding ports on the RAK2287. The ports are labelled, match each antenna to its port and gently press it until the connectors fit one to the other.

$plugin[{
    "type": "callout",
    "data": {
        "text": "It is not recommended to have the device powered with the antennas detached. This might damage the circuity.",
        "type": "warning",
        "title": "Warning:"
    }
}]$

### Mount the HAT

Take the RAK2287 Pi HAT, that now has the RAK2287 concentrator module securely sitting on top and insert it over the Raspberry Pi. Both the Pi and the HAT have a **40-pin connector** that should fit together when pressed on top of each other.

### SD Card

Insert the SD card with the Firmware you flashed in the previous step into the SD card slot on the bottom of the Raspberry Pi.

### Boot

Power the raspberry Pi via the Micro USB port (Pi3) / USB type-C port (Pi4). As this is going to be the first time to boot the OS it might take a couple of minutes before everything is set up, so please be patient.  

$plugin[{
    "type": "callout",
    "data": {
        "text": "It is recommended to use at least a **2A power supply**.",
        "type": "info",
        "title": "Note:"
    }
}]$

