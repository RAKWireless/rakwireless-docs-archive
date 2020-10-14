---
type: page
title: ABP Mode
listed: true
slug: chirpstack-abp-mode
---published

1.If you select “**Device Profile  ABP**” or “**DeviceProfile_ABP_CN470**”, it means you want to join ChirpStack in **ABP mode**.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1580629318\/24812\/d2yg1k2jisypbejszfzg.png",
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
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1580629691\/24812\/buahb0dbl6vhdjcmub5g.png",
        "mode": "responsive",
        "width": 1909,
        "height": 1094,
        "caption": "**Figure 2:** ABP Parameters"
    }
}]$

3.Next, let’s use these parameters to set RAK811 LPWAN Evaluation Board by using **AT command**. Let's join in **ABP** mode and set **EU868** frequency as an example.

4.If the join mode is not in ABP, just set the LoRa® join mode to **ABP** and LoRa® a class to **Class A** by typing the following commands in RAK Serial Port Tool

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1579522241\/24812\/dkulqzpldm5nlpsjhbyz.jpg",
        "mode": "responsive",
        "width": 1366,
        "height": 869,
        "caption": "**Figure 3:** Setting of LoRaWAN Mode and Class"
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

- Now, try sending data from our RAK811 LPWAN Evaluation Board to the Chirpstack

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

- You can see the data which is just sent from RAK811 LPWAN Evaluation Boardon ChirpStack page:

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1580629481\/24812\/tk1ypmzg0va9nwaprkqe.png",
        "mode": "responsive",
        "width": 1934,
        "height": 1094,
        "caption": "**Figure 8:** Message Status in ChirpStack"
    }
}]$

