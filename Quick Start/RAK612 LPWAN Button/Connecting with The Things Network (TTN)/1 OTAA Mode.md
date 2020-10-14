---
type: page
title: OTAA Mode
listed: true
slug: otaa-mode
---published

According to **The Things Network, Over-the-Air Activation** (OTAA) is the preferred and most secure way to connect with The Things Network. Thus, it is chosen as the default method when registering a device.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1580634670\/17091\/pus4rdk31ilp5fkwf2sl.png",
        "mode": "responsive",
        "width": 1934,
        "height": 1094,
        "caption": "**Figure 1:** Activation Method - OTAA"
    }
}]$

$plugin[{
    "type": "callout",
    "data": {
        "text": "As an example, let's join in OTAA mode and EU868 frequency.",
        "type": "info",
        "title": "Note:"
    }
}]$

1.Set the LoRa® join mode to **OTAA** as follows:

$plugin[{
    "type": "code-block",
    "data": {
        "languageBlocks": [
            {
                "code": "at+set_config=join_mode:1",
                "language": "none"
            }
        ]
    }
}]$

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1580492731\/17091\/wvnonumilcnjr3eqhv9t.jpg",
        "mode": "responsive",
        "width": 569,
        "height": 717,
        "caption": "**Figure 2**: AT Command for OTAA LoRa\u00ae Join Mode via RAK Serial Port Tool"
    }
}]$

2.Set the frequency/region to **EU868**:

$plugin[{
    "type": "code-block",
    "data": {
        "languageBlocks": [
            {
                "code": "at+band=EU868",
                "language": "none"
            }
        ]
    }
}]$

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1580492802\/17091\/kd2g5fbinnosyf3x9tir.jpg",
        "mode": "responsive",
        "width": 572,
        "height": 721,
        "caption": "**Figure 3**: AT Command for OTAA LoRa\u00ae Region\/Frequency via RAK Serial Port Tool"
    }
}]$

3.Set the **Device EUI.**

$plugin[{
    "type": "code-block",
    "data": {
        "languageBlocks": [
            {
                "code": "at+set_config=dev_eui:XXXX",
                "language": "none"
            }
        ]
    }
}]$

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1580494141\/17091\/hiwjx9epabmbk7bup8wx.jpg",
        "mode": "responsive",
        "width": 569,
        "height": 717,
        "caption": "**Figure 4**: AT Command for OTAA LoRa\u00ae Device EUI via RAK Serial Port Tool"
    }
}]$

4.Set the **Application EUI**:

$plugin[{
    "type": "code-block",
    "data": {
        "languageBlocks": [
            {
                "code": "at+set_config=app_eui:XXXX",
                "language": "none"
            }
        ]
    }
}]$

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1580494460\/17091\/rijbsaqitijyh7bgbyy1.jpg",
        "mode": "responsive",
        "width": 560,
        "height": 715,
        "caption": "**Figure 5:** AT Command for OTAA LoRa\u00ae Application EUI via RAK Serial Port Tool"
    }
}]$

5.Set the **Application Key**:

$plugin[{
    "type": "code-block",
    "data": {
        "languageBlocks": [
            {
                "code": "at+set_config=app_key:XXXX",
                "language": "none"
            }
        ]
    }
}]$

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1580494558\/17091\/uiwsm5mgnxjy1curwzfg.jpg",
        "mode": "responsive",
        "width": 560,
        "height": 713,
        "caption": "**Figure 6**: AT Command for OTAA LoRa\u00ae Application Key via RAK Serial Port Tool"
    }
}]$

$plugin[{
    "type": "callout",
    "data": {
        "text": "After configuring all the parameters, you need to reset your RAK612 LPWAN Button for saving parameters.",
        "type": "info",
        "title": "Note:"
    }
}]$

6.After resetting RAK612 LPWAN Button, join in OTAA mode:

$plugin[{
    "type": "code-block",
    "data": {
        "languageBlocks": [
            {
                "code": "at+join=otaa",
                "language": "none"
            }
        ]
    }
}]$

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1580494756\/17091\/m2wbm5gbcedynt9vn46b.jpg",
        "mode": "responsive",
        "width": 563,
        "height": 717,
        "caption": "**Figure 7**: AT Command for OTAA LoRa\u00ae Join via RAK Serial Port Tool"
    }
}]$

7.Joined successfully! Now, let’s try to send a data to TTN. Try pressing any key on your RAK612 LPWAN Button. You should see any data printed in the RAK Serial Port Tool whenever you press any key same as with the image below:

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1580495094\/17091\/bfbuudtrwada6kcrzrfc.jpg",
        "mode": "responsive",
        "width": 569,
        "height": 713,
        "caption": "**Figure 8**: Testing the RAK612 LPWAN Button in RAK Serial Port Tool"
    }
}]$

You can then see the data sent from RAK612 LPWAN BUtton in TTN website as follows:

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1580635031\/17091\/hrfjtdrenpsxcx0hscds.jpg",
        "mode": "responsive",
        "width": 1818,
        "height": 476,
        "caption": "**Figure 9**: OTAA Test Sample Data Sent Viewed in The Things Network"
    }
}]$

