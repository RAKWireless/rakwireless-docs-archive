---
type: page
title: Burning the Bootloader into the Device
listed: true
slug: burning-the-bootloader-into-the-device
---published

An easier and quick way to get started is to use the latest pre-compiled Firmware accessible in this **[directory](https://downloads.rakwireless.com/en/LoRa/WisNode/Firmware/)**.

1.Download and Install the “STM32CubeProgrammer” tool in your PC through this [**link**](https://downloads.rakwireless.com/en/LoRa/RAK811/Tools/SetupSTM32CubeProgrammer-2.1.0.rar).

2.You can download the bootloader archive [**here**](https://downloads.rakwireless.com/en/LoRa/WisNode/Firmware/RAK811_BOOT_V3.0.0.0.rar).

3.Download the "Serial tool" [**here**](https://downloads.rakwireless.com/en/LoRa/RAK811/Tools/RAK_SERIAL_PORT_TOOL_V1.2.1.zip).

4.Bridge the “**BOOT**” pin and “**3V3**” pin to set the board in boot mode as shown in the image
below:

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1563066715\/17276\/c7n0hpocsosss86qo80a.jpg",
        "mode": "responsive",
        "width": 555,
        "height": 370,
        "caption": null
    }
}]$

5.Connect RAK811 WisNode LoRa Module with a computer or laptop through the USB interface.

6.Press the "**RST"** button on the RAK811 WisNode LoRa Module.

7.Open the “**STM32CubeProgrammer**” tool, and select **UART** type, then configure the **Port**, **Baudrate**, and **Parity** as the following picture shows:

Make sure to choose the correct port in the COM Port field. You can check this in the
Device Manager for example in Windows.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1562131402\/17276\/aayrl3cn0y3j4y9hgccs.jpg",
        "mode": "responsive",
        "width": 1198,
        "height": 780,
        "caption": "**Figure 2.** UART Settings in STM32CubeProgrammer"
    }
}]$

8.Then, press the “**Connect**” button at the top right corner.

$plugin[{
    "type": "callout",
    "data": {
        "text": "If there are some errors in the Log box or it can not connect, reset RAK811 WisNode LoRa Module, re-open the STM32CubeProgrammer and connect again.",
        "type": "warning",
        "title": "Warning:"
    }
}]$

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1562133572\/17276\/z5nhidzfntkmfxl1bqye.jpg",
        "mode": "responsive",
        "width": 1196,
        "height": 779,
        "caption": "**Figure 3.** Errors Occurred During Connecting"
    }
}]$

Now, let’s start burning a bootloader into the RAK811 WisNode LoRa Module.

9.Erase all data on the RAK811 WisNode LoRa Module as shown in the picture
below:

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1562134377\/17276\/qb8qnxdmyytdkz2gthgr.jpg",
        "mode": "responsive",
        "width": 1204,
        "height": 777,
        "caption": "**Figure 4.** Erasing the Data in the Chip"
    }
}]$

10.Press “**Open file**” and select the unziped bootloader _bin_ file you downloaded in Step 1:

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1562134628\/17276\/lelkjdojaq8a9tulhquj.jpg",
        "mode": "responsive",
        "width": 1198,
        "height": 779,
        "caption": "**Figure 5.** Opening the Bootloader file"
    }
}]$

11.Click the “**Download**”
button to start the burning process:

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1562135334\/17276\/lam5v1phzkkksepqoad5.jpg",
        "mode": "responsive",
        "width": 1433,
        "height": 888,
        "caption": "**Figure 6.** Downloading of Bootloader to the Device"
    }
}]$

12.OK, you have burned the firmware into RAK 811 WisNode LoRa successfully!

13.Remove the jump in the "**BOOT**"
and "**3V3**"
pins and transfer it to the “**BOOT**” pin
and the “**GND**”
as shown in the image below:

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1562135436\/17276\/cju1ydmecqvwc9xmyumm.jpg",
        "mode": "responsive",
        "width": 1194,
        "height": 747,
        "caption": "**Figure 7.** Completing the Download of Bootloader into the device"
    }
}]$

14.“Disconnect” and close the “STM32CubeProgrammer” tool.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1562136239\/17276\/k6qgupbaoecu4ummoopj.jpg",
        "mode": "responsive",
        "width": 623,
        "height": 462,
        "caption": "**Figure 8.** BOOT and GND Connected"
    }
}]$

15.Reconnect the RAK811 WisNodeLoRa Module with
your PC’s USB interface and proceed to the Firmware Upgrade Burning
Document.

