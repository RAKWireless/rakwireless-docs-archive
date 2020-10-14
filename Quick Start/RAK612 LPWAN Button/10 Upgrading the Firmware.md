---
type: page
title: Upgrading the Firmware
listed: true
slug: upgrading-the-firmware
---published

Please use the the latest firmware for the RAK612 LPWAN Button in order to avoid potential problems. Installing the firmware for is done as follows:

1.Download the **[RAK LoRaButton Upgrade tool](https://downloads.rakwireless.com/en/LoRa/RAK612-LoRaButton/Tools/)** and the latest **[firmware](https://downloads.rakwireless.com/en/LoRa/RAK612-LoRaButton/Firmware/)** for the RAK612 LPWAN Button.

2.Connect your RAK612 LPWAN Button to your PC using the micro-USB cable.

3.Press and Hold Key 1 and Key 2 simultaneously for more than 5 seconds until you see all of the LEDs blink very fast. This will set the LPWAN Button in **boot mode**.

4.Open the RAK LPWAN Button Upgrade tool.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1580396486\/14014\/gorcqexgnzcwclawah1d.png",
        "mode": "responsive",
        "width": 900,
        "height": 753,
        "caption": "**Figure 1:** RAK LPWAN Button Upgrade Tool"
    }
}]$

5.Choose the appropriate port number in the **COM Port** field. Open [auto$](/rak612-lora-button/interfacing-with-rak612-lora-button) document to learn on how to choose the appropriate COM Port used by your RAK612 LPWAN Button. For this demonstration, the COM Port is "**COM3**".

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1580396650\/14014\/tepmumxbepfp4sdbhjkz.png",
        "mode": "responsive",
        "width": 901,
        "height": 747,
        "caption": "**Figure 2:** Select the Appropriate COM Port"
    }
}]$

6.Click **Choose File** and navigate to the directory where you have saved the firmware, that you have just downloaded.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1580396807\/14014\/rd9r0uzkntcflig7rjn3.png",
        "mode": "responsive",
        "width": 900,
        "height": 749,
        "caption": "**Figure 3:** Choosing the Firmware"
    }
}]$

7.Click the **Start** Button and wait for a couple of minutes.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1580397346\/14014\/izbys463j4iss5opqven.png",
        "mode": "responsive",
        "width": 900,
        "height": 749,
        "caption": "**Figure 4:** Start Flashing the Firmware"
    }
}]$

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1580397241\/14014\/s3tifd8ftnqsj6kbpypp.png",
        "mode": "responsive",
        "width": 900,
        "height": 749,
        "caption": "**Figure 5:** Upgrade Firmware Success"
    }
}]$

### Testing the Installed Firmware

In order for you to check if you have successfully installed the firmware on your RAK612 LPWAN Button, open the RAK Serial Port tool on your PC. 

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1561462460\/14014\/aqdkgpflxza7nyu1h1as.png",
        "mode": "responsive",
        "width": 904,
        "height": 590,
        "caption": "**Figure 6:** RAK Serial Port Tool"
    }
}]$

1. **COM Port** - this is where you choose the COM Port of your RAK612 LPWAN Button. 
2. **Baudrate** - the rate, at which information is transferred. (Use **115200** for RAK612 LPWAN Button).
3. **Receiving** - this is where all the responses of your AT Commands will be displayed. 
4. **Sending** - this is where you input your AT Command.
5. **Command** - this is where you save all of your AT Commands for quick reuse. This is very useful for [auto$](/rak612-lora-button/configuring-the-lora-button-using-at-commands).

- Choose the appropriate COM Port and Baud Rate for your RAK612 LPWAN Button then Click the **Open** button to open the serial port.
- Hold any key of the RAK612 LPWAN Button for more than 5 seconds and then you will be able to see the following information:

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1561808989\/14014\/iorhsu7avhgkme7o62jz.jpg",
        "mode": "responsive",
        "width": 305,
        "height": 229,
        "caption": "**Figure 7:** RAK612 LPWAN Button Upgraded Firmware"
    }
}]$

