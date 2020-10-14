---
type: page
title: Set-up RAK7249-B with MQTT Bridge
listed: true
slug: set-up-rak7249-with-mqtt-bridge
---published

In this document, we will demonstrate on how to point the External RAK7249-B Macro Outdoor Gateway to the built-in LoRa® Server of RAK7249-A Macro Outdoor Gateway.

### Packet Forwarder Set-up

1.By navigating through LoRa® Gateway tab-> LoRa® Packet Forwarder-> General Setup, set the Protocol in the drop-down list to **LoRa Gateway MQTT Bridge**.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1584453672\/27006\/q0lrs5vddm9eah86v5hc.png",
        "mode": "responsive",
        "width": 1933,
        "height": 856,
        "caption": "**Figure 1**: Set LoRa\u00ae Gateway MQTT Bridge Protocol"
    }
}]$

### LoRa®  Gateway MQTT Bridge

1.Navigate through LoRa® Gateway tab -> LoRa Gateway MQTT Bridge -> General Setup and turn-on this feature using the Enable slider.

2.Update the credentials needed in the list provided below.

- **MQTT Broker Address**: IP address of RAK7249-A Gateway
- **MQTT Broker Port**: By default, its value is 1883. Please update this if it is not.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1584454258\/27006\/zei2sdxoopke3somxieo.png",
        "mode": "responsive",
        "width": 1282,
        "height": 654,
        "caption": "**Figure 2**: LoRa\u00ae Gateway MQTT Bridge Configuration"
    }
}]$

3.After clicking "**Save & Apply**", all LoRa® traffic should be redirected via the Bridge of Gateway-B to the MQTT Brocker of Gateway-A.

### Register RAK7249-B to RAK7249-A's Built-in LoRa® NS

This procedure is the same as when you registered RAK7249-A in its built-in LoRa® Network Server. Please refer to the [Set-up RAK7249-A with Built-in LoRa® Network  Server](/quick-start/rak7249-macro-outdoor-gateway/rak7249-build-in-lora-network-server-sc2#register-rak7249-gateway) and repeat the process. The image below is the representation of what your configuration should look like with the two Gateways are added.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1584455198\/27006\/bajuc5roazb5ajzylg2m.png",
        "mode": "responsive",
        "width": 1290,
        "height": 652,
        "caption": "**Figure 3**: LoRa\u00ae Network Server Gateway List"
    }
}]$

You can add more Gateways in the same manner as we did for the two. This is a convenient way to monitor if they are up using the "**Last Seen**" feed.

