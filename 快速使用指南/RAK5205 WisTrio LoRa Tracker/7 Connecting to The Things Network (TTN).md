---
type: page
title: Connecting to The Things Network (TTN)
listed: true
slug: connecting-to-the-things-network--ttn-
---published

In this section, we will be connecting the RAK5205 WisTrio LoRa Tracker to The Things Network (TTN). If you don't have an account yet, head on to [https://www.thethingsnetwork.org/](https://www.thethingsnetwork.org/) and create one. Once done, Log in to your account and go to the console which can be found here:

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1562323818\/17319\/jb8ckibkbrpgioja03yr.jpg",
        "mode": "responsive",
        "width": 1345,
        "height": 638,
        "caption": "**Figure 1:** The Things Network Home Page"
    }
}]$

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1562333132\/17319\/myhvrix3afyi4x6dbx4d.jpg",
        "mode": "responsive",
        "width": 1794,
        "height": 819,
        "caption": "**Figure 2:** TTN Console Page"
    }
}]$

- Choose "**APPLICATIONS**"

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1562333159\/17319\/diwkgwy0plfrfwx3sh7v.jpg",
        "mode": "responsive",
        "width": 1822,
        "height": 446,
        "caption": "**Figure 3:** Application Page"
    }
}]$

## Adding an Application

- Click the "**add application**" button

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1562333256\/17319\/x1bbebrlhyxfu4bkxh9c.jpg",
        "mode": "responsive",
        "width": 1318,
        "height": 641,
        "caption": "**Figure 4:** Adding an Application"
    }
}]$

Here are the things that you should take note in adding an application:

1. **Application ID** - this will be the unique id of your application in the Network. Please note that characters should be in lower case, no spaces are allowed.
2. **Description** - this is a short and concise human readable description of your application.
3. **Application EUI** - this will be generated automatically by The Things Network for convenience.
4. **Handler Registration** - handler you want to register this application to.

- After you fill in the necessary information, press the "**Add application**" button at the bottom of this page. If you see the following page, this means that you have successfully registered your application.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1562333414\/17319\/ncxhd78r2e4nak71imni.jpg",
        "mode": "responsive",
        "width": 778,
        "height": 417,
        "caption": "**Figure 5:** Application Overview"
    }
}]$

### Register Device

- Scroll down until you see the Devices section, or you can also click the "**Devices**" button at the top:

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1562333481\/17319\/jroqdznnofe7oeax42xv.jpg",
        "mode": "responsive",
        "width": 1117,
        "height": 214,
        "caption": "**Figure 6:** Device Section"
    }
}]$

- Click "**Register device "**

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1562333618\/17319\/ggiwhpgus2n5fixoz22h.jpg",
        "mode": "responsive",
        "width": 1319,
        "height": 636,
        "caption": "**Figure 7:** Add your Device"
    }
}]$

Here are the things that you should take note in registering your device:

1. **Device ID** - this is the unique identifier for your RAK5205 WisTrio LoRa Tracker in your application. You need to enter this manually.
2. **Device EUI** - this is the unique identifier for your device in the network. You can change it later, if you want.

Click the following icon and the Device EUI will be automatically generated. The App Key should be in auto generation mode by default.

- Lastly, click the Register button. Now, your device is registered under the corresponding application.

