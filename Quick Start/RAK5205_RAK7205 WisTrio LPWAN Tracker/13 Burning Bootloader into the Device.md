---
type: page
title: Burning Bootloader into the Device
listed: true
slug: installing-the-firmware
---published

Please use the the latest firmware for the RAK5205 WisTrio LPWAN Tracker accessible in this **[directory](https://downloads.rakwireless.com/en/LoRa/WisTrio-LoRa-RAK5205/Firmware/)** in order to avoid potential problems. Burning the Bootloader into the device is done as follows:

$plugin[{
    "type": "callout",
    "data": {
        "text": "Skip this section if you have a RAK5205 V3.0.0.0 firmware or newer, for it has already a bootloader.",
        "type": "warning",
        "title": "Warning!"
    }
}]$

You need to make sure you have the latest firmware on your device . To be able to do this, you need to follow these steps:

**1.** To start with, download and install the “STM32CubeProgrammer” tool in your PC through this link or through this RAK directory.

**2.** Then, configure your RAK5205 by jumping the “**BOOT**” pin and “**VCC**” pin for boot mode as the following pictures shown below:

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1570807770\/17318\/eeh8zvvyderwyp6caxsu.jpg",
        "mode": "responsive",
        "width": 708,
        "height": 358,
        "caption": "**Figure 1**: Boot and VCC Pins"
    }
}]$

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1570807775\/17318\/ygkxl9ch7laja72wssxw.jpg",
        "mode": "responsive",
        "width": 752,
        "height": 360,
        "caption": "**Figure 2**: Jumper at Boot and VCC pins"
    }
}]$

**3.** Connect your RAK5205 to your PC using the USB cable as follow:

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1570807785\/17318\/mnlyzbqc9pcxtudki9gb.jpg",
        "mode": "responsive",
        "width": 589,
        "height": 633,
        "caption": "**Figure 3**: RAK5205 connected to your PC via USB cable"
    }
}]$

**4.** Choose the correct port number in the **COM Port** field. You can check this in the Device Manager.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1570807983\/17318\/ct9xcr8m3feyf4hcsuc1.jpg",
        "mode": "responsive",
        "width": 832,
        "height": 666,
        "caption": "**Figure 4**: Checking COM Port through Device Manager"
    }
}]$

**5.** Open the “**STM32CubeProgrammer**” tool.

**6.** Select **UART type**; go to COM Port and look for your RAK5205 Breakout Board COM Port (ex. COM5).

**7.** Configure the **Baud rate** and **Parity**.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1570808155\/17318\/kxwsnn5cfc3c7mhdg9kw.jpg",
        "mode": "responsive",
        "width": 1106,
        "height": 719,
        "caption": "**Figure 5**: UART Settings in STM32CubeProgrammer"
    }
}]$

**8.** Then, press the “**Connect**” button at the top right corner.

$plugin[{
    "type": "callout",
    "data": {
        "text": "If there are some errors in the Log\nbox or it can\u2019t connect, please close the STM32CubeProgrammer and reset RAK5205,\nthen open the STM32CubeProgrammer and connect again.",
        "type": "warning",
        "title": "Warning"
    }
}]$

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1570808351\/17318\/uu4dimjfeqnzjefqbznv.jpg",
        "mode": "responsive",
        "width": 1107,
        "height": 776,
        "caption": "**Figure 6**: Errors Occurred During Connecting"
    }
}]$

- The correct Log you should see is the information like the following picture shows:

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1570808578\/17318\/fe8qmougdo8brhppqggd.jpg",
        "mode": "responsive",
        "width": 1107,
        "height": 686,
        "caption": "**Figure 7**: Successful Connection Log to your Device"
    }
}]$

Now, let’s start burning the bootloader into the RAK5205 WisTrio LPWAN Tracker.

**9.** First, **erase all** data on the RAK5205 WisTrio LPWAN Tracker referred from the following picture below:

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1570808539\/17318\/tzcxzjuvnvzibznrfcwg.jpg",
        "mode": "responsive",
        "width": 1107,
        "height": 772,
        "caption": "**Figure 8**: Erasing the Data in the Chip"
    }
}]$

**10.** Press “**Open file**” and select the bootloader file in the pop-up window as follows:

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1570808792\/17318\/ldnfi1fr87cxoxwgfbpa.jpg",
        "mode": "responsive",
        "width": 1135,
        "height": 737,
        "caption": "**Figure 9**: Opening the Bootloader file"
    }
}]$

**11.** Click the “**Download**” button to start the burning process

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1570809016\/17318\/gzos6pwkmw5lvbotnxf5.jpg",
        "mode": "responsive",
        "width": 831,
        "height": 530,
        "caption": "**Figure 10**: Downloading of Bootloader to the device"
    }
}]$

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1570809092\/17318\/iteqb0yu5pqaz13he92k.jpg",
        "mode": "responsive",
        "width": 885,
        "height": 554,
        "caption": "**Figure 11**: Completing the Download of Bootloader into the device"
    }
}]$

**12.** OK, you have successfully burned the firmware into RAK5205 WisTrio LPWAN Tracker!

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1570809276\/17318\/fnx2ybuctwfdgjcdnb9c.jpg",
        "mode": "responsive",
        "width": 942,
        "height": 589,
        "caption": "**Figure 12**: Successfully Burned the Bootloader to the device"
    }
}]$

**13.** "**Disconnect**” and close the “**STM32CubeProgrammer**” tool. Then, power down and remove the connection between BOOT pin and VCC pin to let RAK5205 WisTrio LPWAN Tracker work in normal mode.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1570809476\/17318\/nuoi6ddmrpp7ne32p7gm.jpg",
        "mode": "responsive",
        "width": 1108,
        "height": 537,
        "caption": "**Figure 13**: Jumper connection removed"
    }
}]$

**14.** Then, connect RAK5205 with your PC’s USB interface again.

If you have opened the serial port tool, you can see some content like this:

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1570809621\/17318\/wpwt4lcs7bupbdess4ns.jpg",
        "mode": "300",
        "width": 466,
        "height": 574,
        "caption": "**Figure 14**: Successfully Downloading the Bootloader"
    }
}]$

Alright! You can now start burning the firmware into RAK5205 WisTrio LPWAN Tracker.

