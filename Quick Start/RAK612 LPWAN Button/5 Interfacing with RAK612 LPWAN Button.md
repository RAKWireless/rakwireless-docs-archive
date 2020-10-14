---
type: page
title: Interfacing with RAK612 LPWAN Button
listed: true
slug: interfacing-with-rak612-lora-button
---published

In order for you to be able to interface with the RAK612 LPWAN Button with your Windows Machine, you need to download the RAK Serial Port Tool **[here](https://downloads.rakwireless.com/en/LoRa/Tools/RAK_SERIAL_PORT_TOOL_V1.2.1.zip).**

- Using a standard **Micro - USB Cable**, connect your RAK612 LPWAN Button to your computer.

$plugin[{
    "type": "callout",
    "data": {
        "text": "If this is your first time to connect your RAK612 LPWAN Button to your computer, it should automatically download the CH340 driver in order for them to communicate properly. Make sure to have an internet access if you want such automatic installation to be successful. If such process fails, re-plug your Micro - USB cord and proceed to the next step.",
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
        "caption": "**Figure 1**: Missing Driver for theRAK612 LPWAN Button"
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

- Wait for it to automatically download and install the missing driver. Once installation is done, "**USB-SERIAL CH340**" must appear in the **Ports (COM & LPT)** drop down list. Take note of the COM Port associated with the driver as it will be used in the succeeding steps. For this sample process, the COM Port used by the USB-SERIAL CH340 driver is **COM4**.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1579788881\/24933\/tfl6jmjcsapgpmagthvj.png",
        "mode": "responsive",
        "width": 1370,
        "height": 939,
        "caption": "**Figure 3**: USB-SERIAL CH340 Driver Successfully Installed"
    }
}]$

$plugin[{
    "type": "callout",
    "data": {
        "text": "In case the driver is still not installed upon doing the previous steps, kindly download the driver manually through this [link](https:\/\/downloads.rakwireless.com\/en\/LoRa\/RAK811\/Tools\/).",
        "type": "info",
        "title": "Note:"
    }
}]$

- Let us now test if your RAK612 LPWAN Button can now communicate with the RAK Serial Port Tool. Connect with the RAK Serial Port Tool using the parameters listed below and click "**Open**".

1. **COM**: Choose the COMPort associated with the USB-SERIAL CH340 from the previous step. For this tutorial, the COM Port is COM4.
2. **Baud Rate**: **115200** bps

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1579790106\/24933\/q5ubbty2twyeocvnmttc.png",
        "mode": "responsive",
        "width": 1377,
        "height": 899,
        "caption": "**Figure 4**: Connecting to the RAK Serial Port Tool"
    }
}]$

- To verify connectivity, let's try sending AT+Commands. In the RAK Serial Port Tool, there are built-in AT+Commands within it at the right side. Try sending the code below to check the firmware version of your RAK612 LPWAN Button. If connection is successful, in the monitor panel at the left, the firmware version should appear same with the image shown below:

$plugin[{
    "type": "code-block",
    "data": {
        "languageBlocks": [
            {
                "code": "at+version",
                "language": "none"
            }
        ]
    }
}]$

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1579790473\/24933\/px93o4onb4kxmiwvsumf.png",
        "mode": "responsive",
        "width": 1375,
        "height": 900,
        "caption": "**Figure 5**: AT+Command Sample Serial Communication Test"
    }
}]$

Congratulations! You have just successfully interfaced your RAK612 LPWAN Button with your computer! Go on to the next documentations to fully configure your RAK612 LPWAN Button.

