---
type: page
title: Connecting to The Things Network (TTN)
listed: true
slug: connecting-to-the-things-network-ttn
---published

The Things Network is about enabling low power devices to be used in long range gateways that connect to an open-source, decentralized network and exchange data with Applications. Learn more about the Things Network [**here**](https://www.thethingsnetwork.org/docs/).

In this section, we will be connecting the RAK4200 LPWAN Breakout Module to The Things Network (TTN). If you don't have an account yet, head on to [https://www.thethingsnetwork.org/](https://www.thethingsnetwork.org/) and create one. Once done, Log in to your account and go to the console which can be found here:

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1588239767\/28885\/qjr7jfga4e1eiuujlszz.png",
        "mode": "responsive",
        "width": 1934,
        "height": 943,
        "caption": "**Figure 1:** The Things Network Home Page"
    }
}]$

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1588240002\/28885\/sfxlj5zsnbvdfdpqfm7y.png",
        "mode": "responsive",
        "width": 1933,
        "height": 1022,
        "caption": "**Figure 2:** TTN Console Page"
    }
}]$

- Choose "**APPLICATIONS**"

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1588240019\/28885\/caqnwisb7ik7eik165kn.png",
        "mode": "responsive",
        "width": 1113,
        "height": 337,
        "caption": "**Figure 3:** Application Page"
    }
}]$

## Adding An Application

- Click the "**add application**" button

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1588240711\/28885\/h1qx5vvmupqtsrglhnpq.png",
        "mode": "responsive",
        "width": 1116,
        "height": 752,
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
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1588241353\/28885\/uubjz0iqvglhnjokpvcr.png",
        "mode": "responsive",
        "width": 1112,
        "height": 602,
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
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1588241430\/28885\/culvejfbigeglp214ixh.png",
        "mode": "responsive",
        "width": 1113,
        "height": 745,
        "caption": "**Figure 7:** Add your Device"
    }
}]$

Here are the things that you should take note in registering your device:

1. **Device ID** - this is the unique identifier for your RAK4200 LPWAN Breakout Module in your application. You need to enter this manually.
2. **Device EUI** - this is the unique identifier for your device in the network. You can change it later, if you want.

Click the following icon and the Device EUI will be automatically generated. The App Key should be in auto generation mode by default.

- Lastly, click the Register button. Now, your device is registered under the corresponding application.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1588241894\/28885\/qqa7q4y4dq0u2q1ah6hj.png",
        "mode": "responsive",
        "width": 1116,
        "height": 1032,
        "caption": "**Figure 8:** Device Overview"
    }
}]$

