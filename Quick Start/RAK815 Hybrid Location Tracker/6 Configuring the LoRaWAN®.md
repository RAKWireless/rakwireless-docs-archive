---
type: page
title: Configuring the LoRaWAN®
listed: true
slug: configuring-the-lorawan
---published

### Project Structure

Because IAR 8.11 and Keil5 has similar project structure, we will be using the IAR 8.11 structure throughout the configuration settings. Visit the [IAR Embedded Workbench IDE](https://www.iar.com/iar-embedded-workbench/#!?architecture=Arm)'s website to know more.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1579656689\/16604\/khctqasrsbw7rmxirvzr.jpg",
        "mode": "300",
        "width": 731,
        "height": 1106,
        "caption": "**Figure 1:** IAR Project Structure"
    }
}]$

### Application Switch

In the [GitHub Open Source](https://github.com/RAKWireless/RAK813-BreakBoard/tree/master/Apps) projects, there are three application cases. Users only need to replace
the **main.c** and **app_lora.c** files in the project to switch between different applications. 

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1579656704\/16604\/fjla2yfati4igeiflxnw.jpg",
        "mode": "responsive",
        "width": 1259,
        "height": 751,
        "caption": "**Figure 2:** Switching Applications in IAR"
    }
}]$

The applications are made available in the open source code by clicking this file directory: `RAK813-BreakBoard-master>>Doc>>hex`

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1579656723\/16604\/u5tglrhn1gy7k9so7ah7.jpg",
        "mode": "responsive",
        "width": 826,
        "height": 394,
        "caption": "**Figure 3:** Application Demo Directory"
    }
}]$

### Configuration of LoRaWAN® Parameters

This Board can be connected to LoRaWAN® through **Over-the-Air-Activation(OTAA)** or **Activation-By-Personalization(ABP)** activation modes. This can be modified through the **Commissioning.h file** available in the open source code

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1579656745\/16604\/nyxlkbrpkbjsfaie6crn.jpg",
        "mode": "responsive",
        "width": 1259,
        "height": 649,
        "caption": "**Figure 4:** Configuring LoRaWAN\u00ae Activation Mode in OTAA"
    }
}]$

Along with the following parameters: **Device EUI, Application EUI, App Key** for OTAA; **Device Address, Network Address and Application key** for ABP.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1579656754\/16604\/bywqof0mo5wmobaznwhb.jpg",
        "mode": "responsive",
        "width": 1256,
        "height": 652,
        "caption": "**Figure 5:** Configuring Application Parameters"
    }
}]$

### Modify LoRaWAN® Region

The open source code is based on LoRaWAN® 1.0.2 modified from, so the supported
regions have: **EU868, US915, AS923, AU915, IN865, KR920**. If you want to modify the
region, you can modify the macro definition.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1579656766\/16604\/ekvepzjgpbfeyiemc8qg.jpg",
        "mode": "responsive",
        "width": 932,
        "height": 818,
        "caption": "**Figure 6:** Modifying the LoRaWAN\u00ae Region in IAR"
    }
}]$

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1579656777\/16604\/urhaiznldn60idrad6xm.jpg",
        "mode": "responsive",
        "width": 1023,
        "height": 767,
        "caption": "**Figure 7:** Modifying the LoRaWAN\u00ae Region in Keil"
    }
}]$

Now, you have successfully modified your LoRaWAN® parameters.

