---
type: page
title: Interfacing with RAK815 Hybrid Location Tracker
listed: true
slug: interfacing-with-rak815-hybrid-location-tracker
---published

In order for you to be able to interface with the RAK815 Hybrid Location Tracker with your Windows Machine, you need to download the [RAK Serial Port Tool](https://downloads.rakwireless.com/en/LoRa/Tools/RAK_SERIAL_PORT_TOOL_V1.2.1.zip).

$plugin[{
    "type": "callout",
    "data": {
        "text": "Before powering the RAK815 Hybrid Location Tracker, you should install the LoRa\u00ae antenna first . Not doing so might damage the board",
        "type": "warning",
        "title": "Warning"
    }
}]$

- Using a standard **Micro - USB Cable**, connect your RAK815 Hybrid Location Tracker to your computer.

$plugin[{
    "type": "callout",
    "data": {
        "text": "If this is your first time to connect your RAK815 Hybrid Location Tracker to your computer, it should automatically download the USB - Serial Port Chip CP2102, in order for them to communicate propperly. Make sure to have an internet access if you want such automatic installation to be successful. If such process fails, re-plug your Micro - USB cord and proceed to the next step.",
        "type": "info",
        "title": "Note:"
    }
}]$

- Go to your **Device Manager** by pressing : **Windows + R** and type `devmgmt.msc` or **search in Start Menu** or right click "**My Computer**" or "**This PC**" and click **Manage**. Look for **Other Devices.**

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1579788425\/24933\/ojnphsuvfgrvwzd4dvu8.png",
        "mode": "responsive",
        "width": 1367,
        "height": 942,
        "caption": "**Figure 1**: Missing Driver for the RAK815 Hybrid Location Tracker"
    }
}]$

- Under "**Other devices**" drop down list, an unknown **USB2.0-Serial** driver must appear. Right click into it and choose "**Search automaticaly for updated driver software**". Again, before doing so, make sure to have an internet access or it will fail.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1579788541\/24933\/ejfeqklgjwmjjky5ewag.png",
        "mode": "responsive",
        "width": 1368,
        "height": 940,
        "caption": "**Figure 2**: Automatic Driver Installation via Internet"
    }
}]$

- Wait for it to automatically download and install the missing driver. Once installation is done, "**Silicon Labs CP210x USB to UART Bridge**" must appear in the **Ports (COM & LPT)** drop down list. Take note of the COM Port associated with the driver as it will be used in the succeeding steps. For this sample process, the COM Port used by the USB - Serial Port Chip CP2102 driver is **COM41**.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1579951199\/24959\/h3yqbz8ztqqelz17ext0.jpg",
        "mode": "responsive",
        "width": 670,
        "height": 116,
        "caption": "**Figure 3**: USB - Serial Port Chip CP2102 Driver Successfully Installed"
    }
}]$

$plugin[{
    "type": "callout",
    "data": {
        "text": "In case the previous measures mentioned beforehand does not install the needed driver, go to the [USB - Serial Port Chip CP2102](https:\/\/www.silabs.com\/products\/development-tools\/software\/usb-to-uart-bridge-vcp-drivers) website to manually download and install it.",
        "type": "info",
        "title": "Note:"
    }
}]$

Congratulations! You have just successfully interfaced your RAK815 Hybrid Location Tracker with your computer!

