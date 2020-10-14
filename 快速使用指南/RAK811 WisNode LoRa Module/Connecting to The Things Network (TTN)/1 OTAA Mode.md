---
type: page
title: OTAA Mode
listed: true
slug: otaa-mode
---published

When setting up a new device in TTN it defaults to OTAA mode. For configuring it you need the following three parameters: **Device EUI, Application EUI** and **App Key**. You can get them all from the **Overview page**.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1563148174\/17642\/hp0k37y97newmavgmo0b.jpg",
        "mode": "full",
        "width": 1834,
        "height": 858,
        "caption": "**Figure 10**. Device OTAA Parameters"
    }
}]$

Now, let us configure the RAK811 to work in OTAA mode in the EU868 band, as an example.

$plugin[{
    "type": "callout",
    "data": {
        "text": "The default LoRa working mode for the RAK811 is LoRaWAN 1.0.2, while the default LoRa join mode is OTAA, and the default LoRa class is Class A. This is how the",
        "type": "info",
        "title": "Info"
    }
}]$

1.Set mode to **OTAA** and LoRa device class to **Class A**, with the following set of commands:

$plugin[{
    "type": "code-block",
    "data": {
        "languageBlocks": [
            {
                "code": "at+set_config=lora:join_mode:0\nat+set_config=lora:class:0",
                "language": "javascript"
            }
        ]
    }
}]$

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1563151058\/17642\/em8x3n0kmyiav87nllo1.jpg",
        "mode": "responsive",
        "width": 903,
        "height": 584,
        "caption": "**Figure 2.** Setting up the RAK811 operation mode"
    }
}]$

2.Now that the modes are set, enter the parameters: : **Device EUI, Application EUI** and **App Key**. Use the commands below. Remember to replace the **"XXXX"** with the corresponding parameter value for your particular case:

$plugin[{
    "type": "code-block",
    "data": {
        "languageBlocks": [
            {
                "code": "at+set_config=lora:dev_eui:XXXX\nat+set_config=lora:app_eui:XXXX\nat+set_config=lora:app_key:XXXX",
                "language": "javascript"
            }
        ]
    }
}]$

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1563152655\/17642\/bbekinoezhrnlqo2wli6.jpg",
        "mode": "responsive",
        "width": 902,
        "height": 589,
        "caption": "**Figure 3.** Setting up the RAK811 OTAA parameters"
    }
}]$

You should end up with a window as the one in **Figure 2** above (**a series of OK messages**).

3.Finally execute the join command:

$plugin[{
    "type": "code-block",
    "data": {
        "languageBlocks": [
            {
                "code": "at+join",
                "language": "javascript"
            }
        ]
    }
}]$

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1563152887\/17642\/fgjesw2ldqd4e3bjgczx.jpg",
        "mode": "responsive",
        "width": 904,
        "height": 587,
        "caption": "**Figure 4.** Join command"
    }
}]$

4.You can test the connection by sending an uplink frame. Use the following for example:

$plugin[{
    "type": "code-block",
    "data": {
        "languageBlocks": [
            {
                "code": "at+send=lora:1:12345678",
                "language": "javascript"
            }
        ]
    }
}]$

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1563154622\/17642\/erd11ri6reuy39djicnc.jpg",
        "mode": "responsive",
        "width": 905,
        "height": 588,
        "caption": "**Figure 5.** Sending an uplink frame"
    }
}]$

If you get a response in your TTN live data feed as in Figure 6, than you are all set!

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1563154815\/17642\/fkkambqytxahosgflci4.jpg",
        "mode": "responsive",
        "width": 1097,
        "height": 670,
        "caption": "**Figure 6.** Sending Data to TTN from RAK811"
    }
}]$

