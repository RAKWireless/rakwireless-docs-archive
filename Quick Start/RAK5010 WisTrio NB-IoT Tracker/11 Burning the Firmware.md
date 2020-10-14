---
type: page
title: Burning the Firmware
listed: true
slug: burning-the-firmware
---published

An easy and quick way to get started with your RAK5010 is through using a pre-compiled firmware.  However, if you wanted to compile your own customized firmware, you can visit [auto$](/rak5010-wistrio-nb-iot-tracker/rui-online-compiler)

### Installing J-Flash

- Go to the Official Website of **Segger** where you can Download the J-Flash software: [https://www.segger.com/products/debug-probes/j-link/tools/j-flash/about-j-flash/](https://www.segger.com/products/debug-probes/j-link/tools/j-flash/about-j-flash/)

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1580368918\/20383\/rhblajzhsv9pb1fdos3h.jpg",
        "mode": "responsive",
        "width": 1362,
        "height": 651,
        "caption": "**Figure 1:** Segger Official Website"
    }
}]$

- Download the software that corresponds to your Operating System, in this guide we will be using Windows

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1580368927\/20383\/etylt7rqrbcjedteqhqc.jpg",
        "mode": "responsive",
        "width": 1365,
        "height": 648,
        "caption": "**Figure 2:** J-link Software in different platforms"
    }
}]$

- After you have downloaded your corresponding software, install it and wait for a couple of minutes.

### Creating Project in J-Flash

- Upon opening the software, you will be greeted with the following window. Choose **Create a new project**. Then Click **Start J-Flash.**

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1580368932\/20383\/qbhdb7hj0cfq0cghohxx.jpg",
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
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1580368949\/20383\/sccml4h6imieppibarpy.jpg",
        "mode": "responsive",
        "width": 931,
        "height": 716,
        "caption": "**Figure 4:** Configuring the Project"
    }
}]$

- Select the Manufacturer to **Nordic Semi** and Select the Device **nRF52840_xxAA.**

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1574934901\/20383\/h3wken4r8z0rfbznrgrc.jpg",
        "mode": "responsive",
        "width": 914,
        "height": 703,
        "caption": "**Figure 5:** Selecting the Device"
    }
}]$

- Select the Target Interface to be **SWD** and the Speed (kHz) to be **4000** and Press **OK.**

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1574934936\/20383\/hil2ag7u5vavbgpluu1c.jpg",
        "mode": "responsive",
        "width": 913,
        "height": 704,
        "caption": "**Figure 6:** Target Interface and Speed (kHz)"
    }
}]$

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1574956505\/20383\/s91d5tazgtvl1lgihina.jpg",
        "mode": "responsive",
        "width": 913,
        "height": 704,
        "caption": "**Figure 7:** Created Project Successfully"
    }
}]$

### Connecting the RAK5010 with JTAG

- Connect your RAK5010 to your PC through [JTAG](https://store.rakwireless.com/products/emulator-kit) using the following pinout diagram below:

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1569633145\/20383\/hx3crsaspcr2aadaesnc.jpg",
        "mode": "300",
        "width": 922,
        "height": 1920,
        "caption": "**Figure 8**: RAK5010 and JTAG Hardware Interface"
    }
}]$

- Download the latest pre-compiled firmware  [here](https://downloads.rakwireless.com/en/Cellular/RAK5010/Firmware/RAK5010_V3.0.0.8.rar) and extract it in your PC.
- In the J-Flash software Menu Bar, Choose Target -> Connect

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1575007956\/20383\/wcw1maqbahdyhqm5hdb6.jpg",
        "mode": "responsive",
        "width": 916,
        "height": 703,
        "caption": "**Figure 9:** Successfully Created Project"
    }
}]$

- Now, choose the demo firmware that you have downloaded

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1575130824\/20383\/iyk5ueztu9i3eul8jp6z.jpg",
        "mode": "responsive",
        "width": 916,
        "height": 703,
        "caption": "**Figure 10:** Selecting the Hex File"
    }
}]$

- Select Target -> Production Programming to start the flashing process and wait for a couple of minutes.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1575130891\/20383\/wechf9fckqgvlw46bfqe.jpg",
        "mode": "responsive",
        "width": 916,
        "height": 703,
        "caption": "**Figure 11:** Connect with the RAK5010"
    }
}]$

