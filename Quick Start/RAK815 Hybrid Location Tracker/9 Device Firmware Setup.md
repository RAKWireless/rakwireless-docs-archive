---
type: page
title: Device Firmware Setup
listed: true
slug: device-firmware-setup
---published

## Accessing the Open Source Directory

The RAK815 Hybrid Location Tracker is an open source hardware where users can get all the information about the product. It includes schematic diagrams, program codes and other references which could be helpful in building your RAK815 projects. 

This open source project is based on the official code LoRaWAN® 1.0.2 and Nordic
nRF5 SDK 14.0.0, modified to support IAR8.11 and Keil5 Compiler. 

- To start with, download the files in this open source **[directory](https://github.com/RAKWireless/RAK813-BreakBoard).**

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1579659622\/16596\/fdvt15m32vf7w1ioygzi.jpg",
        "mode": "responsive",
        "width": 1252,
        "height": 622,
        "caption": "**Figure 1:** Open Source Directory for RAK815"
    }
}]$

## Downloading the Firmware

To enable the Bluetooth functionality of our device, you must first write the Bluetooth protocol stack using the official nRFgo Studio Tool. 

- Download and Install the nRFgo Studio Tool through the **[Nordic Official Site](http://www.nordicsemi.com/Products/Low-power-short-range-wireless/nRF52832)** or through this **[link](https://downloads.rakwireless.com/en/LoRa/RAK815/Tools/)**.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1579659629\/16596\/cfvozry3umjio0tty9wj.jpg",
        "mode": "responsive",
        "width": 1100,
        "height": 420,
        "caption": "**Figure 2:** nRFgo Studio tool Installer"
    }
}]$

### Installing of the J-Link Driver

1. Navigate to this **[J-Link Site](https://www.segger.com/downloads/jlink).**
2. Click  the “**Click for downloads**” under “**J-Link Software and Documentation Pack**”.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1579659649\/16596\/gig3jnaqo7wwqebfqz3r.jpg",
        "mode": "responsive",
        "width": 1310,
        "height": 648,
        "caption": "**Figure 3:** Downloading J-Link Software"
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
        "caption": "**Figure 4:** RAK815 Breakout Board connected to J-TAG Debugger"
    }
}]$

    2.    Open the nRFgo Studio Tool, then select "nRF5X Programming" under the Device Manager.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1579657676\/16596\/dsmeqivou0kghl5bgkcs.jpg",
        "mode": "responsive",
        "width": 1250,
        "height": 805,
        "caption": "**Figure 5:** nRF5x Programming in nRFgo Studio Tool"
    }
}]$

    3.    Click "Erase all" and select the "Program SoftDevice".

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1579657688\/16596\/i2wvwxa2xzliptdddbx6.jpg",
        "mode": "responsive",
        "width": 1273,
        "height": 820,
        "caption": "**Figure 6:** Erasing all and Program SoftDevice Function"
    }
}]$

    4.    Browse the Bluetooth protocol stack file from the open source code through this directory: `RAK813-Breakboard-master>>nRFLib>>components>>softdevice>>s132>>hex`

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1579657695\/16596\/uwuekit0gfov3yoy98td.jpg",
        "mode": "responsive",
        "width": 798,
        "height": 394,
        "caption": "**Figure 7:** Bluetooth Protocol Stack Directory"
    }
}]$

    5.    And click "Program" to complete the download.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1579657706\/16596\/slvyyz3yxrdauzb4unsm.jpg",
        "mode": "responsive",
        "width": 1273,
        "height": 820,
        "caption": "**Figure 8:** Browsing Stack File and Clicking Program"
    }
}]$

## Downloading the Application Code

There are three ways to download your application code into your device: **nRFgo Studio Tool**, **Keil Compiler** and **IAR compiler**.

### Using nRFgo Studio Tool

- After completing the Bluetooth protocol station, click the "**Program Application**".

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1579657715\/16596\/y0dwclqlgofdftxda3vr.jpg",
        "mode": "responsive",
        "width": 1266,
        "height": 577,
        "caption": "**Figure 9:** Downloading Program Application"
    }
}]$

