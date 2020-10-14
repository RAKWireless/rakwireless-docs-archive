---
type: page
title: Burning Bootloader into the Device
listed: true
slug: burning-bootloader-into-the-device
---draft

Please use the the latest firmware for the RAK811 LoRa Module Breakout Board accessible in this [**directory**](https://downloads.rakwireless.com/en/LoRa/RAK811/Firmware/) in order to avoid potential problems. Burning the Bootloader into the device is done as follows:

$plugin[{
    "type": "callout",
    "data": {
        "text": "Skip this section if you have a  V3.0.0.0 RAK811 firmware or newer, for it has already a bootloader.",
        "type": "warning",
        "title": "Warning!"
    }
}]$

1- To start with, download and install the “**STM32CubeProgrammer**” tool in your PC through this [link](https://www.st.com/content/st_com/en/products/development-tools/software-development-tools/stm32-software-development-tools/stm32-programmers/stm32cubeprog.html#overview) or through this [RAK directory]([https://downloads.rakwireless.com/en/LoRa/RAK811/Tools/SetupSTM32CubeProgra](https://downloads.rakwireless.com/en/LoRa/RAK811/Tools/SetupSTM32CubeProgra) mmer-2.1.0.rar).

2- Then, configure your RAK811 by jumping the “**BOOT**” pin and “**VCC**” pin for boot mode then connect **RX, TX, VCC**, and **GND** with a USB-UART tool, as the following pictures shown below:

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1564455041\/16634\/aleditom1olysdlbdues.jpg",
        "mode": "300",
        "width": 841,
        "height": 619,
        "caption": "**Figure 1**: Pin Configuration for Burning BootLoader"
    }
}]$

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1565101666\/16634\/iazi7pnutuumetesq7sw.jpg",
        "mode": "600",
        "width": 4167,
        "height": 2590,
        "caption": "**Figure 2**: RAK811 Interface to USB-UART module Connection"
    }
}]$

3- Choose the correct port number in the **COM Port** field. You can check this in the Device Manager.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1562143642\/16634\/lanbw02v6mkcxp75jnac.jpg",
        "mode": "responsive",
        "width": 832,
        "height": 666,
        "caption": "**Figure 3**: Checking Com PORT through Device Manager"
    }
}]$

4- Open the “**STM32CubeProgrammer**” tool.

5- Select **UART type**; go to COM Port and look for your RAK811 Breakout Board COM Port (ex. COM5). 

6- Configure the Baud rate and Parity.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1561798910\/16634\/pcki7wjry2w2hrognjzg.png",
        "mode": "responsive",
        "width": 1198,
        "height": 780,
        "caption": "**Figure 4**: UART Settings in STM32CubeProgrammer"
    }
}]$

7- Then, press the “**Connect**” button at the top right corner.

$plugin[{
    "type": "callout",
    "data": {
        "text": "If there are some errors in the Log box or it can\u2019t connect, just close the STM32CubeProgrammer, and reinsert the RAK811 Breakout Board again; then open the STM32CubeProgrammer and connect.",
        "type": "info",
        "title": "Warning!"
    }
}]$

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1561799050\/16634\/zn5wxznbcwm8bdvhr3yc.png",
        "mode": "responsive",
        "width": 1196,
        "height": 779,
        "caption": "**Figure 5**: Errors Occurred During Connecting"
    }
}]$

Now, let’s start burning the bootloader into the RAK811 Breakout Board.

8- First, erase all data on the **RAK811 Breakout Board** referred from the following picture below:

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1561799492\/16634\/mpakwwtdjaf9kb9efvdv.jpg",
        "mode": "responsive",
        "width": 1204,
        "height": 777,
        "caption": "**Figure 6**: Erasing the Data in the Chip"
    }
}]$

9- Press “**Open file**” and select the bootloader file in the pop-up window as follows:

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1561799515\/16634\/k2bi3s5q8ipmmtrxsef3.png",
        "mode": "responsive",
        "width": 1198,
        "height": 779,
        "caption": "**Figure 7**: Opening the Bootloader file"
    }
}]$

10- Click the “**Download**” button to start the burning process:

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1561799544\/16634\/ljua570nb5wiyyrdyofe.jpg",
        "mode": "responsive",
        "width": 1433,
        "height": 888,
        "caption": "**Figure 8**: Downloading of Bootloader to the device"
    }
}]$

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1561799587\/16634\/ksbjk3tk2wfdtskq4x7l.jpg",
        "mode": "responsive",
        "width": 1200,
        "height": 750,
        "caption": "**Figure 9**: Completing the Download of Bootloader into the device"
    }
}]$

11- OK, you have burned the firmware into **RAK811 Breakout Board** successfully!

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1561799616\/16634\/v4y3hopgwhizcmju8uik.jpg",
        "mode": "responsive",
        "width": 1194,
        "height": 747,
        "caption": "**Figure 10**: Successfully Downloaded the Bootloader to the device"
    }
}]$

12- "**Disconnect**” and close the “**STM32CubeProgrammer**” tool. Then, disconnect BOOT pin and VCC pin to let RAK811 Breakout Board work in normal mode.

13- Pull out and reinsert the USB interface into your PC.

If you have opened the serial port tool, you can see some content like this:

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1564455497\/16634\/ttm1egimejuxxfb1zsj8.jpg",
        "mode": "responsive",
        "width": 467,
        "height": 571,
        "caption": "**Figure 11**: Successfully Downloading the Bootloader"
    }
}]$

