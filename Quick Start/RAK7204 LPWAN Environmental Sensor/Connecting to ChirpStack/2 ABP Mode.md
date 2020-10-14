---
type: page
title: ABP Mode
listed: true
slug: chirpstack-abp-mode
---published

1.If you select “**Device Profile  ABP**” or “**DeviceProfile_ABP_CN470**”, it means you want to join ChirpStack in **ABP mode**.

$plugin[{
    "type": "callout",
    "data": {
        "text": "Frequency AS923 in ABP Mode is not supported in ChirpStack",
        "type": "warning",
        "title": "Warning:"
    }
}]$

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1582559880\/24884\/ezfbaa2iue5jolxhcn5m.png",
        "mode": "responsive",
        "width": 1909,
        "height": 1093,
        "caption": "**Figure 1:** Switching to ABP Mode"
    }
}]$

**2.** Then you can see that there are some parameters for ABP in the “**ACTIVATION**” item:

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1582559889\/24884\/z1ox6hvoa4zwe8cpadz5.png",
        "mode": "responsive",
        "width": 1909,
        "height": 1094,
        "caption": "**Figure 2:** ABP Parameters"
    }
}]$

**3.** Next, let’s use these parameters to set WisNode LoRa® by using **AT command**. Let's join in **ABP** mode and set **EU868** frequency as an example.

**4.** If the join mode is not in ABP, just set the LoRa® join mode to **ABP** and LoRa® a class to **Class A** by typing the following commands in RAK Serial Port Tool

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1579522241\/24812\/dkulqzpldm5nlpsjhbyz.jpg",
        "mode": "responsive",
        "width": 1366,
        "height": 869,
        "caption": "**Figure 3:** Setting of LoRaWAN\u00ae Mode and Class"
    }
}]$

5.Type the following AT command to set your respective: **Frequency/Region**, **Device Address**, **Network Session Key** and **App Session Key**.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1579522359\/24812\/lvccenrrczmt4nrtbjya.jpg",
        "mode": "responsive",
        "width": 1367,
        "height": 868,
        "caption": "**Figure 4:** Setting of Frequency and Device Address"
    }
}]$

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1579522542\/24812\/v1mclxe7vemha0yewfyu.jpg",
        "mode": "responsive",
        "width": 1367,
        "height": 872,
        "caption": "**Figure 5:** Setting of Device EUI and Network Session Key"
    }
}]$

6.Then, **join** in ABP mode.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1579522735\/24812\/pqwlq93vihikp0rgilvi.jpg",
        "mode": "300",
        "width": 679,
        "height": 865,
        "caption": "**Figure 6:** Joining of ABP"
    }
}]$

- Now, try sending data from our WisNode LoRa® to the Chirpstack

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1579522633\/24812\/enenhki5eduvosgktdz8.png",
        "mode": "300",
        "width": 680,
        "height": 864,
        "caption": "**Figure 7:** Sending Data to ChirpStack"
    }
}]$

You can see the data which is just sent from RAK7204 LPWAN Environmental Sensor on ChirpStack page:

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1582559908\/24884\/haxxnxf1wv5jlzlytakp.png",
        "mode": "responsive",
        "width": 1934,
        "height": 1094,
        "caption": "**Figure 8:** Message Status in ChirpStack"
    }
}]$