- Browse for the application code and click "**Program**". Sample programs are made available in the open source code, follow this directory: `RAK813-BreakBoard-master>>Doc>>hex`

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1579657727\/16596\/l7j5sojkbfm6ieh5brhx.jpg",
        "mode": "responsive",
        "width": 826,
        "height": 394,
        "caption": "**Figure 10:** Application Demo Location"
    }
}]$

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1579657738\/16596\/ywbhtpkajwlk3gqvpkam.jpg",
        "mode": "responsive",
        "width": 847,
        "height": 552,
        "caption": "**Figure 11:** Browsing Application and Click"
    }
}]$

### Using Keil Compiler

- Download and Install the latest version of Keil Compiler through the [Keil Website](http://www.keil.com/).

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1579657746\/16596\/rupucqotsbqgfu1noty1.jpg",
        "mode": "responsive",
        "width": 1283,
        "height": 517,
        "caption": "**Figure 12:** ARM KEIL Homepage"
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
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1579657754\/16596\/ca6vivfvemxdkjauxmbe.jpg",
        "mode": "responsive",
        "width": 791,
        "height": 396,
        "caption": "**Figure 13:** Compiler Environment for Keil5 Directory"
    }
}]$

- After installing it, you can see the Nordic chip information from Options -> Device.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1579657762\/16596\/ywekpiszifffmyruas3a.jpg",
        "mode": "responsive",
        "width": 604,
        "height": 456,
        "caption": "**Figure 14:** Selecting the Nordic Chip Information"
    }
}]$

- Use the J-Link device to connect your RAK815 and PC, then write your project. You can open sample projects available in this directory: `RAK813-BreakBoard-master>>Keil5`

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1579657771\/16596\/dllsmntcb0gjwhione6y.jpg",
        "mode": "responsive",
        "width": 791,
        "height": 396,
        "caption": "**Figure 15:** Project Sample Location"
    }
}]$

- Click "Build", then "Download" to download your application code. 

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1579657828\/16596\/ybbnse7b39ygaushnycb.jpg",
        "mode": "responsive",
        "width": 1650,
        "height": 992,
        "caption": "**Figure 16:** Building and Downloading the Application Code"
    }
}]$

If you choose to “**Create HEX file**” in the Keil tool's options then you can see the HEX
file in Keil's output directory. This file can also be used by nRFgo Stdio Tool.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1579657798\/16596\/mx3j9jhjjdnezr2u5mju.jpg",
        "mode": "responsive",
        "width": 872,
        "height": 653,
        "caption": "**Figure 17:** Allowing HEX Files in KEIL5"
    }
}]$

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1579657920\/16596\/fx1nso7vfvnrpzkxgzvh.jpg",
        "mode": "responsive",
        "width": 1260,
        "height": 446,
        "caption": "**Figure 18:** Sample Hex File Location"
    }
}]$

### Using IAR Compiler

The writing of programs using IAR Compiler has the same steps with the Keil Compiler with different tools but the same functions.

- First, download and Install the latest version of IAR Compiler through the [IAR Website](https://www.iar.com/).
- Open the IAR project and click "Make" menu. 

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1579657934\/16596\/wakz6mw0fkco6va4labs.png",
        "mode": "responsive",
        "width": 935,
        "height": 729,
        "caption": "**Figure 19:** Make Tool in IAR Compiler"
    }
}]$

- Then, click the "**Project**" menu and select the download directory in the "**Download Activities Application**" option to complete the download.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1579657946\/16596\/gkrn6ev9el4mphrlmotb.png",
        "mode": "responsive",
        "width": 647,
        "height": 761,
        "caption": "**Figure 20:** Downloading Application Code to the Device"
    }
}]$

If you choose to export the HEX file in the IAR options menu, you can also see the
HEX file in the IAR output folder. This file can also be used by nRFgo Stdio Tool.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1579657959\/16596\/nzuqowyolcp2jigjc6vr.jpg",
        "mode": "responsive",
        "width": 830,
        "height": 722,
        "caption": "**Figure 21:** Allowing HEX File Exports in IAR"
    }
}]$

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1579657972\/16596\/nstows3e7mtddnbk0oj2.jpg",
        "mode": "responsive",
        "width": 1260,
        "height": 446,
        "caption": "**Figure 22:** Sample Hex File Directory"
    }
}]$

Now, you have completed your firmware setup. Up next will be the configuration of your LoRaWAN® settings.

