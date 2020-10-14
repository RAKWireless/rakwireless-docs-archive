---
type: page
title: Upgrading the Firmware
listed: false
slug: upgrading-the-firmware
---published

Before to starting, it is recommended to keep the RAK5010-M module updated to the latest version of the firmware. The latest firmware, manuals, datasheets of the RAK5010-M can be found [here](https://downloads.rakwireless.com/Cellular/RAK5010/).

1.Download the latest compiled firmware from the RAKwireless website [here](https://downloads.rakwireless.com/Cellular/RAK5010/Firmware/RAK5010-M_Latest_Firmware.zip).

2.The firmware file is in a ".**zip**" format. Decompress it to get a file with "**.hex**" extension.

3.Connect the RAK5010-M module with a computer through JTAG as shown in Figure 1.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1595245801\/32193\/c4hyemgb6a93nionvfvv.jpg",
        "mode": "responsive",
        "width": 3292,
        "height": 1520,
        "caption": "**Figure 1**: RAK5010 and PC Connection through JTAG"
    }
}]$

4.Connect the micro USB cable to your PC to supply power to the module or use an external 18650 litium batterry.

5.Install J-Link tool on your computer. You can download the software from the RAKwireless website [here](https://downloads.rakwireless.com/en/Cellular/Tools/).

6.RAKWireless has prepared a set of scripts to simplify the configuration of the J-Flash tool projects. Please download “**RAK itracker flash tool**” from the website [here](https://downloads.rakwireless.com/en/Cellular/Tools/).

7.Decompress the "**.zip**" file, you will get a folder as shown as the Figure 2:

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1595246004\/32193\/j1jl5rguzbvkx6a0ck1v.jpg",
        "mode": "600",
        "width": 747,
        "height": 166,
        "caption": "**Figure 2**: RAK iTracker flash tool folder"
    }
}]$

8.Copy the "**.hex**" file of RAK5010-M from step 2 into the folder shown above. 

9.Rename the firmware file to “**production_final.hex**”.

10.Execute the script “**nrf52840_program.bat**”. The J-Flash tool will start as shown in the Figure 3.

///////// MISSING FIGURE 3

11.On completion of the flashing process, the J-Flash tool will close automatically.

