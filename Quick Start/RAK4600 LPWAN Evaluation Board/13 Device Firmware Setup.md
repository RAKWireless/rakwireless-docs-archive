---
type: page
title: Device Firmware Setup
listed: true
slug: burning-the-firmware-into-the-device
---published

If you want to get a pre-compiled firmware instead of compiling the source code by yourself, and flash it into RAK4600 through J-Link, you can find the latest firmware on RAK website after it is released **[here](https://downloads.rakwireless.com/en/LoRa/RAK4600/Firmware/)**.

### Installing J-Flash

- Go to the Official Website of **Segger** where you can Download the J-Flash software: [https://www.segger.com/products/debug-probes/j-link/tools/j-flash/about-j-flash/](https://www.segger.com/products/debug-probes/j-link/tools/j-flash/about-j-flash/)

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1580197958\/22594\/chigugx8lnw5xc1xi3bv.jpg",
        "mode": "responsive",
        "width": 1362,
        "height": 651,
        "caption": "**Figure 1:** Segger Official Website"
    }
}]$

- Download the software that corresponds to your Operating System, in this guide we will be using Windows OS.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1580198007\/22594\/rr1yopbrhjw2xmpmiwue.jpg",
        "mode": "responsive",
        "width": 1365,
        "height": 648,
        "caption": "**Figure 2:** J-link Software in different platforms"
    }
}]$

- After you have downloaded the corresponding software for your machine, install it and wait for a couple of minutes.

### Creating Project in J-Flash

- Upon opening the software, you will be greeted with the following window. Choose Create a new project. Then Click Start J-Flash.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1580198432\/22594\/zaeihbaoq4cbnf4dt2zd.jpg",
        "mode": "responsive",
        "width": 927,
        "height": 717,
        "caption": "**Figure 3:** J-flash Interface"
    }
}]$

- You will be then prompt to configure your new Project. Select the Target Device by clicking the box labeled red below:

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1580198454\/22594\/djbvyzwlbgn1j2mrif96.jpg",
        "mode": "responsive",
        "width": 931,
        "height": 716,
        "caption": "**Figure 4:** Configuring the Project"
    }
}]$

- Select the Manufacturer to **Nordic Semi** and Select the Device **nRF52832_XXAA.**

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1580221015\/22594\/fzxezoootvevolfb4igi.png",
        "mode": "responsive",
        "width": 770,
        "height": 512,
        "caption": "**Figure 5:** Selecting the Device"
    }
}]$

- Select the Target Interface to be **SWD** and the Speed (kHz) to be **4000** and Press OK.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1580221071\/22594\/mhddralkqejjxg4rytjc.png",
        "mode": "responsive",
        "width": 928,
        "height": 717,
        "caption": "**Figure 6:** Target Interface and Speed (kHz)"
    }
}]$

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1580221221\/22594\/r54lhlakju7kxoytqmsx.png",
        "mode": "responsive",
        "width": 930,
        "height": 717,
        "caption": "**Figure 7:** Project Created Successfully"
    }
}]$

### [Connecting the RAK4600 LPWAN Evaluation Board with JTAG](https://doc.rakwireless.com/rak4260-lora---evaluation-board/burning-the-firmware#connecting-the-rak4260-lora-evaluation-board-with-jtag)

- Connect the RAK4600 LPWAN Evaluation Board with your J-Link in your PC through JTAG (refer to the Figure Below)

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1580179731\/22594\/iouectenf1oll8kwx76z.png",
        "mode": "responsive",
        "width": 6170,
        "height": 3114,
        "caption": null
    }
}]$

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1580131548\/22594\/ynx1rtolamjddsqrhzft.png",
        "mode": "responsive",
        "width": 4041,
        "height": 1633,
        "caption": "**Figure 8**: RAK4600 to Windows PC connection thru JTAG"
    }
}]$

- In the J-Flash software Menu Bar, Choose Target -> Connect

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1580223385\/22594\/grfidkobx8jqno7d4grc.png",
        "mode": "responsive",
        "width": 930,
        "height": 717,
        "caption": "**Figure 10:** Connect to the RAK4260"
    }
}]$

- If everything works properly, it will prompt "Connected Successfully" indicating that you have successfully connected the RAK4600 with J-Link.
- Now, choose the demo firmware (.hex) that you have downloaded and extracted.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1580222747\/22594\/afc3lsreloedocidbfjy.png",
        "mode": "responsive",
        "width": 930,
        "height": 717,
        "caption": "**Figure 11:** Choosing the Firmware"
    }
}]$

- After you choose the firmware, select **Target -> Production Programming**  or Press F7 to start the flashing process and wait for a couple of minutes.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1580223317\/22594\/zqmxlrkxu4f3siwxn6pd.png",
        "mode": "responsive",
        "width": 930,
        "height": 717,
        "caption": "**Figure 12:** Burning the Firmware"
    }
}]$

