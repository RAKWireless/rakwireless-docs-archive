---
type: page
title: OTAA Mode
listed: true
slug: chirpstack-otaa-mode
---published

**1.** If you select “**device_profile_otaa**”, it means you want to join ChirpStack in **OTAA mode**.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1580572117\/22604\/xhkn525b4hoeohzxuajh.png",
        "mode": "responsive",
        "width": 1934,
        "height": 1094,
        "caption": "**Figure 1**: Chirpstack OTAA Activation"
    }
}]$

**2.** Click “**CREATE DEVICE**” then generate the application key in this page. You can write it by yourself or generate it automatically by clicking the following icon and press “**SET DEVICE-KEYS**”.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1580572127\/22604\/xggfwxe1m4jnngkeej4y.png",
        "mode": "responsive",
        "width": 1934,
        "height": 1094,
        "caption": "**Figure 2**: Chirpstack OTAA Set Device Keys"
    }
}]$

**3.** Set the **Device EUI** for the RAK4600 LPWAN Evaluation Board using the "**dev_eui**" same with the image below:

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1580572138\/22604\/xvbsa9x8ews64lagkg4c.png",
        "mode": "responsive",
        "width": 1934,
        "height": 1094,
        "caption": "**Figure 3**: Chirpstack OTAA Set Device EUI"
    }
}]$

**4.** Set the **Application Key** for the RAK4600 LPWAN Evaluation Board using the "**app_key**" same with the image below:

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1580572200\/22604\/iei9la4tqzofvucrfote.jpg",
        "mode": "responsive",
        "width": 1920,
        "height": 1080,
        "caption": "**Figure 4**: Chirpstack OTAA Set Application Key"
    }
}]$

$plugin[{
    "type": "callout",
    "data": {
        "text": "The Application EUI which will be set into RAK4600 LPWAN Evaluation Board as \u201capp_eui\u201d is not necessary for ChirpStack, and you can set it to any value with a correct format.",
        "type": "info",
        "title": "Note:"
    }
}]$

**5.** Configure RAK4600 LPWAN Evaluation Board by using the available AT Commands found in this [section](/rak4600-lora-evaluation-board/at-commands-for-rak4600). Connect your RAK4600 LPWAN Evaluation Board in your Windows Machine.

**6.** Power it **ON** and open **RAK Serial Port Tool** on your PC as instructed [here](/rak4200-lora-evaluation-board/interfacing-with-rak4200-lora-evaluation-board).

$plugin[{
    "type": "callout",
    "data": {
        "text": "The default join mode is **OTAA**, the default class is **Class A** and the default region is **EU868**.",
        "type": "info",
        "title": "Note:"
    }
}]$

**7.** If the **join mode** is not in OTAA, just set the LoRa® join mode to **OTAA** as follows:

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
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1579528394\/24042\/mrydatc2hlwrxiyjpoqw.jpg",
        "mode": "responsive",
        "width": 557,
        "height": 681,
        "caption": "**Figure 5**: Chirpstack OTAA Join Mode via RAK Serial Port Tool"
    }
}]$

**8.** Set the LoRa® class to **Class A**:

$plugin[{
    "type": "code-block",
    "data": {
        "languageBlocks": [
            {
                "code": "at+set_config-lora:class:0",
                "language": "none"
            }
        ]
    }
}]$

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1579528402\/24042\/edffrutqfohfxvhz0su8.jpg",
        "mode": "responsive",
        "width": 547,
        "height": 662,
        "caption": "**Figure 6**: Chirpstack OTAA Set Class via RAK Serial Port Tool"
    }
}]$

**9.** Set the frequency/region to **EU868**:

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
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1579528409\/24042\/evudoedib3ovd9ye98gy.jpg",
        "mode": "responsive",
        "width": 554,
        "height": 675,
        "caption": "**Figure 7**: Chirpstack OTAA Set Region\/Frequency via RAK Serial Port Tool"
    }
}]$

**10.** Set the **Device EUI**:

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
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1579528416\/24042\/vsbevdit52xkqq0ocn5n.jpg",
        "mode": "responsive",
        "width": 554,
        "height": 671,
        "caption": "**Figure 8**: Chirpstack OTAA Set Device EUI via RAK Serial Port Tool"
    }
}]$

**11.** Set the **Application EUI**:

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
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1579528423\/24042\/yzqpmzjhqj58akm7xqcm.jpg",
        "mode": "responsive",
        "width": 552,
        "height": 670,
        "caption": "**Figure 9**: Chirpstack OTAA Set Application EUI via RAK Serial Port Tool"
    }
}]$

**12.** Set the **Application Key**:

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
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1579528429\/24042\/uf6hawlomc92hhp2dlbl.jpg",
        "mode": "responsive",
        "width": 551,
        "height": 676,
        "caption": "**Figure 10**: Chirpstack OTAA Set Application Key via RAK Serial Port Tool"
    }
}]$

$plugin[{
    "type": "callout",
    "data": {
        "text": "After configuring all parameters, you need to reset RAK4600 LPWAN Evaluation Board for saving parameters!",
        "type": "info",
        "title": "Note:"
    }
}]$

**13.** After resetting, start
to join:

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
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1579528435\/24042\/kp0hhztd0d1txr0xlsnd.jpg",
        "mode": "responsive",
        "width": 556,
        "height": 675,
        "caption": "**Figure 11**: Chirpstack OTAA Join via RAK Serial Port Tool"
    }
}]$

**14.** You can then see the **JoinRequest** and **JoinAccept** on ChirpStack page:

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1580573024\/22604\/uupd1tzdxylviuomb8xu.png",
        "mode": "responsive",
        "width": 1934,
        "height": 1094,
        "caption": "**Figure 12**: Chirpstack OTAA JoinRequest and JoinAccept"
    }
}]$

**15.** Let’s try to send a data from RAK4600 LPWAN Evaluation Board to ChirpStack:

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
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1579528442\/24042\/sy4nezodryajjldti9ki.jpg",
        "mode": "responsive",
        "width": 562,
        "height": 673,
        "caption": "**Figure 13**: Chirpstack OTAA Sample Data Sent via RAK Serial Port Tool"
    }
}]$

- You can then see the message on ChirpStack page:

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1580572918\/22604\/zwyl9ithjrhyluctkjpz.png",
        "mode": "responsive",
        "width": 1934,
        "height": 1094,
        "caption": "**Figure 14**: Chirpstack Data Received Preview"
    }
}]$

OK, that’s all about “Join in OTAA Mode” with ChirpStack.

