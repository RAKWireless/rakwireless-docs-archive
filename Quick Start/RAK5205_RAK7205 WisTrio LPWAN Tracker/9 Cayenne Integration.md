---
type: page
title: Cayenne Integration
listed: true
slug: cayenne-integration
---published

MyDevice/Cayenne is a service that allows one to monitor node data in real time and can also send downlink control messages. Additionally it has a wide range of integrations for alerts, notifications, and alarms. Its visualization tools provide various ways of representing both real time and statistical data (graphs, dials, gauges, scales, charts, etc.).

### The Things Network Configuration

Before we can use Cayenne , we need to configure our Application in TTN to properly work with it.

- Log into your TTN Console and navigate to the desired application and Device (RAK5205 in this case).
- Go to the Payload Formats tab as seen in the Figure 1 and choose **"Cayenne LPP**"

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1580361907\/17321\/crg46b4kwqgjgutbshaa.jpg",
        "mode": "responsive",
        "width": 1211,
        "height": 375,
        "caption": "**Figure 1:** Device Payload Formats"
    }
}]$

- Next, go to the Integrations Tab and press the "add integration" button:

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1580361913\/17321\/qpggeszni6bbpsvngyjr.jpg",
        "mode": "responsive",
        "width": 1330,
        "height": 372,
        "caption": "**Figure 2:** Device Integration"
    }
}]$

- Select the MyDevices Icon :

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1580361923\/17321\/szfeauknzfqphzri2pwb.jpg",
        "mode": "responsive",
        "width": 1330,
        "height": 612,
        "caption": "**Figure 3:** My Devices Integration"
    }
}]$

- You will then be redirected to a page as seen below (Figure 4) where you need to enter a Process ID and select an Access Key (Choose the default key)

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1580362044\/17321\/y5ruf9bbupnyvggmjm1d.jpg",
        "mode": "responsive",
        "width": 1331,
        "height": 621,
        "caption": "**Figure 4:** myDevices Integration Configuration"
    }
}]$

### Cayenne Configuration

If you don't have an account in Cayenne, head on to [https://mydevices.com/cayenne/signup/](https://mydevices.com/cayenne/signup/) and create an account for free.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1580362063\/17321\/o4dkqcf3od2nzjxn5vws.jpg",
        "mode": "responsive",
        "width": 1447,
        "height": 713,
        "caption": "**Figure 5:** Cayenne start screen"
    }
}]$

- Once logged in, navigate to the "Add New" drop down menu in the upper left corner and choose "Device/Widget".

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1580362069\/17321\/jixjac2mbfkrsskosthu.jpg",
        "mode": "responsive",
        "width": 922,
        "height": 247,
        "caption": "**Figure 6:** Adding a device"
    }
}]$

- Select **LoRa** in the list of Devices and Widgets and navigate to The Things Network at the end of the list.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1580362085\/17321\/aqizwyy4tnhzu7qrrext.jpg",
        "mode": "responsive",
        "width": 1313,
        "height": 752,
        "caption": "**Figure 7:** Choosing your device from the list"
    }
}]$

- A list of LoRa® Products and Widgets are now displayed. Scroll down and look for "**Cayenne LPP**".

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1580362094\/17321\/hrzw47je3uxbv9a8fyhe.jpg",
        "mode": "responsive",
        "width": 1317,
        "height": 703,
        "caption": "**Figure 8:** Cayenne LPP device selection"
    }
}]$

- Lastly, Input the Device EUI and Optionally set if your device is moving or stationary.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1580362099\/17321\/tlrku9fdhfgzkypfgswe.jpg",
        "mode": "responsive",
        "width": 1334,
        "height": 564,
        "caption": "**Figure 9:** Setting device parameters"
    }
}]$

- If everything went well you should end up with a screen as the in Figure 10:

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1580362106\/17321\/x80ncxi5xnwkhjlqcqby.jpg",
        "mode": "responsive",
        "width": 1910,
        "height": 870,
        "caption": "**Figure 10:** Dashboard live view of RAK5205"
    }
}]$

$plugin[{
    "type": "callout",
    "data": {
        "text": "There are two widgets that appear as general Analog ones. The first one on channel 8 is the Speed as measured by the GPS receiver. The second one on channel 9 is the AQI (Air Quality Index). The user needs to edit the names and choose an appropriate UI representation by hand. This is so, because as of this moment LPP doesn\u2019t support data of such type and they are transmitted as general analog values. In Rev2 of the LPP standard it is expected these issues will be address.",
        "type": "info",
        "title": "Note"
    }
}]$

