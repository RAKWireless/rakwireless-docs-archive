---
type: page
title: ABP Mode
listed: true
slug: ttn-abp-mode
---published

**1.** First, switch the activation method to ABP as shown in the following image:

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1580538250\/24040\/bryeyppqcyb1amkfs4po.png",
        "mode": "responsive",
        "width": 1934,
        "height": 1094,
        "caption": "**Figure 1**: APB Activation in The Things Network"
    }
}]$

**2.** These three parameters will be used on  RAK4200 LPWAN Evaluation Board: **Device Address**, **Network Session Key** and **App Session Key**.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1580538510\/24040\/ckwoomxjgqosjifk9p7z.png",
        "mode": "responsive",
        "width": 1934,
        "height": 1094,
        "caption": "**Figure 2**: ABP Parameters in The Things Network"
    }
}]$

$plugin[{
    "type": "callout",
    "data": {
        "text": "As an example, let\u2019s join in ABP\nmode, EU868 frequency, and LoRa\u00ae class is Class A.",
        "type": "info",
        "title": "Note:"
    }
}]$

**3.** If the join mode is
not in ABP Mode, just set the LoRa® join mode to **ABP** as follows:

$plugin[{
    "type": "code-block",
    "data": {
        "languageBlocks": [
            {
                "code": "at+set_config=lora:join_mode:1",
                "language": "none"
            }
        ]
    }
}]$

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1579426122\/24040\/cl6jv8cge7hzkavag3hn.jpg",
        "mode": "responsive",
        "width": 558,
        "height": 667,
        "caption": "**Figure 3**: AT Command for ABP LoRa\u00ae Join Mode via RAK Serial Port Tool"
    }
}]$

**4.** Set the LoRa® class to **Class A**:

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
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1579426153\/24040\/mmll3jdm6l9hg3jm5jy7.jpg",
        "mode": "responsive",
        "width": 560,
        "height": 675,
        "caption": "**Figure 4**: AT Command for ABP LoRa\u00ae Class via RAK Serial Port Tool"
    }
}]$

**5.** Set the frequency/region to **EU868**:

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
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1579427029\/24040\/hoxaobrwlgh6otjde6vd.jpg",
        "mode": "responsive",
        "width": 556,
        "height": 669,
        "caption": "**Figure 5**: AT Command for ABP LoRa\u00ae Region\/Frequency via RAK Serial Port Tool"
    }
}]$

**6.** Set the **Device Address**:

$plugin[{
    "type": "code-block",
    "data": {
        "languageBlocks": [
            {
                "code": "at+set_config=lora:dev_addr:XXXX",
                "language": "none"
            }
        ]
    }
}]$

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1579427130\/24040\/i5tmaceu0jqjbh3qt4po.jpg",
        "mode": "responsive",
        "width": 559,
        "height": 678,
        "caption": "**Figure 6**: AT Command for ABP LoRa\u00ae Device Address via RAK Serial Port Tool"
    }
}]$

**7.** Set the **Network Session Key**:

$plugin[{
    "type": "code-block",
    "data": {
        "languageBlocks": [
            {
                "code": "at+set_config=lora:nwks_key:XXXX",
                "language": "none"
            }
        ]
    }
}]$

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1579427136\/24040\/kc6fxzmr4ijlan1sgrh8.jpg",
        "mode": "responsive",
        "width": 557,
        "height": 665,
        "caption": "**Figure 7**: AT Command for ABP LoRa\u00ae Network Session Key via RAK Serial Port Tool"
    }
}]$

**8.** Set the **Application Session Key**:

$plugin[{
    "type": "code-block",
    "data": {
        "languageBlocks": [
            {
                "code": "at+set_config=lora:apps_key:XXXX",
                "language": "none"
            }
        ]
    }
}]$

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1579427142\/24040\/wcfzckjltpwf2n8pdobs.jpg",
        "mode": "responsive",
        "width": 556,
        "height": 676,
        "caption": "**Figure 8**: AT Command for ABP LoRa\u00ae Application Session Key via RAK Serial Port Tool"
    }
}]$

$plugin[{
    "type": "callout",
    "data": {
        "text": "After configuring all parameters, you need to reset  RAK4200 LPWAN Evaluation Board for saving parameters!",
        "type": "info",
        "title": "Note:"
    }
}]$

**9.** After resetting your  RAK4200 LPWAN Evaluation Board, join in **ABP mode**:

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
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1579427149\/24040\/mqklekitvyx1smagkvx5.jpg",
        "mode": "responsive",
        "width": 554,
        "height": 672,
        "caption": "**Figure 9**: AT Command for ABP LoRa\u00ae  Join via RAK Serial Port Tool"
    }
}]$

$plugin[{
    "type": "callout",
    "data": {
        "text": "There is no need to join in ABP mode. But you still need to set this AT command to validate the parameters which you just set for ABP mode.",
        "type": "info",
        "title": "Note:"
    }
}]$

Now, let’s try to send a data from the  RAK4200 LPWAN Evaluation Board to TTN in ABP mode.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1579427155\/24040\/hdyn5eezsmczhxvblpkn.jpg",
        "mode": "responsive",
        "width": 554,
        "height": 667,
        "caption": "**Figure 10**: OTAA Test Sample Data Sent via RAK Serial Port Tool"
    }
}]$

Then you can see that TTN has received the data you just sent.

