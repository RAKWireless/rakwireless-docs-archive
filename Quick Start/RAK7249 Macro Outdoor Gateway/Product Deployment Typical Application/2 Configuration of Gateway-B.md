---
type: page
title: Configuration of Gateway-B
listed: true
slug: configuration-of-gateway-b
---published

Now we will point Gateway-B to the built-in LoRa® Server of Gateway-A.

## 1 . Packet-forwarder Setup

- Go to the **LoRaWAN™ Gateway tab >>LoRa® Packet Forwarder >> General Setup**. In the drop down menu for Protocol select  **LoRaWAN™ Gateway MQTT Bridge**.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1580554497\/23154\/rpsm8o5puvxhgaaoiruh.jpg",
        "mode": "responsive",
        "width": 810,
        "height": 419,
        "caption": "**Figure 1**: Gateway Protocol Mode (LoRaWAN\u2122 Gateway MQTT Bridge)"
    }
}]$

## 2 . LoRa®  Gateway MQTT Bridge

Go to the **LoRaWAN™ Gateway tab >> LoRaWAN™ Gateway MQTT Bridge >> General Setup**.

- Enable the MQTT Bridge it via the slider and enter the IP address of Gateway-A.
- Set **Port : 1883** as default, if it isn’t please update the data. Leave the rest of the settings with their default values.
- After Saving & Applying, all LoRa® traffic should be redirected via the Bridge of Gateway- B to the MQTT Brocker of Gateway-A.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1580554505\/23154\/b7kyhrqze7bnt3zfkkvz.jpg",
        "mode": "responsive",
        "width": 807,
        "height": 422,
        "caption": "**Figure 2**: LoRaWAN\u2122 Gateway MQTT Bridge Configuration"
    }
}]$

- You can add more Gateway in the same manner as we did for the two we are using. This is a convenient way to monitor if they are up (Last Seen field).

