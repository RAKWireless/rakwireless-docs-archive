---
type: page
title: Burning the Bootloader into the Device
listed: false
slug: burning-the-bootloader-into-the-device
---published

An easy and quick way to have a fully functional gateway is by using a Precompiled Firmware Image provided in this **[directory](https://downloads.rakwireless.com/en/LoRa/WisNode/Firmware/)**.  In this document are the step by step instructions of the bootloader’s burning process into the RAK811 WisNode. 

1.Download and Install the “**STM32CubeProgrammer**” tool in your PC through this [**link**](https://downloads.rakwireless.com/en/LoRa/RAK811/Tools/SetupSTM32CubeProgrammer-2.1.0.rar).

2.You can download the bootloader archive **[here](https://downloads.rakwireless.com/en/LoRa/WisNode/Firmware/RUI_RAK811_BOOT_Version3_0_2.rar)**.

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

5.Connect RAK811 LoRa® Evaluation Board with a computer or laptop through the USB interface.

6.Press the "**RST"** button on the RAK811 LoRa® Evaluation Board.

7.Open the “**STM32CubeProgrammer**” tool, and select **UART** type, then configure the **Port**, **Baudrate**, and **Parity** as the following picture shows:

$plugin[{
    "type": "callout",
    "data": {
        "text": "Make sure to choose the correct port in the COM Port field. You can check this in the [Interfacing with RAK811 LoRa\u00ae Evaluation Board](https:\/\/doc.rakwireless.com\/rak811-lora---evaluation-board\/interfacing-with-rak811-lora---evaluation-board) document.",
        "type": "info",
        "title": "Note:"
    }
}]$

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1579528831\/17276\/tnmjamlsi2v46ececuyw.png",
        "mode": "responsive",
        "width": 1841,
        "height": 1094,
        "caption": "**Fure 2:** UART Settings in STM32CubeProgrammer"
    }
}]$

8.Then, press the “**Connect**” button at the top right corner.

$plugin[{
    "type": "callout",
    "data": {
        "text": "If there are some errors in the Log box or it can not connect, reset RAK811 LoRa\u00ae Evaluation Board, re-open the STM32CubeProgrammer and connect again.",
        "type": "warning",
        "title": "Warning:"
    }
}]$

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1579528927\/17276\/emqstyrikr3xxozxpuuw.png",
        "mode": "responsive",
        "width": 1932,
        "height": 1035,
        "caption": "**Figure 3:** Errors Occurred During Connecting"
    }
}]$

Now, let’s start burning a bootloader into the RAK811 LoRa® Evaluation Board.

9.**Erase** all data on the RAK811 LoRa® Evaluation Board as shown in the picture
below:

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1579529177\/17276\/dqgr32e0pjpodndnivki.png",
        "mode": "responsive",
        "width": 1934,
        "height": 1035,
        "caption": "**Figure 4:** Erasing the Data in the Chip"
    }
}]$

10.Press “**Open file**” and select the unzipped bootloader _bin_ file you downloaded in **Step 2**:

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1579529237\/17276\/omyclw46bapphdfncza8.png",
        "mode": "responsive",
        "width": 1934,
        "height": 1033,
        "caption": "**Figure 5:** Opening the Bootloader file"
    }
}]$

11.Click the “**Download**”
button to start the burning process:

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1579529317\/17276\/gwqu62e6ijyjjgeqaqzj.png",
        "mode": "responsive",
        "width": 1934,
        "height": 1033,
        "caption": "**Figure 6:** Downloading of Bootloader to the Device"
    }
}]$

12.OK, you have burned the firmware into RAK811 LoRa® Evaluation Board successfully!

13.Remove the jump in the "**BOOT**"
and "**3V3**"
pins and transfer it to the “**BOOT**” pin
and the “**GND**”
as shown in the image below:

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1579529354\/17276\/mhnqg3pz8xphtqurzs16.png",
        "mode": "responsive",
        "width": 1934,
        "height": 1035,
        "caption": "**Figure 7:** Completing the Download of Bootloader into the device"
    }
}]$

14.“**Disconnect**” and close the “STM32CubeProgrammer” tool.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1562136239\/17276\/k6qgupbaoecu4ummoopj.jpg",
        "mode": "responsive",
        "width": 623,
        "height": 462,
        "caption": "**Figure 8:** BOOT and GND Connected"
    }
}]$

15.Reconnect the RAK811 LoRa® Evaluation Board with
your PC’s USB interface and proceed to the [Firmware Upgrade Burning](https://doc.rakwireless.com/rak811-lora---evaluation-board/upgrading-the-firmware)
Document.

