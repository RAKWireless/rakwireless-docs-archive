---
type: page
title: Upgrading the Firmware
listed: true
slug: upgrading-the-firmware
---published

### Burning the Bootloader

If the firmware version of your **RAK7200 LoRa Tracker** is newer than V3.0.0.0 or you have just burned the bootloader into the board according to the **Burning Bootloader** section, proceed to Step 2.

1.In case you have not just burned the bootloader, as instructed in the previous section you need to manually go into **boot mode**. Connect you board via the USB interface and enter the following **AT command** after you have connected via the Serial Tool via the proper COM port (tool download [here](https://downloads.rakwireless.com/en/LoRa/WisTrio-LoRa-RAK5205/Tools/RAK_SERIAL_PORT_TOOL_V1.2.1.zip)):

$plugin[{
    "type": "code-block",
    "data": {
        "languageBlocks": [
            {
                "code": "at+set_config=device:boot",
                "language": "javascript"
            }
        ]
    }
}]$

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1564794814\/18272\/bzzfo3x2ge11mnsvkkax.jpg",
        "mode": "responsive",
        "width": 2257,
        "height": 1468,
        "caption": "**Figure 1.** Entering Boot Mode"
    }
}]$

2.Download the **RAK Upgrade Tool** from the RAKwireless website **[here](https://downloads.rakwireless.com/en/LoRa/RAK612-LoRaButton/Tools/RAK%20LoRaButton%20Upgrade%20Tool%20V1.0.zip)**. Then, open the tool. Again don't forget to choose the correct port!

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1564795147\/18272\/dyrp6lcnweitrpf3c3o4.jpg",
        "mode": "responsive",
        "width": 1467,
        "height": 1219,
        "caption": "**Figure 2.** RAK Upgrade Tool"
    }
}]$

3.Download the latest RAK7200 Firmware **[here](https://downloads.rakwireless.com/en/LoRa/RAK7200-Tracker/Firmware/)**. Click “**Choose File**” and choose the firmware you have just downloaded. Make sure you choose the one for your particular band:

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1564795214\/18272\/wqzl1cgbialecmhno3ic.jpg",
        "mode": "responsive",
        "width": 1467,
        "height": 1219,
        "caption": "**Figure 3.** Choosing the Correct Firmware file"
    }
}]$

4.Click “**Start**” to upload the Firmware, this may take a minute:

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1564795611\/18272\/sg6xevdjzccuie6zouhl.jpg",
        "mode": "responsive",
        "width": 1464,
        "height": 1222,
        "caption": "**Figure 4.** Firmware Upgrading in Process"
    }
}]$

5.You should see something like the image in Figure 5, if everything went well.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1564795833\/18272\/xcpglryk835ntw3womq8.jpg",
        "mode": "responsive",
        "width": 1467,
        "height": 1214,
        "caption": "**Figure 5.** Successfully Upgraded Firmware"
    }
}]$

6.Now, **CLOSE** the upgrade tool and **and proceed to the next section.**

### Testing the Installed Firmware

7.In order for you to check if you have successfully installed the firmware on your RAK7200 LoRa Tracker, open a Serial Port tool again.  Press the "Reset button" or type the command below. You should see the message in Figure 6:

$plugin[{
    "type": "code-block",
    "data": {
        "languageBlocks": [
            {
                "code": "at+set_config=device:restart",
                "language": "javascript"
            }
        ]
    }
}]$

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1564796710\/18272\/csaq7yantp0afavendju.jpg",
        "mode": "responsive",
        "width": 2256,
        "height": 1461,
        "caption": "**Figure 6.** Restarting your Device"
    }
}]$

This information means that you have uploaded the Firmware successfully!

In the next section, you will learn how to **configure** your RAK7200 LoRa Tracker Board using the available **AT commands**.

