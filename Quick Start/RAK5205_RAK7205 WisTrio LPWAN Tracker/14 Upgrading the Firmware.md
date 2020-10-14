---
type: page
title: Upgrading the Firmware
listed: true
slug: burning-the-firmware-into-the-device
---published

If the firmware version of your RAK5205 WisTrio LPWAN Tracker is newer than V3.0.0.0 or you have just burned the bootloader into RAK5205 WisTrio LPWAN Tracker according to the Burning Bootloader into the Device section, you just need to burn the upgrade firmware according to the following steps now:

- First, type the command to let the RAK5205 WisTrio LPWAN Tracker work in boot mode.

$plugin[{
    "type": "callout",
    "data": {
        "text": "If you have just burned the bootloader by\nyourself according to the section 2, it works in boot mode now. If the current version of\nthe RAK5205\u2019s firmware is newer than V3.0.0.0, you need to set an AT command\n to let it work in boot mode",
        "type": "info",
        "title": "Note"
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
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1570810267\/20613\/ak6dmrbeykbyxktghplr.jpg",
        "mode": "300",
        "width": 485,
        "height": 543,
        "caption": "**Figure 1**: Turning the Boot Mode on"
    }
}]$

- Next, close the serial port tool and download the **RAK Upgrade Tool** from this **[website](https://downloads.rakwireless.com/en/LoRa/RAK612-LoRaButton/Tools/RAK%20LoRaButton%20Upgrade%20Tool%20V1.0.zip)**. Then, extract and open the tool.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1570810341\/20613\/bhnagxk2lyikpa1rqpmd.jpg",
        "mode": "responsive",
        "width": 729,
        "height": 600,
        "caption": "**Figure 2**: RAK Upgrade Tool"
    }
}]$

- Click “**Choose File**” button to choose the correct upgrade file:

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1570810554\/20613\/xy32xtmb8urj28pk1cr0.jpg",
        "mode": "responsive",
        "width": 736,
        "height": 602,
        "caption": "**Figure 3**: Choosing the Correct Upgrade file"
    }
}]$

- Click “**Start**” to upgrade, this may take a minute:

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1570810459\/20613\/nbn7qmum5do7ivvvva3m.jpg",
        "mode": "responsive",
        "width": 732,
        "height": 608,
        "caption": "**Figure 4**: Start Upgrading your Firmware"
    }
}]$

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1570810559\/20613\/eprjekj8xxk77om7vbw3.jpg",
        "mode": "responsive",
        "width": 730,
        "height": 598,
        "caption": "**Figure 5**: Successfully Upgraded your Firmware"
    }
}]$

- Now, close the upgrade tool and open a serial port tool.
- We recommend you to use RAK serial port tool, because there are some ready AT commands in this tool and this will be very useful for you. You can get it from RAK website available for free at this[**RAK directory**](https://downloads.rakwireless.com/en/LoRa/RAK811/Tools/RAK_SERIAL_PORT_TOOL_V1.2.1.zip).
- Choose the correct **COM port** and set the baud rate to **115200**. Then open the serial port and enter the AT command  to restart.

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
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1570810655\/20613\/nrnvbjsxvodttrumo7x9.jpg",
        "mode": "300",
        "width": 468,
        "height": 568,
        "caption": "**Figure 6**: Restarting your Firmware"
    }
}]$

**Congratulation**! This information means that you have upgraded successfully the new firmware.

