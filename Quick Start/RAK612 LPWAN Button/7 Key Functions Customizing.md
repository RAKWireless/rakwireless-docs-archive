---
type: page
title: Key Functions Customizing
listed: true
slug: key-functions-customizing
---published

This document walks through the step-by-step discussion on how to customize each key functions of the RAK612 LPWAN Button. For you to enable the message customization, you must at least have the 2.0.2.1.2 firmware version. 

$plugin[{
    "type": "callout",
    "data": {
        "text": "If your RAK612 LPWAN Button's firmware version is lower than the least version set, please download the latest RAK612 LPWAN Button firmware [here](https:\/\/downloads.rakwireless.com\/en\/LoRa\/RAK612-LoRaButton\/Firmware\/) and proceed to the [auto$](\/rak612-lora-button\/upgrading-the-firmware) document.",
        "type": "info",
        "title": "Note:"
    }
}]$

### Defaults

Listed below are the default messages send by the RAK612 LPWAN Button whenever each key is pressed:

| **Key** | **Message** | 
| ---- | ---- | 
| Key 1 | "Key 1" | 
| Key 2 | "Key 2" | 
| Key 3 | "Key 3" | 
| Key 4 | "Key 4" | 


### Customizing

To fully customize the messages sent by the RAK612 LPWAN Button in each key pressed, we must configure it using the [RAK Serial Port Tool](https://downloads.rakwireless.com/en/LoRa/Tools/RAK_SERIAL_PORT_TOOL_V1.2.1.zip) with the AT Command below:

$plugin[{
    "type": "code-block",
    "data": {
        "languageBlocks": [
            {
                "code": "at+key_config=<key>,<frame_port>,<message>",
                "language": "none"
            }
        ]
    }
}]$

- **key** - The key you want to customize in your  RAK612 LPWAN Button
- **frame_port** - the port you want to send the customized message
- **message** - your customized message in replacement of your default message in every key pressed.

1.**Connect** your RAK612 LPWAN Button to your Windows PC using a Micro USB cable. Follow the steps in the [auto$](/rak612-lora-button/interfacing-with-rak612-lora-button) document if this is the first time you are connecting the device into your WIndows PC. 

2.Using the same RAK Serial Port Tool used in the previous step and the AT Command syntax, let us try configuring your RAK612 LPWAN Button keys. As an example, try sending the AT Command same with the image shown below:

$plugin[{
    "type": "code-block",
    "data": {
        "languageBlocks": [
            {
                "code": "at+key_config=2,37,Hello Mark Angelo!",
                "language": "none"
            }
        ]
    }
}]$

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1580395407\/17093\/opo7s3ps1yaylogh6uao.png",
        "mode": "responsive",
        "width": 459,
        "height": 604,
        "caption": "**Figure 1:** Configuring Each button"
    }
}]$

- You should be able to change the message to "**Hello Mark Angelo!**" whenever you press the key "**Key 2**". Congratulations, you have just customized your RAK612 LPWAN Button keys. Go try the other keys with your desired message!

