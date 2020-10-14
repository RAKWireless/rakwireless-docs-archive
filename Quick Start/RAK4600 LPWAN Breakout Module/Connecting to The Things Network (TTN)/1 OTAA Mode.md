---
type: page
title: OTAA Mode
listed: true
slug: otaa-mode
---published

When setting up a new device in TTN its default is to join in OTAA mode. For configuration, you need the following three parameters: **Device EUI, Application EUI** and **App Key**. You can get them all from the **Overview page**.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1588253172\/28900\/qocwypgzdu6aghafc6db.jpg",
        "mode": "responsive",
        "width": 1100,
        "height": 1008,
        "caption": "**Figure 1**: Device Overview Parameters"
    }
}]$

$plugin[{
    "type": "callout",
    "data": {
        "text": "As an example, let\u2019s join in OTAA mode, EU868 frequency and the default LoRa\u00ae\nclass is Class A.",
        "type": "info",
        "title": "Note:"
    }
}]$

$plugin[{
    "type": "callout",
    "data": {
        "text": "Execute the following commands one by one and in the\norder given.",
        "type": "info",
        "title": "Note:"
    }
}]$

**1.** Set the LoRa® join mode to
**OTAA** as follows:

$plugin[{
    "type": "code-block",
    "data": {
        "languageBlocks": [
            {
                "code": "at+set_config=lora:join_mode:0",
                "language": "none"
            }
        ]
    }
}]$

**2.** Set the LoRa® class to **Class A**:

$plugin[{
    "type": "code-block",
    "data": {
        "languageBlocks": [
            {
                "code": "at+set_config=lora:class:0",
                "language": "none"
            }
        ]
    }
}]$

**3.** Set the frequency/region to **EU868**:

$plugin[{
    "type": "code-block",
    "data": {
        "languageBlocks": [
            {
                "code": "at+set_config=lora:region:EU868",
                "language": "none"
            }
        ]
    }
}]$

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1588253246\/28900\/ozijrghaes3lthpbnbs5.png",
        "mode": "600",
        "width": 672,
        "height": 946,
        "caption": "**Figure 2**: AT Command for OTAA Join Mode, Class and Region"
    }
}]$

$plugin[{
    "type": "callout",
    "data": {
        "text": "Execute the following commands one by one and in the\norder given.",
        "type": "info",
        "title": "Note:"
    }
}]$

**4.** Set the **Device EUI.**

$plugin[{
    "type": "code-block",
    "data": {
        "languageBlocks": [
            {
                "code": "at+set_config=lora:dev_eui:XXXX",
                "language": "none"
            }
        ]
    }
}]$

**5.** Set the **Application EUI**:

$plugin[{
    "type": "code-block",
    "data": {
        "languageBlocks": [
            {
                "code": "at+set_config=lora:app_eui:XXXX",
                "language": "none"
            }
        ]
    }
}]$

**6.** Set the **Application Key**:

$plugin[{
    "type": "code-block",
    "data": {
        "languageBlocks": [
            {
                "code": "at+set_config=lora:app_key:XXXX",
                "language": "none"
            }
        ]
    }
}]$

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1588253405\/28900\/ancelvnpnwlfujeo4qac.png",
        "mode": "responsive",
        "width": 677,
        "height": 952,
        "caption": "**Figure 3**: AT Command for OTAA Device EUI, Application EUI and Application Key"
    }
}]$

**7.**Reboot the RAK4600 LPWAN Breakout Module to save the parameters.

$plugin[{
    "type": "code-block",
    "data": {
        "languageBlocks": [
            {
                "code": "at+set_config=device:restart",
                "language": "none"
            }
        ]
    }
}]$

**8.** After resetting  RAK4600 LPWAN Breakout Module, join in OTAA mode:

$plugin[{
    "type": "code-block",
    "data": {
        "languageBlocks": [
            {
                "code": "at+join",
                "language": "none"
            }
        ]
    }
}]$

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1588254229\/28900\/pnf8fwhfpstl8vbhr7xp.png",
        "mode": "responsive",
        "width": 671,
        "height": 947,
        "caption": "**Figure 4**: AT Command for OTAA LoRa\u00ae Join via RAK Serial Port Tool"
    }
}]$

**9.** Joined successfully! Now, let’s try to send a data from the  RAK4600 LPWAN Breakout Module to TTN:

$plugin[{
    "type": "code-block",
    "data": {
        "languageBlocks": [
            {
                "code": "at+send=lora:2:0123456789",
                "language": "none"
            }
        ]
    }
}]$

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1588253865\/28900\/rv9opnvsjjpayix9p0gu.png",
        "mode": "responsive",
        "width": 675,
        "height": 952,
        "caption": "**Figure 5**: OTAA Test Sample Data Sent via RAK Serial Port Tool"
    }
}]$

You can then see the data sent from  RAK4600 LPWAN Breakout Module on TTN website as follows:

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1588248687\/28894\/qjrfqg2wxiavtsccznof.png",
        "mode": "responsive",
        "width": 1116,
        "height": 481,
        "caption": "**Figure 6**: OTAA Test Sample Data Sent Viewed in The Things Network"
    }
}]$

