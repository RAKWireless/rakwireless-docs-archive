---
type: page
title: Connecting to The Things Network
listed: true
slug: connecting-to-the-things-network
---published

In this section, we will be connecting the RAK7200 LoRa Tracker to The Things Network (TTN). If you don't have an account yet, head on to [https://www.thethingsnetwork.org/](https://www.thethingsnetwork.org/) and create one. Once done, Log in to your account and go to the console which can be found here:

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1563421695\/17848\/pb0mdchjud7eorohvuet.jpg",
        "mode": "responsive",
        "width": 1345,
        "height": 638,
        "caption": "**Figure 1:** The Things Network Home Page"
    }
}]$

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1563421728\/17848\/e4l5zixkbfhuqw7ysgdb.jpg",
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
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1564069648\/17848\/ftpljdg4theghxibsx7z.jpg",
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
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1564048164\/17848\/qvkk1mbcnwiag2uuqkeh.jpg",
        "mode": "responsive",
        "width": 1747,
        "height": 772,
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
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1564048179\/17848\/x0sdf39czf9gagznbzsf.jpg",
        "mode": "responsive",
        "width": 1745,
        "height": 766,
        "caption": "**Figure 5:** Application Overview"
    }
}]$

### Register Device

- Scroll down until you see the Devices section, or you can also click the "**Devices**" button at the top:

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1563422077\/17848\/mjpa9mvzixihvzbfdmb5.jpg",
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
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1563422471\/17848\/hzm9ove71lab95rxoi5d.jpg",
        "mode": "responsive",
        "width": 1750,
        "height": 753,
        "caption": "**Figure 7:** Add your Device"
    }
}]$

Here are the things that you should take note in registering your device:

1. **Device ID** - this is the unique identifier for your RAK7200 LoRa Tracker in your application. You need to enter this manually.
2. **Device EUI** - this is the unique identifier for your device in the network. You can change it later, if you want.

Click the following icon and the Device EUI will be automatically generated. The App Key should be in auto generation mode by default.

- Lastly, click the Register button. Now, your device is registered under the corresponding application.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1564048247\/17848\/tmgfmmzaaatiy6dwnagj.jpg",
        "mode": "responsive",
        "width": 1743,
        "height": 889,
        "caption": "**Figure 8:** Device Overview"
    }
}]$

