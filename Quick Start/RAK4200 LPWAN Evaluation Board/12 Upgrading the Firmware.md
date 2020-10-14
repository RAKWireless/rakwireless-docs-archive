---
type: page
title: Upgrading the Firmware
listed: true
slug: upgrading-the-firmware
---published

The following steps show you how to update the firmware for RAK4200 LPWAN Module connected to the Baseboard.

**1.** Download and install the software needed in your PC:

- [RAK Serial Port Tool](https://downloads.rakwireless.com/en/LoRa/Tools/RAK_SERIAL_PORT_TOOL_V1.2.1.zip)
- [RAK Firmware Upgrade Tool](https://downloads.rakwireless.com/en/LoRa/Tools/RAK_Upgrade_Tool_V1.0.rar)
- [RAK4200 Firmware](https://downloads.rakwireless.com/en/LoRa/RAK4200/Firmware/RAK4200_V3.2.0.12.rar)

**2.** Connect your RAK4200 LPWAN Breakout Module into your windows machine as instructed in the [auto$](/rak4200-lora-evaluation-board/interfacing-with-rak4200-lora-evaluation-board).

**3.** Open the RAK Serial Port Tool you have just installed and let RAK4200 work in boot mode by setting an AT command through serial port as follows: 

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
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1579532606\/24032\/hdtvmsxeqpzo2tx53a2x.jpg",
        "mode": "responsive",
        "width": 545,
        "height": 601,
        "caption": "**Figure 1:** Entering Boot Mode"
    }
}]$

**4.** Close RAK serial port tool and open RAK firmware upgrade tool on your PC. Make sure to choose the correct COM Port.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1579532612\/24032\/uq2mchzjcptfhpiem4p0.jpg",
        "mode": "responsive",
        "width": 743,
        "height": 614,
        "caption": "**Figure 2:** RAK Firmware Upgrade Tool"
    }
}]$

**5.** Click “**Choose File**” button to choose a correct upgrade file:

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1579532618\/24032\/qaxfg8sllput33ycskaq.jpg",
        "mode": "responsive",
        "width": 741,
        "height": 617,
        "caption": "**Figure 3:** Choosing the Correct Upgrade file"
    }
}]$

**6**. Click “**Start**” to upgrade, this may take a minute:

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1579532627\/24032\/dzctnumbclyzrawjf6kl.jpg",
        "mode": "responsive",
        "width": 727,
        "height": 601,
        "caption": "**Figure 4:** Firmware Upgrading in Process"
    }
}]$

**7.** You should see something like the image below if everything went well.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1579532633\/24032\/xrtlzi2q6cht8tfkn9kr.jpg",
        "mode": "responsive",
        "width": 734,
        "height": 614,
        "caption": "**Figure 5:** Successfully Upgraded Firmware"
    }
}]$

**8.** CLOSE the Firmware Upgrade Tool and OPEN the RAK Serial Port Tool again.

**9.** Choose the correct **COM port** and set the baud rate to **115200**. Then open the serial port and enter the AT command shown below to restart.

$plugin[{
    "type": "code-block",
    "data": {
        "languageBlocks": [
            {
                "code": "at+set_config=device:restart",
                "language": "none"
            }
        ]
    }
}]$

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1579532637\/24032\/xgkhng5xr1tg4prxnbuq.jpg",
        "mode": "responsive",
        "width": 561,
        "height": 669,
        "caption": "**Figure 6:** Restarting your Device"
    }
}]$

This information means that you have uploaded the Firmware successfully!

