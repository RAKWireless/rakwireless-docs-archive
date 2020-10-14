---
type: page
title: Upgrading the Firmware
listed: true
slug: upgrading-the-firmware
---published

If the firmware version of your RAK811 Breakout Board is newer than V3.0.0.0 or you
have just burned the bootloader into RAK811 Breakout Board according to the Burning Bootloader into the Device document, you just need to burn the upgrade firmware according to the following steps now:

- First, type the command to let the RAK811 Breakout board work in boot mode.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1561800211\/-1\/h61yt8fjhs7ww6sidksg.jpg",
        "mode": "300",
        "width": 531,
        "height": 587,
        "caption": "**Figure 1**: Turning the Boot Mode on"
    }
}]$

- Next, close the serial port tool and download the **RAK Upgrade Tool** from this **[website](https://www.rakwireless.com/en/download/LoRa/RAK612-LoRaButton)**. Then, open the tool.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1561800640\/-1\/aew8v62yg5s019mfzmf1.jpg",
        "mode": "600",
        "width": 729,
        "height": 600,
        "caption": "**Figure 2**: RAK Upgrade Tool"
    }
}]$

- Click “**Choose File**” button to choose the correct upgrade file:

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1561800675\/-1\/fp94jtjzo3f9vczukcxt.jpg",
        "mode": "600",
        "width": 735,
        "height": 606,
        "caption": "**Figure 3**: Choosing the Correct Upgrade file"
    }
}]$

- Click “Start” to upgrade, this may take a minute:

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1561800697\/-1\/kt7vqcuo2l7pcggjv9q9.jpg",
        "mode": "600",
        "width": 727,
        "height": 605,
        "caption": "**Figure 4**: Start Upgrading your Firmware"
    }
}]$

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1561800719\/-1\/iu485yvakkxhhtfq7lfp.jpg",
        "mode": "600",
        "width": 732,
        "height": 599,
        "caption": "**Figure 5**: Successfully Upgraded your Firmware"
    }
}]$

- Now, close the upgrade tool and open a serial port tool. 
- We recommend you to use RAK serial port tool, because there are some ready AT commands in this tool and this will be very useful for you. You can get it from RAK website available for free at this **[RAK directory](http://docs.rakwireless.com/en/LoRa/RAK811/Tools/RAK_SERIAL_PORT_TOOL_V1.%202.1.zip)**.
- Choose the correct **COM port** and set the baud rate to **115200**. Then open the serial port and
enter the AT command `<at+set_config=device:restart>` to restart.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1561800735\/-1\/sfxpgfyf1wamx9dc1sbs.jpg",
        "mode": "300",
        "width": 524,
        "height": 583,
        "caption": "**Figure 6**: Restarting your Firmware"
    }
}]$

Congrats! This information means that you have upgraded successfully the new firmware.

In the next section, you will know how to configure your RAK811 Breakout Board using the available AT commands.

