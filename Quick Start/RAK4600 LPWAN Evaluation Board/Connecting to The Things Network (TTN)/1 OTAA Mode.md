---
type: page
title: OTAA Mode
listed: true
slug: ttn-otaa-mode
---published

When setting up a new device in TTN its defaults is to join in OTAA mode. For configuration, you need the following three parameters: **Device EUI, Application EUI** and **App Key**. You can get them all from the **Overview page**.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1580617492\/22601\/y897soyva7uv78ai5iyi.png",
        "mode": "responsive",
        "width": 1934,
        "height": 1094,
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

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1579425471\/24039\/ugvheykwbjgqrmve3gr1.jpg",
        "mode": "responsive",
        "width": 559,
        "height": 675,
        "caption": "**Figure 2**: AT Command for OTAA LoRa\u00ae Join Mode via RAK Serial Port Tool"
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

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1579425063\/24039\/uwdcbt0uegx9s5nacmdh.jpg",
        "mode": "responsive",
        "width": 553,
        "height": 667,
        "caption": "**Figure 3**: AT Command for OTAA LoRa\u00ae Class via RAK Serial Port Tool"
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
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1579425544\/24039\/iuxsdncululn7d4ywcis.jpg",
        "mode": "responsive",
        "width": 553,
        "height": 674,
        "caption": "**Figure 4**: AT Command for OTAA LoRa\u00ae Region\/Frequency via RAK Serial Port Tool"
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

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1579425574\/24039\/pu2digmbwm9tms4h3mtm.jpg",
        "mode": "responsive",
        "width": 545,
        "height": 673,
        "caption": "**Figure 5**: AT Command for OTAA LoRa\u00ae Device EUI via RAK Serial Port Tool"
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

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1579425617\/24039\/k2nhwyd1ctfx6gjwuboz.jpg",
        "mode": "responsive",
        "width": 554,
        "height": 669,
        "caption": "**Figure 6:** AT Command for OTAA LoRa\u00ae Application EUI via RAK Serial Port Tool"
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
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1579425800\/24039\/rv7qwzhicwokmmgxcawf.jpg",
        "mode": "responsive",
        "width": 559,
        "height": 677,
        "caption": "**Figure 7**: AT Command for OTAA LoRa\u00ae Application Key via RAK Serial Port Tool"
    }
}]$

$plugin[{
    "type": "callout",
    "data": {
        "text": "After\nconfiguring all parameters, you need to reset  RAK4600 LPWAN Evaluation Board for saving parameters!",
        "type": "info",
        "title": "Note:"
    }
}]$

**7.** After resetting  RAK4600 LPWAN Evaluation Board, join in OTAA mode:

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
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1579425807\/24039\/mgztynrigiozealhlv6t.jpg",
        "mode": "responsive",
        "width": 554,
        "height": 675,
        "caption": "**Figure 8**: AT Command for OTAA LoRa\u00ae Join via RAK Serial Port Tool"
    }
}]$

**8.** Joined successfully! Now, let’s try to send a data from the  RAK4600 LPWAN Evaluation Board to TTN:

$plugin[{
    "type": "code-block",
    "data": {
        "languageBlocks": [
            {
                "code": "at+send=lora:2:1234567890",
                "language": "none"
            }
        ]
    }
}]$

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1579425813\/24039\/drwvcagphdvkbt8kefnc.jpg",
        "mode": "responsive",
        "width": 554,
        "height": 666,
        "caption": "**Figure 9**: OTAA Test Sample Data Sent via RAK Serial Port Tool"
    }
}]$

You can then see the data sent from  RAK4600 LPWAN Evaluation Board on TTN website as follows:

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1579425137\/24039\/vdrrdeh7oifamkrwvryn.jpg",
        "mode": "responsive",
        "width": 1803,
        "height": 603,
        "caption": "**Figure 10**: OTAA Test Sample Data Sent Viewed in The Things Network"
    }
}]$

