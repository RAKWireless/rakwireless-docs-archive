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
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1581340591\/13822\/mxuydlvrphzfjpcpxvaw.png",
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
        "text": "A unique ID will be generated in for gateway. This is also called Gateway EUI squared in red in the figure above and is essential for registering the gateway with any LoRa\u00ae Network Server (TTN, ChirpStack)",
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
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1581340613\/13822\/u7mh6kga7akhvpjey29m.png",
        "mode": "responsive",
        "width": 676,
        "height": 173,
        "caption": "**Figure 2**: Gateway ID using the command line"
    }
}]$

## Setting a new password for the Gateway

It is a good security practice to change the default password "**raspberry**" which is the same on all Raspberry Pi devices.

- First, choose "1 Set pi password" option referred on the image below.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1581340623\/13822\/uodfwynklz8khnj7cv7w.png",
        "mode": "responsive",
        "width": 1351,
        "height": 670,
        "caption": "**Figure 3:** Set Pi Password"
    }
}]$

- Next, press "Yes" and you will be asked to enter your new password twice then press "Enter".

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1581340634\/13822\/imslbab8y9evizo5l12p.png",
        "mode": "responsive",
        "width": 1185,
        "height": 429,
        "caption": "**Figure 4:** Confirm Password Change"
    }
}]$

- Alright, the success message for changing password will then pop up.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1581340646\/13822\/a8whl0lnrmba6m3css3r.png",
        "mode": "responsive",
        "width": 1185,
        "height": 429,
        "caption": "**Figure 5:** Successful Password Change"
    }
}]$

## Set up RAK Gateway LoRa® Concentrator

This menu allows you to select your LoRa® frequency band and one of the two available Networks Server options by choosing "**2 Setup RAK Gateway LoRa® concentrator**"

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1581340654\/13822\/midmgg4tj6ob8y8jwn5b.jpg",
        "mode": "responsive",
        "width": 1337,
        "height": 656,
        "caption": "**Figure 6**:  Choosing Setup RAK Gateway LoRa\u00ae concentrator"
    }
}]$

You can choose one of two supported LoRa® Servers here: **TTN** or
**ChirpStack**.

### Server is TTN

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1581340661\/13822\/qagvx1pl6nkpfcgtcfrr.png",
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
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1581340671\/13822\/uzlzodqpqobehbaxzswh.jpg",
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
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1581340680\/13822\/ccqwdl61cdntcj3ig7km.png",
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
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1581340690\/13822\/rjsjjh32d15dttia0pzq.png",
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

First, select option 1 for configuring your Regional Frequency Band

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1581340737\/13822\/ndlwl5zmhun43tp11j2g.png",
        "mode": "responsive",
        "width": 1393,
        "height": 680,
        "caption": "**Figure 11:** Regional Frequency Band Option"
    }
}]$

Then, set the IP address of the ChirpStack which you want your gateway to work with:

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1581340751\/13822\/zlyc3tgjwoaazainc2ws.png",
        "mode": "responsive",
        "width": 1228,
        "height": 513,
        "caption": "**Figure 12:** Default LoRaServer IP Address"
    }
}]$

$plugin[{
    "type": "callout",
    "data": {
        "text": "The default IP Address is **`127.0.0.1`**which means you will be using the Built-in LoRa\u00ae Server. If you want to use an independent LoRa\u00ae Server\nrunning on another device or a cloud based LoRa\u00ae Server, you need to\nset it to the corresponding IP address",
        "type": "info",
        "title": "Note:"
    }
}]$

- If you have instead selected "**Chirpstack ADR Configure**" you can enable/disable the Adaptive Data Rate (ADR) functionality:

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1581340776\/13822\/llfkz2nzhdxrobku1tbc.png",
        "mode": "responsive",
        "width": 1331,
        "height": 675,
        "caption": "**Figure 13:** Chirpstack ADR Enable\/Disable"
    }
}]$

