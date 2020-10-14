---
type: page
title: Upgrading the Firmware
listed: true
slug: upgrading-the-firmware
---published

If the firmware version of your **RAK811 WisNode LoRa Module** is newer than V3.0.0.0 or you have just burned the bootloader into RAK811 Breakout Board according to the **Burning Bootloader into the Device** section, proceed to Step 2.

1.In case you have not just burned the bootloader, as instructed in the previous section you need to manually go into **boot mode**. Connect you board via the USB interface and enter the following **AT command** after you have connected via the proper COM port:

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
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1562143058\/17278\/ghvkvpesyeycpvuko2pe.jpg",
        "mode": "responsive",
        "width": 531,
        "height": 587,
        "caption": "**Figure 1.** Entering Boot Mode"
    }
}]$

2.Download the **RAK Upgrade Tool** from the RAKwireless website **[here](https://downloads.rakwireless.com/en/LoRa/RAK612-LoRaButton/Tools/RAK%20LoRaButton%20Upgrade%20Tool%20V1.0.zip)**. Then, open the tool. Again don't forget to choose the correct port!

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1562143557\/17278\/mmfs8uhrv2e1uhhjop73.jpg",
        "mode": "responsive",
        "width": 729,
        "height": 600,
        "caption": "**Figure 2.** RAK Upgrade Tool"
    }
}]$

3.Click “**Choose File**” and choose the firmware you have downloaded for your desired frequency band.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1562143691\/17278\/p7kx1astp9oudsekskyx.jpg",
        "mode": "responsive",
        "width": 735,
        "height": 606,
        "caption": "**Figure 3.** Choosing the Correct Upgrade file"
    }
}]$

4.Click “**Start**” to upgrade, this may take a minute:

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1562143784\/17278\/l4cyh7w2zlhnfdxjrqs9.jpg",
        "mode": "responsive",
        "width": 727,
        "height": 605,
        "caption": "**Figure 4.** Firmware Upgrading in Process"
    }
}]$

5.You should see something like the image in Figure 5, if everything went well.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1562143826\/17278\/jzv8nr7gphakutif3tre.jpg",
        "mode": "responsive",
        "width": 732,
        "height": 599,
        "caption": "**Figure 5.** Successfully Upgraded Firmware"
    }
}]$

6.Now, **CLOSE** the upgrade tool and **OPEN** the serial port too, again.

7.Choose the correct **COM port** and set the baud rate to **115200**. Then open the serial port and enter the AT command shown below to restart. Another option is to press the **RST** button on the RAK811 WisNode LoRa module. 

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
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1562144412\/17278\/zguheugha73jhtl9lm63.jpg",
        "mode": "responsive",
        "width": 424,
        "height": 302,
        "caption": "**Figure 6.** Restarting your Device"
    }
}]$

This information means that you have uploaded the Firmware successfully!

In the next section, you will learn how to **configure** your RAK811 WisNode LoRa Board using the available **AT commands**.

