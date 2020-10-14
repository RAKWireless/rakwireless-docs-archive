---
type: page
title: Upgrading your Device Firmware
listed: true
slug: upgrading-your-device-firmware
---published

Device Firmware Upgrade or DFU is a tool in upgrading your firmware. It is part of the [GitHub Open Source](https://github.com/RAKWireless/RAK813-BreakBoard) project you downloaded for upgrading the firmware of your IAR and Keil Compiler. 

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1579659717\/17098\/ymxjiioqpd6jfv8h6hui.jpg",
        "mode": "responsive",
        "width": 837,
        "height": 393,
        "caption": "**Figure 1**. DFU File Location"
    }
}]$

We provide users with hex files, which users can find in the open source project Doc
folder:

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1579659726\/17098\/ljqqgajl3mwzlyi2bbx1.jpg",
        "mode": "responsive",
        "width": 810,
        "height": 392,
        "caption": "**Figure 2**. DFU Hex Files"
    }
}]$

However, it should be noted that using the DFU function of the nRF, unlike the
previous firmware programming method, the bootloader firmware must be programmed. Therefore, three firmwares need to be programmed to use the DFU function. They are the
Bluetooth protocol stack firmware, the DFU application firmware, and the bootload
firmware. Bootload firmware can be found in open source functions.

$plugin[{
    "type": "callout",
    "data": {
        "text": "For details on how to program the Bluetooth protocol stack and application firmware, review the [Device Firmware Setup](https:\/\/doc.rakwireless.com\/rak815-hybrid-location-tracker\/device-firmware-setup).",
        "type": "info",
        "title": "Note!"
    }
}]$

- The following figure shows how to program bootloader firmware:

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1579659736\/17098\/dz64adye25uadke68xcp.jpg",
        "mode": "responsive",
        "width": 1259,
        "height": 913,
        "caption": "**Figure 3**. Programming Bootloader Firmware"
    }
}]$

After all firmware are written, the device will automatically restart. At this time, use your
mobile phone Bluetooth scan, you will see a device named "**RAK813_DFU**".

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1579659746\/17098\/f91ymso1y4jswquu8dyx.jpg",
        "mode": "300",
        "width": 1111,
        "height": 514,
        "caption": "**Figure 4**. RAK813 DFU Bluetooth Radio"
    }
}]$

Use the nRF official phone app nRF Connect to connect to the device's Bluetooth. 

To upgrade the firmware, you need to import the upgraded firmware to your mobile phone. The upgrade file, a zip file, is accessible from the downloaded open source code by following this directory: **RAK813-BreakBoard-master**>> **Doc**>> **Hex**>> **rak815_app_package.zip**. Copy this sample upgrade file to your mobile phone. 

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1579659760\/17098\/k9huc8sgzee3tspmeuhj.jpg",
        "mode": "responsive",
        "width": 798,
        "height": 395,
        "caption": "**Figure 5**. DFU App Package Zip File"
    }
}]$

$plugin[{
    "type": "callout",
    "data": {
        "text": "About how to make an upgraded zip file, and how to program DFU step by step, \nvisit the official forum detailing the method. Interested parties can view this link: [https:\/\/devzone.nordicsemi.com\/b\/blog\/posts\/getting-started-with-nordics-secure-dfu-bootloader](https:\/\/devzone.nordicsemi.com\/b\/blog\/posts\/getting-started-with-nordics-secure-dfu-bootloader)",
        "type": "info",
        "title": "Info"
    }
}]$

Open the nRF app and press "**CONNECT**" button in the **RAK813_DFU** Bluetooth. Then, click the **DFU** icon in the
upper right corner.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1579659784\/17098\/n6fv73oxlnuyozymoizb.jpg",
        "mode": "responsive",
        "width": 954,
        "height": 891,
        "caption": "**Figure 6**. Connecting to RAK813 DFU"
    }
}]$

Select the **rak815_app_package.zip** file, and the device will automatically start upgrading the firmware. 

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1579659797\/17098\/zttygc8yefvl13taaiik.jpg",
        "mode": "responsive",
        "width": 993,
        "height": 919,
        "caption": "**Figure 7**.  Importing the Upgrade Zip File"
    }
}]$

At this point, the program will jump to the bootload and execute the bootload. Then click on the
RAK813_DFU as highlighted in the figure to the right, you can see the progress of the program sent.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1579659811\/17098\/jfreob0xgcahf1ukuxim.jpg",
        "mode": "responsive",
        "width": 1001,
        "height": 928,
        "caption": "**Figure 8.** Upgrade Progress Chart"
    }
}]$

After the program upgrade is complete, reset the device and you will see that your
device's Bluetooth broadcast name has changed.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1579659825\/17098\/vbe1h6n1o9h72elk3og0.jpg",
        "mode": "responsive",
        "width": 455,
        "height": 852,
        "caption": "**Figure 9**. Device's Bluetooth Broadcast Changes"
    }
}]$

Great, you have completed the RAK815 Hybrid Location Tracker Configuration and successfully upgraded the firmware. You are now ready to try your own projects using the device.

