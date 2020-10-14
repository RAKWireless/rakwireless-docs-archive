---
type: page
title: OTAA Mode
listed: true
slug: chirpstack-otaa-mode
---published

**1.** To join ChirpStack in OTAA mode, select “**DeviceProfile_OTAA**”.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1582540095\/24858\/vy0kq5njvnuzo49ivkd5.png",
        "mode": "responsive",
        "width": 1912,
        "height": 1093,
        "caption": "**Figure 1:** Selecting OTAA Activation Mode in ChirpStack"
    }
}]$

**2.** Press “**CREATE DEVICE**” button. You may write the application key by yourself or generate it automatically by clicking the icon highlighted in the image.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1582540114\/24858\/ojwnskkac1njlitkurvr.png",
        "mode": "responsive",
        "width": 1934,
        "height": 1094,
        "caption": "**Figure 2:** Application Key Generation"
    }
}]$

**3.** Click "**SET DEVICE KEYS**” button. Now, you’ve completed the configuration on ChirpStack.

- The Device EUI which was set in the previous section to your RAK811 LPWAN Breakout Module as "dev_eui" is the same in the image highlighted below.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1582540124\/24858\/tvgeeoltqkzdne3ya5qw.png",
        "mode": "responsive",
        "width": 1934,
        "height": 1094,
        "caption": "**Figure 3:** Device EUI Code"
    }
}]$

- Same with the Application Key, which was set in the previous section as "app_key" is the same with the image highlighted.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1582540133\/24858\/j0gh8yxjinczq4m7rxo1.png",
        "mode": "responsive",
        "width": 1934,
        "height": 1094,
        "caption": "**Figure 4:** Application Key LoRaWAN\u00ae"
    }
}]$

$plugin[{
    "type": "callout",
    "data": {
        "text": "The Application EUI which was into RAK811 LPWAN Breakout Module as \u201c**app_eui**\u201d is not needed for ChirpStack.",
        "type": "info",
        "title": "Note:"
    }
}]$

**4.** Next, let’s **configure** RAK811 LPWAN Breakout Module by using **AT commands**. To do this, connect your RAK811 LPWAN Breakout Module to a PC, power it on and open **RAK Serial Port Tool** on your computer.

$plugin[{
    "type": "code-block",
    "data": {
        "languageBlocks": [
            {
                "code": "at+version",
                "language": "none"
            }
        ]
    }
}]$

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1579396158\/17310\/fqw3e70otnu8ymgnmu79.png",
        "mode": "300",
        "width": 682,
        "height": 865,
        "caption": "**Figure 5:** RAK Serial Port Tool"
    }
}]$

- Now, let us join our RAK811 using the OTAA activation mode.

**5.** If the join mode is not in OTAA, just set the LoRa® join mode to **OTAA** and LoRa® class to **Class A** by typing the AT commands shown in the picture below.

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
                "code": "at+set_config-lora:class:0",
                "language": "none"
            }
        ]
    }
}]$

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1579440795\/24811\/mdjpe1uhxdmahhthbt8w.jpg",
        "mode": "responsive",
        "width": 1358,
        "height": 865,
        "caption": "**Figure 6:** Setting of LoRaWAN\u00ae mode and class"
    }
}]$

**6.** Type the following AT command to set the:**Frequency/Region, Device EUI, Application EUI and Application Key.** Remember to replace "**XXX"** and "**XXXX"** with the parameters set in the previous steps.

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
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1579441032\/24811\/vugtbybavkertynte382.jpg",
        "mode": "responsive",
        "width": 1364,
        "height": 867,
        "caption": "**Figure 7:** Setting of Frequency and Device EUI"
    }
}]$

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1579521974\/24811\/rkeautvpyyd4oquhxvgq.jpg",
        "mode": "responsive",
        "width": 1366,
        "height": 868,
        "caption": "**Figure 8:** Setting of Application EUI and Key"
    }
}]$

**7.** Then, **join** in OTAA mode.

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
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1579440539\/24811\/xlebk2u3xe2ryxo5ss11.png",
        "mode": "300",
        "width": 681,
        "height": 862,
        "caption": "**Figure 9:** Joining in OTAA"
    }
}]$

- **Joined Successfully!**

**8.** You can view the "**JoinRequest**" and "**JoinAccept**" on ChirpStack page:

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1582540151\/24858\/ll6wmv6jqlnyhpxgaovj.png",
        "mode": "responsive",
        "width": 1934,
        "height": 1094,
        "caption": "**Figure 10:** Join Request of the Device in the ChirpStack"
    }
}]$

**9.** Let’s try sending data from our RAK811 LPWAN Breakout Module to the ChirpStack by typing the command below in the serial port.

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
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1579441103\/24811\/j7c4lszbgth963mh6kea.png",
        "mode": "300",
        "width": 680,
        "height": 864,
        "caption": "**Figure 11:** Sending Data to ChirpStack"
    }
}]$

You can see the message on ChirpStack page:

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1582540162\/24858\/ovefavt84zya1aepa2kk.png",
        "mode": "responsive",
        "width": 1934,
        "height": 1094,
        "caption": "**Figure 12:** Message Received in ChirpStack"
    }
}]$

