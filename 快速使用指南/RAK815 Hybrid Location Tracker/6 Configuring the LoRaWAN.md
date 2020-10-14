---
type: page
title: Configuring the LoRaWAN
listed: true
slug: configuring-the-lorawan
---published

### Project Structure

Because IAR 8.11 and Keil5 has similar project structure, we will be using the IAR 8.11 structure throughout the configuration settings.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1561966703\/16604\/cdann0gkbb3tt0to83bc.jpg",
        "mode": "300",
        "width": 717,
        "height": 1092,
        "caption": "Figure 1. IAR Project Structure"
    }
}]$

### Application Switch

In the open source project, there are three application cases. Users only need to replace
the main.c and app_lora.c files in the project to switch between different applications. 

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1561967707\/16604\/zrqqgs1ddu8vhxtyiryg.jpg",
        "mode": "responsive",
        "width": 1245,
        "height": 737,
        "caption": "Figure 2. Switching Applications in IAR"
    }
}]$

The applications are made available in the open source code by clicking this file directory: `RAK813-BreakBoard-master>>Doc>>hex`

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1561967609\/16604\/tkti6jf3bukcjrlzxxpk.jpg",
        "mode": "responsive",
        "width": 812,
        "height": 380,
        "caption": "Figure 3. Application Demo Directory"
    }
}]$

### Configuration of LoRaWAN Parameters

This Board can be connected to LoRaWAN through Over-the-Air-Activation(OTAA) or Activation-By-Personalization(ABP) activation modes. This can be modified through the **Commissioning.h file** available in the open source code

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1561968852\/16604\/nsiycikj66hmfrzyuk8q.jpg",
        "mode": "responsive",
        "width": 1245,
        "height": 635,
        "caption": "Figure 4. Configuring LoRaWAN Activation Mode in OTAA"
    }
}]$

Along with the following parameters: **Device EUI, Application EUI, App Key** for OTAA; **Device Address, Network Address and Application key** for ABP.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1561968949\/16604\/gl9rlllwpgg4r3kqfmsh.jpg",
        "mode": "responsive",
        "width": 1242,
        "height": 638,
        "caption": "Figure 5. Configuring Application Parameters"
    }
}]$

### Modify LoRaWAN Region

The open source code is based on LoRaWAN1.0.2 modified from, so the supported
regions have: **EU868, US915, AS923, AU915, IN865, KR920**. If you want to modify the
region, you can modify the macro definition.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1561969073\/16604\/j7757n5faaqb0zd5ysbi.jpg",
        "mode": "responsive",
        "width": 918,
        "height": 804,
        "caption": "Figure 6. Modifying the LoRaWAN Region in IAR"
    }
}]$

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1561969109\/16604\/e0isoohrsxu0josllk0r.jpg",
        "mode": "responsive",
        "width": 1009,
        "height": 753,
        "caption": "Figure 7. Modifying the LoRaWAN Region in Keil"
    }
}]$

Now, you have successfully modified your LoRaWAN parameters.

