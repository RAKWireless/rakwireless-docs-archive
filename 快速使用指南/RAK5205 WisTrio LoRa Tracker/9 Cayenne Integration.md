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
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1562343431\/17321\/dadjtoxojhwqkidgxccy.jpg",
        "mode": "responsive",
        "width": 1197,
        "height": 361,
        "caption": "**Figure 1:** Device Payload Formats"
    }
}]$

- Next, go to the Integrations Tab and press the "add integration" button:

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1562343485\/17321\/rvvcogx99jxdcjxzs2t2.jpg",
        "mode": "responsive",
        "width": 1316,
        "height": 358,
        "caption": "**Figure 2:** Device Integration"
    }
}]$

- Select the MyDevices Icon :

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1562343543\/17321\/debqpxusqiid1hvbfuit.jpg",
        "mode": "responsive",
        "width": 1316,
        "height": 598,
        "caption": "**Figure 3:** My Devices Integration"
    }
}]$

- You will then be redirected to a page as seen below (Figure 4) where you need to enter a Process ID and select an Access Key (Choose the default key)

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1562343784\/17321\/kk0cwlgnxqkb3jc1gtin.jpg",
        "mode": "responsive",
        "width": 1317,
        "height": 607,
        "caption": "**Figure 4:** myDevices Integration Configuration"
    }
}]$

### Cayenne Configuration

If you don't have an account in Cayenne, head on to [https://mydevices.com/cayenne/signup/](https://mydevices.com/cayenne/signup/) and create an account for free.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1562344019\/17321\/ce9xntyrstdxjgs2dhj0.jpg",
        "mode": "responsive",
        "width": 1433,
        "height": 699,
        "caption": "**Figure 5:** Cayenne start screen"
    }
}]$

- Once logged in, navigate to the "Add New" drop down menu in the upper left corner and choose "Device/Widget".

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1562344090\/17321\/ywalgpwe69xxmtiupain.jpg",
        "mode": "responsive",
        "width": 908,
        "height": 233,
        "caption": "**Figure 6:** Adding a device"
    }
}]$

- Select **LoRa** in the list of Devices and Widgets and navigate to The Things Network at the end of the list.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1562344248\/17321\/t1gayyr7ulesgkv4atkh.jpg",
        "mode": "responsive",
        "width": 1299,
        "height": 738,
        "caption": "**Figure 7:** Choosing your device from the list"
    }
}]$

- A list of LoRa Products and Widgets are now displayed. Scroll down and look for "**Cayenne LPP**".

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1562344446\/17321\/b8daawz4wdrv4twckkd4.jpg",
        "mode": "responsive",
        "width": 1303,
        "height": 689,
        "caption": "**Figure 8:** Cayenne LPP device selection"
    }
}]$

- Lastly, Input the Device EUI and Optionally set if your device is moving or stationary.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1562344923\/17321\/vxrsbnkq34rvsvksnwcx.jpg",
        "mode": "responsive",
        "width": 1320,
        "height": 550,
        "caption": "**Figure 9:** Setting device parameters"
    }
}]$

- If everything went well you should end up with a screen as the in Figure 10:

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1562888471\/17321\/ynlgfjr93k2rld1aot3r.jpg",
        "mode": "responsive",
        "width": 1896,
        "height": 856,
        "caption": "**Figure 10:** Dashboard live view of RAK5205"
    }
}]$

$plugin[{
    "type": "callout",
    "data": {
        "text": "There are two widgets that appear as general Analog ones. The first one on channel 8 is the Speed as measured by the GPS receiver. The second one on channel 9 is the AQI (Air Quality Index). The user needs to edit the names and choose an appropriate UI representation by hand. This is so, because as of this moment LPP doesn\u2019t support data of such type and they are transmitted as general analogue values. In Rev2 of the LPP standard it is expected this issues will be address.",
        "type": "info",
        "title": "Note"
    }
}]$

