---
type: page
title: Customizing the Function of 4 Keys
listed: true
slug: customizing-the-function-of-4-keys
---published

If you have installed Version 2.00.2.1.2 firmware and above on your RAK612 LoRa button, you can customize the message freely for every key.

By default:

1. When you Press Key 1, it will send "Key 1"
2. When you Press Key 2, it will send "Key 2"
3. When you Press Key 3, it will send "Key 3"
4. When you Press Key 4, it will send "Key 4"

Using the RAK Serial Port Tool, you can change it using the following AT Command:
`at+key_config=2,37,Hello Mark Angelo!`

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1561828858\/17093\/tk5izfilyzddi42kp4pb.png",
        "mode": "responsive",
        "width": 445,
        "height": 590,
        "caption": "**Figure 1:** Configuring Each button"
    }
}]$

where:

- **2** - is the key that you want to customize
- **37** - is the Frame Port the button is going to send the message on
- **Hello Mark Angelo!** - is the text that you want to send when you will press the button

