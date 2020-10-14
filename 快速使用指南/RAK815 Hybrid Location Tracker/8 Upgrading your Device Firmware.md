---
type: page
title: Upgrading your Device Firmware
listed: true
slug: upgrading-your-device-firmware
---published

Device Firmware Upgrade or DFU is a tool in upgrading your firmware. It is part of the open source project you downloaded for upgrading the firmware of your IAR and Keil Compiler. 

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1562131146\/17098\/kak2afa8wijmscerr3vm.jpg",
        "mode": "responsive",
        "width": 823,
        "height": 379,
        "caption": "Figure 1. DFU File Location"
    }
}]$

We provide users with hex files, which users can find in the open source project Doc
folder:

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1562131438\/17098\/etw1vczpsp3mwpx7a3qt.jpg",
        "mode": "responsive",
        "width": 796,
        "height": 378,
        "caption": "Figure 2. DFU Hex Files"
    }
}]$

However, it should be noted that using the DFU function of the nRF, unlike the
previous firmware programming method, the bootloader firmware must be programmed. Therefore, three firmwares need to be programmed to use the DFU function. They are the
Bluetooth protocol stack firmware, the DFU application firmware, and the bootload
firmware. Bootload firmware can be found in open source functions.

$plugin[{
    "type": "callout",
    "data": {
        "text": "For details on how to program the Bluetooth protocol stack and application firmware, review the Device Firmware Setup.",
        "type": "info",
        "title": "Note!"
    }
}]$

The following figure shows how to program bootloader firmware:

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1561977221\/17098\/nmen1o0wykcmqoig5v9y.jpg",
        "mode": "responsive",
        "width": 1245,
        "height": 899,
        "caption": "Figure 3. Programming Bootloader Firmware"
    }
}]$

After all firmware are written, the device will automatically restart. At this time, use your
mobile phone Bluetooth scan, you will see a device named "RAK813_DFU".

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1561977182\/17098\/tg5ghrucxgjohag2k6zj.jpg",
        "mode": "responsive",
        "width": 1097,
        "height": 500,
        "caption": "Figure 4. RAK813 DFU Bluetooth Radio"
    }
}]$

Use the nRF official phone app nRF Connect to connect to the device's Bluetooth. 

To upgrade the firmware, you need to import the upgraded firmware to your mobile phone. The upgrade file, a zip file, is accessible from the downloaded open source code by following this directory: **RAK813-BreakBoard-master**>> **Doc**>> **Hex**>> **rak815_app_package.zip**. Copy this sample upgrade file to your mobile phone. 

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1562131838\/17098\/vktrgcoxocld0zlcfoew.jpg",
        "mode": "responsive",
        "width": 784,
        "height": 381,
        "caption": "Figure 5. DFU App Package Zip File"
    }
}]$

$plugin[{
    "type": "callout",
    "data": {
        "text": "About how to make an upgraded zip file, and how to program DFU step by step, \nvisit the official forum detailing the method. Interested parties can view this link: https:\/\/devzone.nordicsemi.com\/b\/blog\/posts\/getting-started-with-nordics-secure-dfu-bootloader",
        "type": "info",
        "title": "Info"
    }
}]$

Open the nRF app and press "**CONNECT**" button in the **RAK813_DFU** Bluetooth. Then, click the **DFU** icon in the
upper right corner.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1561977546\/17098\/louloo2ndneemlis73kr.jpg",
        "mode": "responsive",
        "width": 940,
        "height": 877,
        "caption": "Figure 6. Connecting to RAK813 DFU"
    }
}]$

Select the **rak815_app_package.zip** file, and the device will automatically start upgrading the firmware. 

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1561977571\/17098\/f30dotlk2xrw9q08ztrz.jpg",
        "mode": "responsive",
        "width": 979,
        "height": 905,
        "caption": "Figure 7.  Importing the Upgrade Zip File"
    }
}]$

At this point, the program will jump to the bootload and execute the bootload. Then click on the
RAK813_DFU as highlighted in the figure to the right, you can see the progress of the program sent.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1561977560\/17098\/g4ovmbqkzmyfpqoddcu4.jpg",
        "mode": "responsive",
        "width": 987,
        "height": 914,
        "caption": "Figure 8. Upgrade Progress Chart"
    }
}]$

After the program upgrade is complete, reset the device and you will see that your
device's Bluetooth broadcast name has changed.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1561977586\/17098\/y3qrazuax3ld0gtxy5yj.jpg",
        "mode": "responsive",
        "width": 441,
        "height": 838,
        "caption": "Figure 9. Device's Bluetooth Broadcast Changes"
    }
}]$

Great, you have completed the RAK815 hybrid Location Tracker Configuration and successfully upgraded the firmware. You are now ready to try your own projects using the device.

