---
type: page
title: Burning the Firmware
listed: true
slug: burning-the-firmware
---published

If the firmware version of your **RAK7204 LPWAN Environmental Sensor**  is newer than V3.0.0.0 or you have just burned the bootloader into the board according to the **Burning the Bootloader** section, follow the steps below

- Make sure you have set your RAK7204 to work in boot mode. If you have just burned the bootloader according to the previous section, it works in boot mode now. 
- Open and download the RAK Serial Port Tool [Here](https://downloads.rakwireless.com/en/LoRa/WisTrio-LoRa-RAK5205/Tools/RAK_SERIAL_PORT_TOOL_V1.2.1.zip) and Connect your board via the USB interface and enter the following **AT command** to let it work in boot mode.

$plugin[{
    "type": "callout",
    "data": {
        "text": "Before configuring your RAK7204, make sure you already connected the Battery provided  on your device in order for you to communicate with the device successfully.",
        "type": "warning",
        "title": "Warning"
    }
}]$

$plugin[{
    "type": "code-block",
    "data": {
        "languageBlocks": [
            {
                "code": "at+set_config=device:boot",
                "language": "none"
            }
        ]
    }
}]$

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1567397243\/18987\/jvuee0euhsqbsdnkd7cw.jpg",
        "mode": "responsive",
        "width": 2257,
        "height": 1468,
        "caption": "**Figure 1.** Entering Boot Mode"
    }
}]$

- Download the **RAK Upgrade Tool** from the RAKwireless website [here](https://downloads.rakwireless.com/en/LoRa/RAK612-LoRaButton/Tools/RAK%20LoRaButton%20Upgrade%20Tool%20V1.0.zip) then, open the tool. 

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1567397370\/18987\/txi7skysk8gtingjysud.jpg",
        "mode": "600",
        "width": 729,
        "height": 600,
        "caption": "**Figure 2:** RAK Upgrade Tool"
    }
}]$

- Download the latest firmware [here](https://downloads.rakwireless.com/en/LoRa/RAK7204/Firmware/) for the RAK7204

$plugin[{
    "type": "callout",
    "data": {
        "text": "Make sure to pick the appropriate bin file depending on the region you are in.\n\n> **\"RUI_RAK7204_V3.x.x.x.H\"** supported regions are: IN865, EU868, US915, AU915, KR920, AS920, AS923\n\n> **\"RUI_RAK7204_V3.x.x.x.L\u201d** supported regions are: EU433, CN470\n\nVisit this [**article**](https:\/\/www.thethingsnetwork.org\/docs\/lorawan\/frequencies-by-country.html) for more information on your local TTN frequency plan.",
        "type": "info",
        "title": "Note"
    }
}]$

- Click "Choose File" then choose the firmware that you have just downloaded: 

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1567398126\/18987\/hs89oyvlean3zvhjxlwe.jpg",
        "mode": "600",
        "width": 1467,
        "height": 1219,
        "caption": "**Figure 3.** Choosing the Correct Firmware file"
    }
}]$

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1567398182\/18987\/d5xgxy7cj8ic7qvglecl.jpg",
        "mode": "600",
        "width": 733,
        "height": 609,
        "caption": "**Figure 4:** Start Upgrade"
    }
}]$

- Choose the correct "**COM Port**", then click Start to Upgrade and wait for a couple of minutes. If it won't start, push the reset button on your RAK7204.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1567398317\/18987\/aqblsh1kqm0nud2obujb.jpg",
        "mode": "600",
        "width": 732,
        "height": 608,
        "caption": "**Figure 5:** Firmware Upgrading in Process"
    }
}]$

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1567398325\/18987\/ih6llchh4ao5vxxjilyv.jpg",
        "mode": "600",
        "width": 728,
        "height": 603,
        "caption": "**Figure 6:**  Firmware Upgrade Finished"
    }
}]$

- Now, **CLOSE** the upgrade tool and and proceed to the next section.

### Testing the Installed Firmware

In order for you to check if you have successfully installed the firmware on your RAK7204 LPWAN Environmental Sensor, open the Serial Port tool again. Press the "Reset button" or type the command below. If everything works  perfectly, you should see the following message below:

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1567406426\/18987\/kyecdcrh2uznsuyqjoqv.jpg",
        "mode": "600",
        "width": 543,
        "height": 659,
        "caption": "**Figure 7:** Restarting Your Device"
    }
}]$

This information means that you have uploaded the Firmware successfully!