Alright! You can now start burning the upgraded firmware into RAK811 Breakout Board.

---published

Please use the the latest firmware for the RAK811 LoRa Module Breakout Board accessible in this [**directory**](https://downloads.rakwireless.com/en/LoRa/RAK811/Firmware/) in order to avoid potential problems. Burning the Bootloader into the device is done as follows:

$plugin[{
    "type": "callout",
    "data": {
        "text": "Skip this section if you have a  V3.0.0.0 RAK811 firmware or newer, for it has already a bootloader.",
        "type": "warning",
        "title": "Warning!"
    }
}]$

1- To start with, download and install the “**STM32CubeProgrammer**” tool in your PC through this [link](https://www.st.com/content/st_com/en/products/development-tools/software-development-tools/stm32-software-development-tools/stm32-programmers/stm32cubeprog.html#overview) or through this [RAK directory](https://downloads.rakwireless.com/en/LoRa/RAK811/Tools/SetupSTM32CubeProgra mmer-2.1.0.rar).

2- Then, configure your RAK811 by jumping the “**BOOT**” pin and “**VCC**” pin for boot mode then connect **RX, TX, VCC**, and **GND** with a USB-UART tool, as the following pictures shown below:

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1564455041\/16634\/aleditom1olysdlbdues.jpg",
        "mode": "300",
        "width": 841,
        "height": 619,
        "caption": "**Figure 1**: Pin Configuration for Burning BootLoader"
    }
}]$

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1564455199\/16634\/pjqkytmyceih3tr4dyik.png",
        "mode": "300",
        "width": 405,
        "height": 526,
        "caption": "**Figure 2**: RAK811 Interface with USB-UART module connected to PC"
    }
}]$

3- Choose the correct port number in the **COM Port** field. You can check this in the Device Manager.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1562143642\/16634\/lanbw02v6mkcxp75jnac.jpg",
        "mode": "responsive",
        "width": 832,
        "height": 666,
        "caption": "**Figure 3**: Checking Com PORT through Device Manager"
    }
}]$

4- Open the “**STM32CubeProgrammer**” tool.

5- Select **UART type**; go to COM Port and look for your RAK811 Breakout Board COM Port (ex. COM5). 

6- Configure the Baud rate and Parity.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1561798910\/16634\/pcki7wjry2w2hrognjzg.png",
        "mode": "responsive",
        "width": 1198,
        "height": 780,
        "caption": "**Figure 4**: UART Settings in STM32CubeProgrammer"
    }
}]$

7- Then, press the “**Connect**” button at the top right corner.

$plugin[{
    "type": "callout",
    "data": {
        "text": "If there are some errors in the Log box or it can\u2019t connect, just close the STM32CubeProgrammer, and reinsert the RAK811 Breakout Board again; then open the STM32CubeProgrammer and connect.",
        "type": "info",
        "title": "Warning!"
    }
}]$

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1561799050\/16634\/zn5wxznbcwm8bdvhr3yc.png",
        "mode": "responsive",
        "width": 1196,
        "height": 779,
        "caption": "**Figure 5**: Errors Occurred During Connecting"
    }
}]$

Now, let’s start burning the bootloader into the RAK811 Breakout Board.

8- First, erase all data on the **RAK811 Breakout Board** referred from the following picture below:

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1561799492\/16634\/mpakwwtdjaf9kb9efvdv.jpg",
        "mode": "responsive",
        "width": 1204,
        "height": 777,
        "caption": "**Figure 6**: Erasing the Data in the Chip"
    }
}]$

9- Press “**Open file**” and select the bootloader file in the pop-up window as follows:

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1561799515\/16634\/k2bi3s5q8ipmmtrxsef3.png",
        "mode": "responsive",
        "width": 1198,
        "height": 779,
        "caption": "**Figure 7**: Opening the Bootloader file"
    }
}]$

10- Click the “**Download**” button to start the burning process:

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1561799544\/16634\/ljua570nb5wiyyrdyofe.jpg",
        "mode": "responsive",
        "width": 1433,
        "height": 888,
        "caption": "**Figure 8**: Downloading of Bootloader to the device"
    }
}]$

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1561799587\/16634\/ksbjk3tk2wfdtskq4x7l.jpg",
        "mode": "responsive",
        "width": 1200,
        "height": 750,
        "caption": "**Figure 9**: Completing the Download of Bootloader into the device"
    }
}]$

11- OK, you have burned the firmware into **RAK811 Breakout Board** successfully!

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1561799616\/16634\/v4y3hopgwhizcmju8uik.jpg",
        "mode": "responsive",
        "width": 1194,
        "height": 747,
        "caption": "**Figure 10**: Successfully Downloaded the Bootloader to the device"
    }
}]$

12- "**Disconnect**” and close the “**STM32CubeProgrammer**” tool. Then, disconnect BOOT pin and VCC pin to let RAK811 Breakout Board work in normal mode.

13- Pull out and reinsert the USB interface into your PC.

If you have opened the serial port tool, you can see some content like this:

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1564455497\/16634\/ttm1egimejuxxfb1zsj8.jpg",
        "mode": "responsive",
        "width": 467,
        "height": 571,
        "caption": "**Figure 11**: Successfully Downloading the Bootloader"
    }
}]$

Alright! You can now start burning the upgraded firmware into RAK811 Breakout Board.

