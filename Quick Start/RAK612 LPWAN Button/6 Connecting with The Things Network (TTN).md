---
type: page
title: Connecting with The Things Network (TTN)
listed: true
slug: connecting-with-the-things-network--ttn-
---published

In this section, we will be connecting the RAK612 LPWAN Button to The Things Network (TTN). If you don't have an account yet, head on to [https://www.thethingsnetwork.org/](https://www.thethingsnetwork.org/) and create one. Once done, log on to your account and go to the console which can be found here:

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1580634478\/16624\/hrw8vw0z6igvwncmaemo.jpg",
        "mode": "responsive",
        "width": 967,
        "height": 472,
        "caption": "**Figure 1:** The Things Network Home Page"
    }
}]$

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1580634538\/16624\/g5uw8isfrlu5txtbxcki.png",
        "mode": "responsive",
        "width": 1934,
        "height": 1092,
        "caption": "**Figure 2:** TTN Console Page"
    }
}]$

- Choose "**APPLICATIONS**"

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1578905118\/24038\/bfbdxer0da06nxv0bymr.png",
        "mode": "responsive",
        "width": 1380,
        "height": 649,
        "caption": "**Figure 3:** Application Page"
    }
}]$

## Adding An Application

- Click the "**add application**" button

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1580634571\/16624\/dpvmhjabxd3d0sni4dd8.png",
        "mode": "responsive",
        "width": 1934,
        "height": 1092,
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
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1580634588\/16624\/l2jw7vfxqx3gpx1oxzss.png",
        "mode": "responsive",
        "width": 1934,
        "height": 1094,
        "caption": "**Figure 5:** Application Overview"
    }
}]$

### Register Device

- Scroll down until you see the Devices section, or you can also click the "**Devices**" button at the top:

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1579406370\/24038\/ow74swwqofv1gxxj0qbk.png",
        "mode": "responsive",
        "width": 1741,
        "height": 375,
        "caption": "**Figure 6:** Device Section"
    }
}]$

- Click "**Register device "**

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1580634605\/16624\/blhql0ao0kz5xf6y9soj.png",
        "mode": "responsive",
        "width": 1934,
        "height": 1094,
        "caption": "**Figure 7:** Add your Device"
    }
}]$

Here are the things that you should take note in registering your device:

1. **Device ID** - this is the unique identifier for your RAK612 LPWAN Button in your application. You need to enter this manually.
2. **Device EUI** - this is the unique identifier for your device in the network. You can change it later, if you want.

Click the following icon and the Device EUI will be automatically generated. The App Key should be in auto generation mode by default.

- Lastly, click the Register button. Now, your device is registered under the corresponding application.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1580634624\/16624\/n0oi1ou4smdl4xfwahsg.png",
        "mode": "responsive",
        "width": 1934,
        "height": 1094,
        "caption": "**Figure 8:** Device Overview"
    }
}]$

Depending on which authentication method you want to use ,proceed to either the **OTAA mode** or **ABP mode** section.

