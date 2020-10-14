---
type: page
title: Burning the Bootloader
listed: true
slug: burning-the-bootloader
---published

You can burn the bootloader on your RAK7200 by following the steps below:

1.Download and Install the [**STM32CubeProgrammer**](https://www.st.com/content/st_com/en/products/development-tools/software-development-tools/stm32-software-development-tools/stm32-programmers/stm32cubeprog.html#overview) Software from STMicroelectronics on your Windows PC.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1579616038\/17846\/wm3z5nau3zpemcfviq0h.png",
        "mode": "responsive",
        "width": 1318,
        "height": 655,
        "caption": "**Figure 1:** STM32CubeProg Download Page"
    }
}]$

1. Plug in the provided Micro-USB cable into the RAK7200 LPWAN Tracker and insert it in your PC. We need to set the RAK7200 first to work in **Boot Mode.** Refer to Figure 2 below and do the following: Hold down the BOOT0 Button, then press the Reset Button for a couple of seconds. Release the Reset and the BOOT0 Button.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1563384567\/17846\/b1horbt3p40hmvnuxqed.jpg",
        "mode": "300",
        "width": 800,
        "height": 578,
        "caption": "**Figure 2:** RAK7200 Buttons and USB Interface"
    }
}]$

3.Open the STM32CubeProgrammer Software and Select UART type.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1579616174\/17846\/aekfryuujx4mig7hfwua.jpg",
        "mode": "responsive",
        "width": 1212,
        "height": 794,
        "caption": "**Figure 3:** STM32CubeProgrammer Interface"
    }
}]$

- Choose the appropriate port number in the **COM Port** field. Open the [auto$](/rak7200-lora-tracker/interfacing-with-rak7200-lora---tracker) document to check the appropritate COM Port to be used for the demonstration.
- Set the Baud Rate to 115200, and the Parity to Even as seen in **Figure 3** then Press **Connect.**

If you didn't properly set your RAK7200 device to work in BOOT Mode, you will see the following information in the Log Section of the Software:

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1579616187\/17846\/pthfpwcme7kv7fk8vdic.jpg",
        "mode": "responsive",
        "width": 1210,
        "height": 793,
        "caption": "**Figure 4:** Error - Device not in Boot Mode"
    }
}]$

- If this happens, go back to the section above and set your RAK7200 device to work in **Boot Mode** again. 
- If all works well, you will then see the following log:

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1579616218\/17846\/xwcazjqx9mfmqvrr3apr.jpg",
        "mode": "responsive",
        "width": 972,
        "height": 634,
        "caption": "**Figure 5:** Success - Working in Boot Mode"
    }
}]$

4.Now that you have successfully connected your RAK7200 to the STM32CubeProgrammer Tool, let's burn the Bootloader into the RAK7200.

- Download the Bootloader for the RAK7200 LPWAN Tracker [**here**](https://downloads.rakwireless.com/en/LoRa/RAK7200-Tracker/Firmware/).
- In the STM32CubeProgrammer, Click the "**Erase Chip**" button to erase all the data on RAK7200:

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1579616236\/17846\/o8jcjqkwzlv5ukqbrpg9.jpg",
        "mode": "responsive",
        "width": 3002,
        "height": 1888,
        "caption": "**Figure 6:** Erase Chip"
    }
}]$

- Click "**Open File**" and select the correct Bootloader file that you have just downloaded.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1579616260\/17846\/f8r7owhtv3psucvhtejc.jpg",
        "mode": "responsive",
        "width": 1212,
        "height": 793,
        "caption": "**Figure 7:** Open the Firmware File"
    }
}]$

- Click the "**Download**" Button to start the burning process:

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1579616283\/17846\/qzhcdcluajgue2hsl7hb.jpg",
        "mode": "responsive",
        "width": 3002,
        "height": 1888,
        "caption": "**Figure 8:** Uploading the Bootloader"
    }
}]$

- After a couple of seconds, you will see the following window telling that you have successfully burned the Bootloader to your RAK7200!

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1579616308\/17846\/yxjlq9zs9ztlugceqnfd.jpg",
        "mode": "responsive",
        "width": 3000,
        "height": 1942,
        "caption": "**Figure 9:** Success Upgrade of the Firmware"
    }
}]$

- “**Disconnect**” and close the STM32CubeProgrammer tool.

