---
type: page
title: Connecting to The Things Network (TTN)
listed: true
slug: connecting-to-the-things-network
---published

The Things Network is about enabling low power devices to be used in long range gateways that connect to an open-source, decentralized network and exchange data with Applications. Learn more about the Things Network [**here**](https://www.thethingsnetwork.org/docs/).
In this section, we’ll show you how to connect the RAK811 LPWAN Breakout Module with TTN.

**1.**First, **connect** the RAK811 LPWAN Breakout Module to your PC and open the **Serial Port Tool**.

**2.Select** the appropriate COM port and **open** it as in the image:

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1579446095\/17307\/lcvx0tpp0mvbqtfvveja.png",
        "mode": "responsive",
        "width": 1374,
        "height": 899,
        "caption": "**Figure 1:** RAK811 Serial Port Tool"
    }
}]$

$plugin[{
    "type": "callout",
    "data": {
        "text": "In this section, it is the assumption that you are within the coverage range of a TTN Gateway.",
        "type": "info",
        "title": "Info:"
    }
}]$

**3.** Now go to the [TTN Website](https://www.thethingsnetwork.org/) and Log in.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1579524316\/17307\/xcnu0ubgglpnncjaxcxx.jpg",
        "mode": "responsive",
        "width": 1145,
        "height": 530,
        "caption": "**Figure 2:** The Things Network Homepage"
    }
}]$

**4.** Choose "**Console**" located at the top right corner. Then, Click "**Application**".

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1579445887\/17307\/dewhjv5kvji5cnwlb8q4.png",
        "mode": "responsive",
        "width": 1910,
        "height": 866,
        "caption": "**Figure 3:** TTN Console page"
    }
}]$

**5.** Press the "**add application**" button.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1579445806\/17307\/q69iye4keg0wcwvllxq4.png",
        "mode": "responsive",
        "width": 1934,
        "height": 584,
        "caption": "**Figure 4:** TTN Applications Page"
    }
}]$

**6.** Create your own Application by filling in with correct contents.

$plugin[{
    "type": "callout",
    "data": {
        "text": "The Application ID is an unique combination of lower case, alphanumerical characters, nonconsecutive - and _.",
        "type": "info",
        "title": "Info"
    }
}]$

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1579447503\/17307\/kyllbiovwoj3dagerfw9.png",
        "mode": "responsive",
        "width": 1910,
        "height": 1158,
        "caption": "**Figure 5:** TTN Add Application Page"
    }
}]$

**7.** Then press the “**Add application**” button at the bottom of this page, and you can see the following page:

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1579447277\/17307\/ig62tkokbeyymlwpe1gr.png",
        "mode": "responsive",
        "width": 1910,
        "height": 876,
        "caption": "**Figure 6:** TTN Application Information Page"
    }
}]$

**8.** At the middle of this page, you can find the box named “**DEVICES**” and click “**register device**”.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1579447590\/17307\/jxfqlvwpvbe8irybx6sm.png",
        "mode": "responsive",
        "width": 1910,
        "height": 923,
        "caption": "**Figure 7:** Registering Device in TTN"
    }
}]$

**9.** Fill in the "**Device ID"** . Click the icon in the **“Device EUI**”, then a code is generated automatically.

You can get the **“Device EUI**” of your RAK811 with the following command, which will display all node parameters:

$plugin[{
    "type": "code-block",
    "data": {
        "languageBlocks": [
            {
                "code": "at+get_config=lora:status",
                "language": "none"
            }
        ]
    }
}]$

In case you have had TTN generate a new **“Device EUI**” you can use the command below to import it into the RAK811 configuration parameters (**XXXX is the Device_EUI you want to update**):

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
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1579447915\/17307\/izycmdjz16pclj4sbhtn.png",
        "mode": "responsive",
        "width": 1910,
        "height": 1168,
        "caption": "**Figure 8:** Filling in the Device Information"
    }
}]$

**10.** Then press the “**Register**” button at the bottom of this page to finish.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1579448021\/17307\/jbsjagixye7gonowplap.png",
        "mode": "responsive",
        "width": 1912,
        "height": 915,
        "caption": "**Figure 9:** Device Overview in TTN"
    }
}]$

Depending on which authentication method you want to use please proceed to either the **OTAA mode** or **ABP mode** section.

