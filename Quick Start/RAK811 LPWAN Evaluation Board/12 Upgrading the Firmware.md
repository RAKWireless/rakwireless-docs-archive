---
type: page
title: Upgrading the Firmware
listed: true
slug: upgrading-the-firmware
---published

If the firmware version of your RAK811 LPWAN Evaluation Board is newer than V3.0.0.0 or you have just burned the bootloader into RAK811 LPWAN Evaluation Board according to the [Burning Bootloader into the Device](https://doc.rakwireless.com/rak811-lora---evaluation-board/burning-the-bootloader-into-the-device) document, proceed to **Step 2**. 

1.In case you have not just burned the bootloader as instructed in the previous section, you need to manually go into **boot mode**. Connect you board via the USB interface and enter the following **AT command** after you have connected via the proper COM port:

$plugin[{
    "type": "callout",
    "data": {
        "text": "Make sure to choose the correct port in the COM Port field. You can check this in the [auto$](\/rak811-lora-evaluation-board\/interfacing-with-rak811-lora-evaluation-board) document.",
        "type": "info",
        "title": "Note:"
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
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1579529640\/17278\/vbshextj0q190mzk6hhf.jpg",
        "mode": "responsive",
        "width": 545,
        "height": 601,
        "caption": "**Figure 1:** Entering Boot Mode"
    }
}]$

2.Download the **RAK Upgrade Tool** from the RAKwireless website **[here](https://downloads.rakwireless.com/en/LoRa/RAK612-LoRaButton/Tools/RAK%20LoRaButton%20Upgrade%20Tool%20V1.0.zip)**. Then, open the tool. Again don't forget to choose the correct port! 

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1579529698\/17278\/e9ratal5kgle1mwh4ufu.png",
        "mode": "responsive",
        "width": 902,
        "height": 750,
        "caption": "**Figure 2:** RAK Upgrade Tool"
    }
}]$

3.Click “**Choose File**” and choose the firmware you have downloaded for your desired frequency band.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1579529756\/17278\/nguqg8huem2urdte26ub.png",
        "mode": "responsive",
        "width": 901,
        "height": 750,
        "caption": "**Figure 3:** Choosing the Correct Upgrade file"
    }
}]$

4.Click “**Start**” to upgrade, this may take a minute:

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1579530023\/17278\/wjdxnmvu2bwkjfj2rgmd.png",
        "mode": "responsive",
        "width": 902,
        "height": 751,
        "caption": "**Figure 4:** Firmware Upgrading in Process"
    }
}]$

5.You should see something like the image in **Figure 5**, if everything went well.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1579530538\/17278\/e7dcwivj7lv7zupcekok.jpg",
        "mode": "600",
        "width": 746,
        "height": 613,
        "caption": "**Figure 5:** Successfully Upgraded Firmware"
    }
}]$

6.Now, **CLOSE** the upgrade tool and **OPEN** the serial port too, again.

7.Choose the correct **COM port** and set the baud rate to **115200**. Then open the serial port and enter the AT command shown below to restart. Another option is to press the **RST** button on the RAK811 LPWAN Evaluation Board. 

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
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1579530583\/17278\/x0fsjpi4xc4hmatdcmyk.jpg",
        "mode": "responsive",
        "width": 438,
        "height": 316,
        "caption": "**Figure 6:** Restarting your Device"
    }
}]$

This information means that you have uploaded the Firmware successfully!

If you want to configure your RAK811 LPWAN Evaluation Board using the available **AT commands**, check the [auto$](/rak811-lora-evaluation-board/configuring-your-rak811-evaluation-board) document.

