---
type: page
title: Device Firmware Setup
listed: true
slug: device-firmware-setup
---published

## Accessing the Open Source Directory

The RAK815 is an open source hardware where users can get all the information about the product. It includes schematic diagrams, program codes and other references which could be helpful in building your RAK815 projects. 

This open source project is based on the official code LoRaWAN1.0.2 and Nordic
nRF5 SDK 14.0.0, modified to support IAR8.11 and Keil5 Compiler. 

- To start with, download the files in this open source **[directory](https://github.com/RAKWireless/RAK813-BreakBoard).**

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1561958285\/16596\/clghuhczntqejlodiu96.jpg",
        "mode": "responsive",
        "width": 1238,
        "height": 608,
        "caption": "Figure 1. Open Source Directory for RAK815"
    }
}]$

## Downloading the Firmware

To enable the Bluetooth functionality of our device, you must first write the Bluetooth protocol stack using the official nRFgo Studio Tool. 

- Download and Install the nRFgo Studio Tool through the **[Nordic Official Site](http://www.nordicsemi.com/Products/Low-power-short-range-wireless/nRF52832)** or through this **[link](https://downloads.rakwireless.com/en/LoRa/RAK815/Tools/)**.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1561959403\/16596\/przz7zthhwxh0nzhy7ai.jpg",
        "mode": "responsive",
        "width": 1086,
        "height": 406,
        "caption": "Figure 2. nRFgo Studio tool Installer"
    }
}]$

### Installing of the J-Link Driver

1. Navigate to this **[J-Link Site](https://www.segger.com/downloads/jlink).**
2. Click  the “Click for downloads” under “J-Link Software and Documentation Pack”.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1561791051\/16596\/yynmq60crbbvjuy2ueay.jpg",
        "mode": "responsive",
        "width": 1296,
        "height": 634,
        "caption": "Figure 3. Downloading J-Link Software"
    }
}]$

    3.     Download the appropriate package for your OS.
    
    4.     Accept the License Agreement.
    
    5.     Run the installation program with default configurations. 

### Downloading of the Bluetooth Protocol Stack

1. Connect the RAK815 SWD interface (refer to the [**datasheet**](https://downloads.rakwireless.com/en/LoRa/RAK815/Hardware%20Specification/RAK815%28RAK813%20BreakBoard%29%20Datasheet%20V1.1.pdf)) with the J-Link device SWD interface. Then, connect the J-Link device to the PC through the USB port.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1561179283\/16596\/abcw6riafpixj85hkaij.jpg",
        "mode": "responsive",
        "width": 477,
        "height": 359,
        "caption": "Figure 4. RAK815 Breakout Board connected to J-TAG Debugger"
    }
}]$

    2.    Open the nRFgo Studio Tool, then select "nRF5X Programming" under the Device Manager.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1561960732\/16596\/nm6m66u1vif1gehbjdzf.jpg",
        "mode": "responsive",
        "width": 1236,
        "height": 791,
        "caption": "Figure 5. nRF5x Programming in nRFgo Studio Tool"
    }
}]$

    3.    Click "Erase all" and select the "Program SoftDevice".

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1561179438\/16596\/luji8jodxrb48k5t68hh.jpg",
        "mode": "responsive",
        "width": 1259,
        "height": 806,
        "caption": "Figure 6. Erasing all and Program SoftDevice Function"
    }
}]$

    4.    Browse the Bluetooth protocol stack file from the open source code through this directory: `RAK813-Breakboard-master>>nRFLib>>components>>softdevice>>s132>>hex`

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1561963823\/16596\/bthombhptbln7i01cv5y.jpg",
        "mode": "responsive",
        "width": 784,
        "height": 380,
        "caption": "Figure 7. Bluetooth Protocol Stack Directory"
    }
}]$

    5.    And click "Program" to complete the download.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1561375197\/16596\/vkzkbvgg9lk00prsk2h5.jpg",
        "mode": "responsive",
        "width": 1259,
        "height": 806,
        "caption": "Figure 8. Browsing Stack File and Clicking Program"
    }
}]$

## Downloading the Application Code

There are three ways to download your application code into your device: **nRFgo Studio Tool**, **Keil Compiler** and **IAR compiler**.

### Using nRFgo Studio Tool

- After completing the Bluetooth protocol station, click the "Program Application".

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1561964210\/16596\/sndodsrhedylsqn3e62l.jpg",
        "mode": "responsive",
        "width": 1252,
        "height": 563,
        "caption": "Figure 9. Downloading Program Application"
    }
}]$

