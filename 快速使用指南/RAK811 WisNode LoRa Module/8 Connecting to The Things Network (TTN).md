---
type: page
title: Connecting to The Things Network (TTN)
listed: true
slug: connecting-to-the-things-network--ttn-
---published

The Things Network is about enabling low power devices to use long range [g](https://www.thethingsnetwork.org/docs/gateways/)ateways to connect to an open-source, decentralized network to exchange data with Applications. Learn more about the Things Network [**here**](https://www.thethingsnetwork.org/docs/).
In this section, we’ll show how to connect the RAK811 WisNode LoRa Module with TTN.

1.First, **connect** the RAK811 WisNode LoRa Module to your PC and open the **Serial Port Tool**.

2.**Select** the appropriate COM port and **open** it as in the image:

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1563155964\/17307\/ur5lfcuh8vkv8eniqdtl.jpg",
        "mode": "responsive",
        "width": 907,
        "height": 583,
        "caption": "**Figure 1.** RAK811 Serial Port Tool"
    }
}]$

$plugin[{
    "type": "callout",
    "data": {
        "text": "In this section, it is the assumption that you are within the coverage range of a TTN Gateway.",
        "type": "info",
        "title": "Info"
    }
}]$

3.Now go to the [TTN Website](https://www.thethingsnetwork.org/) and Log in.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1563156084\/17307\/kgjialvxamjwva0seidv.jpg",
        "mode": "responsive",
        "width": 1149,
        "height": 562,
        "caption": "**Figure 2.** The Things Network Homepage"
    }
}]$

4.Choose "**Console**" located at the top right corner. Then, Click "**Application**".

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1563156131\/17307\/xq8jwvlifkdwuv9firat.jpg",
        "mode": "responsive",
        "width": 1794,
        "height": 819,
        "caption": "**Figure 3.** TTN Console page"
    }
}]$

5.Press the "**add application**" button.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1563156165\/17307\/cwhz1zbh7czvotjoye7w.jpg",
        "mode": "responsive",
        "width": 1822,
        "height": 446,
        "caption": "**Figure 4.** TTN Applications Page"
    }
}]$

6.Create your own Application by filling in with correct contents.

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
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1563156346\/17307\/odk1y5lji1qwkatnyvor.jpg",
        "mode": "responsive",
        "width": 1779,
        "height": 935,
        "caption": "**Figure 5.** TTN Add Application Page"
    }
}]$

7.Then press the “**Add application**” button at the bottom of this page, and you can see the following page:

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1563156402\/17307\/mcofsd78tcmhsue1tmnb.jpg",
        "mode": "responsive",
        "width": 1783,
        "height": 919,
        "caption": "**Figure 6.** TTN Application Information Page"
    }
}]$

8.At the middle of this page, you can find the box named “**DEVICES**” and click “**register device**”.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1563156433\/17307\/tn8uspaynomhhj4mx2h1.jpg",
        "mode": "responsive",
        "width": 1361,
        "height": 262,
        "caption": "**Figure 7.** Registering Device in TTN"
    }
}]$

9.Fill in the "**Device ID"** . Click the icon in the **“Device EUI**”, then a code is generated automatically.

You can get the **“Device EUI**” of your RAK811 with the following command, which will display all node parameters:

$plugin[{
    "type": "code-block",
    "data": {
        "languageBlocks": [
            {
                "code": "at+get_config=lora:status",
                "language": "javascript"
            }
        ]
    }
}]$

In case you have had TTN generate a new **“Device EUI**” you can use the command below to import it into the RAK811 configuration parameters (**X is the Device_EUI you want to update**):

$plugin[{
    "type": "code-block",
    "data": {
        "languageBlocks": [
            {
                "code": "at+set_config=lora:dev eui:XXXX",
                "language": "javascript"
            }
        ]
    }
}]$

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1563156540\/17307\/rpb6p0uo5diqamwyslfp.jpg",
        "mode": "responsive",
        "width": 1789,
        "height": 885,
        "caption": "**Figure 8.** Filling in the Device Information"
    }
}]$

10.Then press the “**Register**” button at the bottom of this page to finish.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1563156583\/17307\/zvbax3y52nchf8iqpift.jpg",
        "mode": "responsive",
        "width": 1781,
        "height": 838,
        "caption": "**Figure 9**. Device Overview in TTN"
    }
}]$

Depending on which authentication method you want to use please proceed to either the **OTAA mode** or **ABP mode** section.

