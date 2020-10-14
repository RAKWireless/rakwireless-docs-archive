---
type: page
title: Configuring the Gateway
listed: true
slug: configuring-the-gateway
---published

Assuming you have successfully logged into your gateway using SSH. Enter the following command in the command line:

$plugin[{
    "type": "code-block",
    "data": {
        "languageBlocks": [
            {
                "code": "sudo gateway-config",
                "language": "none"
            }
        ]
    }
}]$

You will now then see a page like the following picture below

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1581343713\/23406\/eers94tb9weex83knn3x.png",
        "mode": "responsive",
        "width": 1351,
        "height": 670,
        "caption": "**Figure 1:** Configuration Options for the Gateway"
    }
}]$

1. **Set pi password** - used to set/change the password of the gateway.
2. **Set up RAK Gateway LoRa® Concentrator** - used to configure the frequency, which the gateway will operate on, and the LoRaWAN® Server which the gateway will work with.
3. **Restart packet -forwarder** - used to restart the LoRa® packet forwarded process.
4. **Edit packet-forwarder config-** used to open the global_conf.json file, in order to edit LoRaWAN®  parameters manually.
5. **Configure Wifi** - used to configure the Wi-Fi settings in order to connect to a network.
6. **Configure LAN** - used to configure the Ethernet adapter settings.

$plugin[{
    "type": "callout",
    "data": {
        "text": "A unique ID will be generated in for gateway. This is also called Gateway EUI and is essential for registering the gateway with any LoRa\u00ae Network Server (TTN, ChirpStack).",
        "type": "info",
        "title": "Note:"
    }
}]$

There is also another way to get your "Gateway ID", just enter the command below in the command line:

$plugin[{
    "type": "code-block",
    "data": {
        "languageBlocks": [
            {
                "code": "sudo gateway-version",
                "language": "none"
            }
        ]
    }
}]$

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1581342499\/23406\/tnfwz5qjorlctgo015sz.png",
        "mode": "responsive",
        "width": 679,
        "height": 149,
        "caption": "**Figure 2**: Gateway ID using the command line"
    }
}]$

## Setting a new password for the Gateway

It is a good security practice to change the default password "**raspberry**" which is the same on all Raspberry Pi devices.

**1.** First, choose "**1 Set pi password**" option referred on the image below.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1581342522\/23406\/y5fdtevlquh4lmibo9d3.png",
        "mode": "responsive",
        "width": 1351,
        "height": 670,
        "caption": "**Figure 3:** Set Pi Password"
    }
}]$

**2.** Next, press "**Yes**" and you will be asked to enter your new password twice then press "**Enter**".

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1581342533\/23406\/noygoobysuhrm7bqtzir.png",
        "mode": "responsive",
        "width": 1185,
        "height": 429,
        "caption": "**Figure 4:** Confirm Password Change"
    }
}]$

**3.** Alright, the success message for changing password will then pop up.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1581342555\/23406\/qcdrxybjsvnlkotnfpso.png",
        "mode": "responsive",
        "width": 1185,
        "height": 429,
        "caption": "**Figure 5:** Successful Password Change"
    }
}]$

## Set up RAK Gateway LoRa® Concentrator

This menu allows you to select your LoRa® frequency band and one of the two available Networks Server options by choosing "**2 Setup RAK Gateway LoRa**® **concentrator** "

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1581342650\/23406\/ptueca5iwscm3fzjdh70.jpg",
        "mode": "responsive",
        "width": 1337,
        "height": 656,
        "caption": "**Figure 6**:  Choosing Setup RAK Gateway LoRa\u00ae contentrator"
    }
}]$

You can choose one of two supported LoRa® Servers here: **TTN** or **ChirpStack**.

### Server is TTN

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1581342825\/23406\/viuxteqcfp06iimvputo.png",
        "mode": "responsive",
        "width": 1248,
        "height": 629,
        "caption": "**Figure 7:** Server Is TTN"
    }
}]$

- **TTN (The Things Network)** - If you choose TTN as the LoRa® Server, you will see the following page. Visit this [article](https://www.thethingsnetwork.org/docs/lorawan/frequencies-by-country.html) for more information on your local TTN frequency plan. This will allow you to choose the correct plan.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1581342840\/23406\/qz7givfpa5zpyyznmoiz.jpg",
        "mode": "responsive",
        "width": 1234,
        "height": 615,
        "caption": "**Figure 8:** Selecting the TTN Channel Plan"
    }
}]$

After choosing the correct frequency, the success message will appear as shown below.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1581342947\/23406\/u155hjvyxxqac9ni7ohp.png",
        "mode": "responsive",
        "width": 1266,
        "height": 452,
        "caption": "**Figure 9**: Successfully Changed the Frequency"
    }
}]$

### Server is Chirpstack

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1581343004\/23406\/obhzc0h5bkdpi3utnoqm.png",
        "mode": "responsive",
        "width": 1248,
        "height": 629,
        "caption": "**Figure 10:** Server Is Chirpstack"
    }
}]$

**ChirpStack** - If you choose Chirpstack as your LoRa® Server, you will see the following page with two options available:

- **ChirpStack Channel Plan Configuration** - used to configure your Regional Frequency Band.
- **ChirpStack ADR Configure** -  used to enable/disable the Adaptive Data Rate (ADR)
functionality.

First, select option 1 for configuring your frequency channel. Then, set the IP address of the ChripStack.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1581343023\/23406\/ado4fzez5hy784eyehvo.png",
        "mode": "responsive",
        "width": 1242,
        "height": 546,
        "caption": "**Figure 11:** Regional Frequency Band Option"
    }
}]$

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1581343045\/23406\/vxuuvsvrigw2byklxcaa.png",
        "mode": "responsive",
        "width": 1228,
        "height": 513,
        "caption": "**Figure 12:** Default LoRaServer IP Address"
    }
}]$

$plugin[{
    "type": "callout",
    "data": {
        "text": "The default IP Address is \"**127.0.0.1**\". If you want to use an external LoRaServer, you need to set it to its IP Address.",
        "type": "info",
        "title": "Note:"
    }
}]$

- If you have instead selected "**Chirpstack ADR Configure**" you can enable/disable the Adaptive Data Rate (ADR) functionality:

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1581343062\/23406\/ivnxqv3s2m5fpcgfvbqo.png",
        "mode": "responsive",
        "width": 1331,
        "height": 675,
        "caption": "**Figure 13:** Chirpstack ADR Enable\/Disable"
    }
}]$

