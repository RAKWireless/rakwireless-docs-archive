---
type: page
title: Firmware Flashing and Testing
listed: true
slug: firmware-flashing-and-testing
---published

## RAK811 LPWAN Evaluation Board Bootloader and Firmware

Kindly look into the different documents on how to burn and update the bootloader and firmware of RAK811 LPWAN Evaluation board. Both the bootloader and firmware files can be downloaded [here](https://downloads.rakwireless.com/en/LoRa/WisNode/Firmware/).

- **Bootloader**: [auto$](/rak811-lora-evaluation-board/burning-the-bootloader-into-the-device)
- **Firmware**: [auto$](/rak811-lora-evaluation-board/upgrading-the-firmware)

## Arduino Demo firmware

1.Open the "**JoinNetworkOTAA.ino**" by navigating through `File>Examples>Arduino-RAK811-Library` in the Arduino IDE.

2.Edit the **Device EUI**, **Application Key and Application EUI** in the "**JoinNetworkOTAA.ino**" which can be obtained in the [auto$](/rak811-lora-evaluation-board/connecting-to-the-things-network--ttn-) document.

3.Afterwhich, proceed to uploading the sketch by following the steps in the image below:

$plugin[{
    "type": "callout",
    "data": {
        "text": "Make sure to disconnect the connection between the Rx and Tx connection between the RAK811 LPWAN Evaluation Board and the Arduino Mega 2560. Not doing so will make the sketch uploading fail.",
        "type": "info",
        "title": "Note:"
    }
}]$

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1580822655\/25245\/jzx86mrtckrokxrumb8w.jpg",
        "mode": "responsive",
        "width": 1510,
        "height": 981,
        "caption": "**Figure 1**: Arduino Mega 2560 Board and Port settings prior to Sketch Uploading."
    }
}]$

4.You can check the uploading logs shown in the red box in the image above to check whether it is successfully uploaded or not. If the sketch uploading fails, kindly look into each of the logs to address each issue.

## Test LoRa® Node with LoRaWAN®

Using the "JoinNetworkOTAA.ino" sketch in the previous section, it should automatically connect to **TheThingsNetwork(TTN)** through the Gateway in range.

1.Setup and open the two Serial Ports, Arduino USB Port and the SoftwareSerial Port using the USB-UART TTL converter. Kindly reset the RAK811 LPWAN Evaluation Board and Serial logs must be shown same with the image below:

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1580823280\/25245\/sxu06fbgafxyxhz3wcum.png",
        "mode": "responsive",
        "width": 1085,
        "height": 620,
        "caption": "**Figure 2**: Serial Port View using USB-UART TTL SoftwareSerial Port (left) and Arduino USB Port (right)"
    }
}]$

In this section, you might be wondering why we are using two serial ports. As a default, the Arduino Mega 2560 has its own Serial Port which can be viewed through the Serial Monitor. In this port, AT Commands setup are written into the RAK811 LPWAN Evaluation Board for us to be able to connect to TheThingsNetwork(TTN). However, debug logs cannot be printed in the same port for it may interfere with the setup. Thus, a secondary Serial Port must be used as debug logs display using the SoftwareSerial Port shown in the USB-UART TTL converter COM Port. 

2.With the successful Serial Logs shown in the image above, we shall then check the logs in the Application Data tab in TheThingsNetwork (TTN). If the connection is successful, received logs must be shown same with the image below:

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1580823927\/25245\/a9dpjl7pfck2ho628eux.png",
        "mode": "responsive",
        "width": 1099,
        "height": 659,
        "caption": "**Figure 3**: TTN logs in the Connection Attempt using Arduino Mega 2560"
    }
}]$

