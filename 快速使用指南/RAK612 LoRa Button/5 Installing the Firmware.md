---
type: page
title: Installing the Firmware
listed: true
slug: installing-the-firmware
---published

Please use the the latest firmware for the RAK612 LoRa Button in order to avoid potential problems. Installing the firmware for is done as follows:

- Download the **[RAK LoRaButton Upgrade tool](https://downloads.rakwireless.com/en/LoRa/RAK612-LoRaButton/Tools/)** and the latest **[firmware](https://downloads.rakwireless.com/en/LoRa/RAK612-LoRaButton/Firmware/)** for the RAK612 LoRa Button.
- Connect your RAK612 LoRa Button to your PC using the micro-usb cable.
- Press and Hold Key 1 and Key 2 simultaneously for more than 5 seconds until you see all of the LEDs blink very fast. This will set the LoRa Button in **boot mode**.
- Open the RAK LoRaButton Upgrade tool.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1560869712\/14014\/ptpffnws4sv2lf2s5zlv.png",
        "mode": "responsive",
        "width": 591,
        "height": 492,
        "caption": "**Figure 1:** RAK LoRa Button Upgrade Tool"
    }
}]$

- Choose the appropriate port number in the **COM Port** field. You can check this is the Device Manager.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1560869886\/14014\/vu2vpkw4t18hg540dpn5.png",
        "mode": "600",
        "width": 832,
        "height": 666,
        "caption": "**Figure 2:**  Device Manager in Windows"
    }
}]$

- Go to Ports (COM & LPT) , and look for your RAK612 LoRa Button COM Port (COM3 in the example)

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1561808932\/14014\/yujpuck99irkrqqrauwd.jpg",
        "mode": "600",
        "width": 738,
        "height": 613,
        "caption": "**Figure 3:** Select the Appropriate COM Port"
    }
}]$

- Click **Choose File** and navigate to the directory where you have saved the firmware, that you just downloaded.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1561808740\/14014\/acnaqvsoqhvknvptx4gg.jpg",
        "mode": "responsive",
        "width": 585,
        "height": 483,
        "caption": "**Figure 4:** Choosing the Firmware"
    }
}]$

- Click the **Start** Button and wait for a couple of minutes.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1561808799\/14014\/bito3bcmxqebz7pkssrx.jpg",
        "mode": "responsive",
        "width": 590,
        "height": 486,
        "caption": "**Figure 5:** Start Flashing the Firmware"
    }
}]$

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1561808847\/14014\/mkkkcs34sjkbwu6wtb6w.jpg",
        "mode": "responsive",
        "width": 589,
        "height": 487,
        "caption": "**Figure 6:** Upgrade Firmware Success"
    }
}]$

### Testing the Installed Firmware

In order for you to check if you have successfully installed the firmware on your RAK612 LoRa Button, open a Serial Port tool on your PC. We recommend using RAK's Serial Port Tool which can be downloaded **[here](https://downloads.rakwireless.com/en/LoRa/RAK811/Tools/)**.

- Open the RAK Serial Port Tool and follow the steps below:

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1561462460\/14014\/aqdkgpflxza7nyu1h1as.png",
        "mode": "responsive",
        "width": 904,
        "height": 590,
        "caption": "**Figure 7:** RAK Serial Port Tool"
    }
}]$

1. **COM Port** - this is where you choose the COM Port of your RAK612 LoRa Button. 
2. **Baudrate** - the rate, at which information is transferred. (Use **115200** for RAK612 LoRa Button).
3. **Receiving** - this is where all the responses of your AT Commands will be displayed. 
4. **Sending** - this is where you input your AT Command.
5. **Command** - this is where you save all of your AT Commands for quick reuse. This is very useful for [auto$](/rak612-lora-button/configuring-the-lora-button-using-at-commands).

- Choose the appropriate COM Port and Baud Rate for your LoRa Button then Click the **Open** button to open the serial port.
- Hold any key of the LoRa Button for more than 5 seconds and then you will be able to see the following information:

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1561808989\/14014\/iorhsu7avhgkme7o62jz.jpg",
        "mode": "responsive",
        "width": 305,
        "height": 229,
        "caption": "**Figure 8:** RAK612 LoRa Button Upgraded Firmware"
    }
}]$

