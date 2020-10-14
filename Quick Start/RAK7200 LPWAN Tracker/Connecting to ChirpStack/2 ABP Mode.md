---
type: page
title: ABP Mode
listed: true
slug: chirpstack-abp-mode
---published

1.If you select “**Device Profile ABP**” or “**DeviceProfile_ABP_CN470**”, it means you want to join ChirpStack in **ABP mode**.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1580632951\/24878\/aonljar59ifcml3havu9.png",
        "mode": "responsive",
        "width": 1909,
        "height": 1093,
        "caption": "**Figure 1:** Switching to ABP Mode"
    }
}]$

2.Then you can see that there are some parameters for ABP in the “**ACTIVATION**” item:

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1580632963\/24878\/pknfpadcpuhqunctcga8.png",
        "mode": "responsive",
        "width": 1909,
        "height": 1094,
        "caption": "**Figure 2:** ABP Parameters"
    }
}]$

3.Next, let’s use these parameters to set RAK7200 by using **AT command**.

4.If the join mode is not in ABP, just set the LoRa® join mode to **ABP** and LoRa® class to **Class A** by typing the following commands in RAK Serial Port Tool

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1579615156\/24878\/b4vtsesbjmk5bxdjljaa.jpg",
        "mode": "responsive",
        "width": 1356,
        "height": 840,
        "caption": "**Figure 3:** Setting of LoRaWAN\u00ae Mode and Class"
    }
}]$

5.Type the following AT command to set your respective: **Frequency/Region**, **Device Address**, **Network Session Key** and **App Session Key**.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1579615175\/24878\/hhvjx9shtfon4bnrh4x1.jpg",
        "mode": "responsive",
        "width": 1356,
        "height": 840,
        "caption": "**Figure 4:** Setting of Frequency and Device Address"
    }
}]$

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1579615199\/24878\/bcslebohju0ibvhcdyms.jpg",
        "mode": "responsive",
        "width": 1356,
        "height": 840,
        "caption": "**Figure 5:** Setting of Device EUI and Network Key"
    }
}]$

- Then Join in ABP Mode

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1579615214\/24878\/vzv9ljxqw7ayfbsyok6y.jpg",
        "mode": "responsive",
        "width": 692,
        "height": 834,
        "caption": "**Figure 6:** Joining of ABP"
    }
}]$

You can see the data which is just sent from RAK7200 on ChirpStack page:

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1580632988\/24878\/catrg6l4uscykpdy32rz.png",
        "mode": "responsive",
        "width": 1934,
        "height": 1094,
        "caption": "**Figure 7:**  Message Status in ChirpStack"
    }
}]$

