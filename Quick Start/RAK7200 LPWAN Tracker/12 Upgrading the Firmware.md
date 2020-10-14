---
type: page
title: Upgrading the Firmware
listed: true
slug: upgrading-the-firmware
---published

If the firmware version of your **RAK7200 LPWAN Tracker** is newer than V3.0.0.0 or you have just burned the bootloader into the board according to the **Burning the Bootloader** section, proceed to Step 2.

1.In case you have not just burned the bootloader, as instructed in the previous section you need to manually go into **boot mode**. Open and download the [RAK Serial Port Tool](https://downloads.rakwireless.com/en/LoRa/WisTrio-LoRa-RAK5205/Tools/RAK_SERIAL_PORT_TOOL_V1.2.1.zip). Connect your board via the USB interface and enter the following **AT command**

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
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1579617165\/18272\/ztbivhcsnzfbso1czs4r.jpg",
        "mode": "responsive",
        "width": 2271,
        "height": 1482,
        "caption": "**Figure 1:** Entering Boot Mode"
    }
}]$

2.Download the **RAK Upgrade Tool** from the RAKwireless website [here](https://downloads.rakwireless.com/en/LoRa/RAK612-LoRaButton/Tools/RAK%20LoRaButton%20Upgrade%20Tool%20V1.0.zip) then, open the tool. Again, don't forget to choose the correct port! Open the [auto$](/rak7200-lora-tracker/interfacing-with-rak7200-lora---tracker) to know the appropriate COM Port used.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1579617188\/18272\/wgif92xy3kpypvwj78p2.jpg",
        "mode": "600",
        "width": 1481,
        "height": 1233,
        "caption": "**Figure 2:** RAK Upgrade Tool"
    }
}]$

3.Download the latest RAK7200 Firmware **[here](https://downloads.rakwireless.com/en/LoRa/RAK7200-Tracker/Firmware/)**. Click “**Choose File**” and choose the firmware you have just downloaded. Make sure you choose the one for your particular band:

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1579617204\/18272\/s1dr3hct65lnxow3cequ.jpg",
        "mode": "600",
        "width": 1481,
        "height": 1233,
        "caption": "**Figure 3:** Choosing the Correct Firmware file"
    }
}]$

4.Click “**Start**” to upload the Firmware, this may take a minute:

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1579617229\/18272\/vx4irgqjudaszyizfebc.jpg",
        "mode": "600",
        "width": 1478,
        "height": 1236,
        "caption": "**Figure 4 :** Firmware Upgrading in Process"
    }
}]$

5.You should see something like the image in **Figure 5**, if everything went well.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1579617245\/18272\/ocithbe0at1h3augu9yo.jpg",
        "mode": "600",
        "width": 1481,
        "height": 1228,
        "caption": "**Figure 5:**  Successfully Upgraded Firmware"
    }
}]$

6.Now, **CLOSE** the upgrade tool and **and proceed to the next section.**

### Testing the Installed Firmware

7.In order for you to check if you have successfully installed the firmware on your RAK7200 LPWAN Tracker, open the Serial Port tool again. Press the "Reset button" or type the command below. If everything works  perfectly, you should see the following message below:

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
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1579617326\/18272\/rbw7qdu20f4yybdks7di.jpg",
        "mode": "responsive",
        "width": 2270,
        "height": 1475,
        "caption": "**Figure 6:**  Restarting your Device"
    }
}]$

This information means that you have uploaded the Firmware successfully!

You can also configure your RAK7200 LPWAN Tracker Board using the available AT Commands listed in the [auto$](/rak7200-lora-tracker/configuring-the-rak7200-lora-tracker-using-at-commands)[ ](https://doc.rakwireless.com/rak7200-lora---tracker/configuring-the-rak7200-lora-tracker-using-at-commands)section.

