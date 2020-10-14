---
type: page
title: Installing the Firmware
listed: true
slug: installing-the-firmware
---published

You need to make sure you have the latest firmware on your RAK5205 WisTrio LoRa Tracker. To be able to do this, you need to follow these steps:

1. Download the appropriate driver for the RAK5205 [**here**](http://docs.rakwireless.com/en/LoRa/WisTrio-LoRa-RAK5205/Tools/CP210x_Windows_Drivers.zip). Extract the package in your windows machine and install the driver.
2. Download the **[latest firmware](https://downloads.rakwireless.com/en/LoRa/WisTrio-LoRa-RAK5205/Firmware/)** for the RAK5205 in this github repository.

$plugin[{
    "type": "callout",
    "data": {
        "text": "Make sure to pick the appropriate bin file depending on the region you are in. \n\n> **\"RUI_RAK5205_V3.x.x.x.H\"** supported regions are:   IN865, EU868, US915, AU915, KR920, AS920, AS923\n\n> **\"RUI_RAK5205_V3.x.x.x.L\u201d** supported regions are:  EU433, CN470\n\nVisit this [**article**](https:\/\/www.thethingsnetwork.org\/docs\/lorawan\/frequencies-by-country.html) for more information on your local TTN frequency plan.",
        "type": "info",
        "title": "Note"
    }
}]$

1. Download the [**STM Flashing Tool**](http://docs.rakwireless.com/en/LoRa/WisTrio-LoRa-RAK5205/Tools/Flash_Loader_Demonstrator.zip). Extract the zip file and install the software. You will be using it in flashing the firmware for your RAK5205.
2. Insert the provided jumper on the Boot line pins, shorting them. This will allow for the firmware to be uploaded. Also,  make sure that the RX pin of J25 is connected to the RXCP pin.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1562318396\/17318\/m43euzyhgmy1kylysdqj.png",
        "mode": "300",
        "width": 842,
        "height": 376,
        "caption": "**Figure 1:** Boot Line shorted using the Jumper Pins"
    }
}]$

$plugin[{
    "type": "callout",
    "data": {
        "text": "Before powering your RAK5205, make sure you have already connected the LoRa and GPS antennas. Not doing so might damage your board.",
        "type": "warning",
        "title": "Warning"
    }
}]$

1. Plug in the provided Micro-USB cable into the RAK5205 Board and insert it in your PC.
2. Open the STM Flashing Tool (**Flash Loader Demonstrator**) and configure the parameters as seen in the Figure 2 below:

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1562318950\/17318\/pn1x1pwpdusg47uljypx.jpg",
        "mode": "responsive",
        "width": 432,
        "height": 522,
        "caption": "**Figure 2:** Flash Loader Tool"
    }
}]$

1. If you have followed the parameters just like in the Figure 2 above, Click "Next" and you will see the following image:

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1562319306\/17318\/of6atbahdrwez0oc1qww.jpg",
        "mode": "responsive",
        "width": 437,
        "height": 521,
        "caption": "**Figure 3:** Flash Loader Device Validation Screen"
    }
}]$

1. Click "Next" and Select the Target device as shown in the figure below:

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1562319854\/17318\/ssvkfulb1uuaa6fkxndb.jpg",
        "mode": "responsive",
        "width": 433,
        "height": 521,
        "caption": "**Figure 4:** Device Selection"
    }
}]$

1. Click "Next". Now you need to select the bin file with the firmware you have just downloaded in the last step. Use the buttons circled in red in Figure 5  and navigate to the location of the file.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1562320106\/17318\/gse9zqwk62jnb3vrahox.jpg",
        "mode": "responsive",
        "width": 1465,
        "height": 566,
        "caption": "**Figure 5:** Selecting the Firmware File"
    }
}]$

1. Press "Next" and wait for a couple of minutes. A screen with a loading bar will appear and will turn green if the process completes successfully.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1562320239\/17318\/wvbfodwzlsbocaclxhrj.jpg",
        "mode": "responsive",
        "width": 928,
        "height": 533,
        "caption": "**Figure 6:** Firmware Upload Progress"
    }
}]$

Congratulations! You have now successfully flashed the latest firmware to your RAK5205 WisTrio LoRa Tracker. You can now close the tool and unplug the device.

$plugin[{
    "type": "callout",
    "data": {
        "text": "Do not forget to remove the boot jumper in your RAK5205 WisTrio LoRa Tracker after you are done flashing the firmware!",
        "type": "warning",
        "title": "Warning"
    }
}]$

### Testing the Installed Firmware

Now that you have removed the Boot Jumper in the previous step, the RAK5205 WisTrio LoRa Tracker is back in operational mode.

- In order for you to check if you have successfully installed the firmware on your RAK5205 WisTrio LoRa Tracker, open a Serial Port tool on your PC. We recommend using RAK's Serial Port Tool which can be downloaded **[here](https://downloads.rakwireless.com/en/LoRa/WisTrio-LoRa-RAK5205/Tools/RAK_SERIAL_PORT_TOOL_V1.2.1.zip)**.
- Open the RAK Serial Port Tool:

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1562323371\/17318\/t4z5eicxo6po9t2ubox3.png",
        "mode": "responsive",
        "width": 904,
        "height": 590,
        "caption": "**Figure 7:** RAK Serial Port Tool"
    }
}]$

1. **COM Port** - this is where you choose the COM Port of your RAK5205.
2. **Baudrate** - the rate, at which information is transferred. (Use **115200** for RAK5205).
3. **Receiving** - this is where all the responses of your AT Commands will be displayed. If you have successfully installed the firmware and set the COM Port and the Baudrate,  you will see data being reported from the on-board sensors of RAK5205. You can also see the version of firmware installed.
4. **Sending** - this is where you input your AT Command.
5. **Command** - this is where you save all of your AT Commands for quick reuse.

In the next section we will list some of the AT commands you will need , if we are to configure the node. As an example we will set it up to work with The Things Network.