- Browse for the application code and click "Program". Sample programs are made available in the open source code, follow this directory: `RAK813-BreakBoard-master>>Doc>>hex`

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1561964862\/16596\/fojw7oe833otyqips63s.jpg",
        "mode": "responsive",
        "width": 812,
        "height": 380,
        "caption": "Figure 10. Application Demo Location"
    }
}]$

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1561375485\/16596\/tehzelqukvncyr9sncxt.jpg",
        "mode": "responsive",
        "width": 833,
        "height": 538,
        "caption": "Figure 11. Browsing Application and Clici"
    }
}]$

### Using Keil Compiler

- Download and Install the latest version of Keil Compiler through the [Keil Website](http://www.keil.com/).

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1561375751\/16596\/gxhry7i6dm4yjkjhz2ia.jpg",
        "mode": "responsive",
        "width": 1269,
        "height": 503,
        "caption": "Figure 12. ARM KEIL Homepage"
    }
}]$

$plugin[{
    "type": "callout",
    "data": {
        "text": "The best version of Keil Compiler is version 5.5 or above. If your installed Keil compiler supports nRF52832 environment, then it is not necessary to install the nRF52832 environment.",
        "type": "info",
        "title": "Note!"
    }
}]$

- Install the nRF52832 compiler environment for Keil5 from our repository:  `RAK813-Breakboard-master>>Keil5`

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1561965382\/16596\/zaybjvk0orhdptwzkgyl.jpg",
        "mode": "responsive",
        "width": 777,
        "height": 382,
        "caption": "Figure 13. Compiler Environment for Keil5 Directory"
    }
}]$

- After installing it, you can see the Nordic chip information from Options -> Device.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1561378278\/16596\/dqsnawy68huxtjappnex.jpg",
        "mode": "responsive",
        "width": 590,
        "height": 442,
        "caption": "Figure 14. Selecting the Nordic Chip Information"
    }
}]$

- Use the J-Link device to connect your RAK815 and PC, then write your project. You can open sample projects available in this directory: `RAK813-BreakBoard-master>>Keil5`

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1561966046\/16596\/sf0wcfnlzrzflqcujnf3.jpg",
        "mode": "responsive",
        "width": 777,
        "height": 382,
        "caption": "Figure 15. Project Sample Location"
    }
}]$

- Click "Build", then "Download" to download your application code. 

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1561379643\/16596\/lw2qcyrsxedmeuusun3u.jpg",
        "mode": "responsive",
        "width": 1636,
        "height": 978,
        "caption": "Figure 16. Building and Downloading the Application Code"
    }
}]$

If you choose to “Create HEX file” in the Keil tool's options then you can see the HEX
file in Keil's output directory. This file can also be used by nRFgo Stdio Tool.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1561966203\/16596\/ll98g23veduwnyyhfcdm.jpg",
        "mode": "responsive",
        "width": 858,
        "height": 639,
        "caption": "Figure 17. Allowing HEX Files in KEIL5"
    }
}]$

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1561966258\/16596\/lbe2tftradbhb4fwtt1v.jpg",
        "mode": "responsive",
        "width": 1246,
        "height": 432,
        "caption": "Figure 18. Sample Hex File Location"
    }
}]$

### Using IAR Compiler

The writing of programs using IAR Compiler has the same steps with the Keil Compiler with different tools but the same functions.

- First, download and Install the latest version of IAR Compiler through the [IAR Website](https://www.iar.com/).
- Open the IAR project and click "Make" menu. 

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1561790776\/16596\/p2tjgrad3qzhwnamvnkp.png",
        "mode": "responsive",
        "width": 921,
        "height": 715,
        "caption": "Figure 19. Make Tool in IAR Compiler"
    }
}]$

- Then, click the "Project" menu and select the download directory in the "Download Activities Application" option to complete the download.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1561790689\/16596\/bwqd0plo9iti4fe13drg.png",
        "mode": "responsive",
        "width": 633,
        "height": 747,
        "caption": "Figure 20. Downloading Application Code to the Device"
    }
}]$

If you choose to export the HEX file in the IAR options menu, you can also see the
HEX file in the IAR output folder. This file can also be used by nRFgo Stdio Tool.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1561966880\/16596\/hskkfrvitfkuqzrvzqmh.jpg",
        "mode": "responsive",
        "width": 816,
        "height": 708,
        "caption": "Figure 21. Allowing HEX File Exports in IAR"
    }
}]$

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1561966909\/16596\/orma5kb2mr68rrzvp2mb.jpg",
        "mode": "responsive",
        "width": 1246,
        "height": 432,
        "caption": "Figure 22. Sample Hex File Directory"
    }
}]$

Now, you have completed your firmware setup. Up next will be the configuration of your LoRaWAN settings.

