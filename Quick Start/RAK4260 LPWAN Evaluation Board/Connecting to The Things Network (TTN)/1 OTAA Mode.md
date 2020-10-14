---
type: page
title: OTAA Mode
listed: true
slug: ttn-otaa-mode
---published

- After connecting the device and choosing the appropriate COM Port and Baudrate, press the "Reset button" on your RAK5005 Baseboard Module and If everything works perfectly, you should see the following message below:

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1579606097\/20859\/kjqh0phcifksizzxca9x.jpg",
        "mode": "responsive",
        "width": 918,
        "height": 769,
        "caption": "**Figure 1:** Serial Port Tool Successful Connection"
    }
}]$

- As you see, RAK4260 has joined with TTN successfully. The default join mode is OTAA, and the default frequency is EU868. After resetting it, RAK4260 will join automatically because the dev_eui, app_eui, and app_key have been configured in the source code.

You can modify the dev_eui, app_eui, and the app_key as you want. You can find it in the following source [**code**](https://github.com/RAKWireless/RAK4260-LoRaNode-demo/blob/master/APPS_ENDDEVICE_DEMO1/src/config/conf_app.h)

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1579607065\/20859\/nvvijwxuwnotqt8esaeh.png",
        "mode": "responsive",
        "width": 1722,
        "height": 399,
        "caption": "**Figure 2:** Device EUI , Application EUI and Application Key"
    }
}]$

In order for you to send the data from the RAK4260 to the TTN successfully, choose the option 2 then press Enter. The following figure below shows the data received in the TTN.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1579606108\/20859\/oljn6zhxdq4lbp8bdlgk.jpg",
        "mode": "responsive",
        "width": 1118,
        "height": 513,
        "caption": "**Figure 3:** Data received in the TTN"
    }
}]$

