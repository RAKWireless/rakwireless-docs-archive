---
type: page
title: OTAA Mode
listed: true
slug: ttn-otaa-mode
---published

When setting up a new device in TTN it defaults to OTAA mode. For configuring it, you need the following three parameters: **Device EUI, Application EUI** and **App Key**. You can get them all from the **Overview page**.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1580631582\/17850\/nt8drr212njdt10py0db.png",
        "mode": "responsive",
        "width": 1934,
        "height": 1094,
        "caption": "**Figure 1:** Device OTAA Parameters"
    }
}]$

Now, let's join in OTAA Mode and set your device to AU915 Frequency for example.

$plugin[{
    "type": "callout",
    "data": {
        "text": "The default LoRa\u00ae work mode is LoRaWAN\u00ae 1.0.2, the default LoRa\u00ae join mode is OTAA, and the default LoRa\u00ae class is Class A.For the full list of AT Commands, head on to [auto$](\/rak7200-lora-tracker\/configuring-the-rak7200-lora-tracker-using-at-commands).",
        "type": "info",
        "title": "Note"
    }
}]$

 1.Set mode to **OTAA** and LoRa® device class to **Class A**, with the following set of commands:

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
    "type": "code-block",
    "data": {
        "languageBlocks": [
            {
                "code": "at+set_config=lora:region:AU915",
                "language": "none"
            }
        ]
    }
}]$

`

`

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1579611871\/17850\/bnax7ppemxgzwzwzibmw.jpg",
        "mode": "responsive",
        "width": 555,
        "height": 676,
        "caption": "**Figure 2:** Setting up the RAK7200 Operation Mode"
    }
}]$

2.Now that the modes are set, enter the parameters: : **Device EUI, Application EUI** and **App Key**. Use the commands below. Remember to replace the **"XXXX"** with the corresponding parameter value for your particular case:

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
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1579944984\/17850\/u6bvilfgirchkipjzcvm.jpg",
        "mode": "responsive",
        "width": 551,
        "height": 676,
        "caption": "**Figure 3:** Setting up the RAK7200 OTAA Parameters"
    }
}]$

- You should end up with a window as the one in **Figure 3** above (**a series of OK messages**).

3.Finally execute the join command:

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
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1579945180\/17850\/fbrritkvpvvzvl69xosg.jpg",
        "mode": "responsive",
        "width": 552,
        "height": 676,
        "caption": "**Figure 4:** Join Command"
    }
}]$

4.Go to the **Device Overview** in the TTN and you can see that the status is now **Green (Online)**. Now your RAK7200 is transmitting sensor data to TTN. You can see it in its raw form in TTN, by going to the Data tab:

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1580631250\/17850\/qw27owcgw812gsf2bcc1.png",
        "mode": "responsive",
        "width": 1910,
        "height": 886,
        "caption": "**Figure 5:** Device Application Data"
    }
}]$

