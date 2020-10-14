---
type: page
title: Configuring the Gateway
listed: true
slug: configuring-the-gateway
---published

Assuming you have successfully logged into your Gateway using SSH, enter the following command in the command line:

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
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1581550153\/24746\/bejbisz0soqcvnwke8m7.png",
        "mode": "responsive",
        "width": 1373,
        "height": 684,
        "caption": "**Figure 1:** Configuration Options for the Gateway"
    }
}]$

1. **Set pi password** - used to set/change the password of the  Gateway.
2. **Set up RAK Gateway LoRa® Concentrator** - used to configure the frequency, which the Gateway will operate on, and the LoRaWAN® Server which the Gateway will work with.
3. **Restart packet -forwarder** - used to restart the LoRa® packet forwarded process.
4. **Edit packet-forwarder config-** used to open the global_conf.json file, in order to edit LoRaWAN®  parameters manually.
5. **Configure Wifi** - used to configure the Wi-Fi settings in order to connect to a network.

$plugin[{
    "type": "callout",
    "data": {
        "text": "A unique ID will be generated in for Gateway. This is also called Gateway EUI squared in red in the figure above and is essential for registering the gateway with any LoRa\u00ae Network Server (TTN, ChirpStack)",
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
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1581550162\/24746\/nzueuvsm64cgpuqd24ot.png",
        "mode": "responsive",
        "width": 654,
        "height": 165,
        "caption": "**Figure 2**: Gateway ID using the command line"
    }
}]$

## Setting a new password for the Gateway

It is a good security practice to change the default password "**raspberry**" which is the same on all Raspberry Pi devices.

**1.**First, choose "**1 Set pi password**" option referred on the image below.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1581550169\/24746\/hscjxkxelkabhenbqm13.png",
        "mode": "responsive",
        "width": 1373,
        "height": 684,
        "caption": "**Figure 3:** Set Pi Password"
    }
}]$

**2.**Next, press "**Yes**" and you will be asked to enter your new password twice then press "**Enter**".

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1581550176\/24746\/zvbdndopi97tzfuweeyw.png",
        "mode": "responsive",
        "width": 1185,
        "height": 429,
        "caption": "**Figure 4:** Confirm Password Change"
    }
}]$

**3.** Alright, the success message for changing password will then pops up.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1581550181\/24746\/pq9ur0z7mwvorqx5gj2c.png",
        "mode": "responsive",
        "width": 1185,
        "height": 429,
        "caption": "**Figure 5:** Successful Password Change"
    }
}]$

## Setup RAK Gateway LoRa® Concentrator

This menu allows you to select your LoRa® frequency band and one of the two available Networks Server options by choosing "**2 Setup RAK Gateway LoRa® concentrator**"

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1581550188\/24746\/ozxbwzvge7insar46dla.png",
        "mode": "responsive",
        "width": 1373,
        "height": 684,
        "caption": "**Figure 6**:  Choosing Setup RAK Gateway LoRa\u00ae concentrator"
    }
}]$

You can choose one of two supported LoRa® Servers here: **TTN** or
**ChirpStack**.

### Server is TTN

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1581550195\/24746\/kuxkzaxxrimequwn9vj8.png",
        "mode": "responsive",
        "width": 1373,
        "height": 684,
        "caption": "**Figure 7:** Server Is TTN"
    }
}]$

- **TTN (The Things Network)** - If you choose TTN as the LoRa® Server, you will see the following page. Visit this [article](https://www.thethingsnetwork.org/docs/lorawan/frequencies-by-country.html) for more information on your local TTN frequency plan. This will allow you to choose the correct plan.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1581550206\/24746\/ple7lkh8wmqd6kwsohdw.jpg",
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
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1581550214\/24746\/ztmwmjtduhrhbyhkznom.png",
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
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1581550238\/24746\/k5uwvfwwrsbiprxfn9u8.png",
        "mode": "responsive",
        "width": 1373,
        "height": 684,
        "caption": "**Figure 10:** Server Is Chirpstack"
    }
}]$

**ChirpStack** - If you choose Chirpstack as your LoRa® Server, choose "**2 Server is Other server**".

First, configure your Regional Frequency Band by choosing the option below:

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1581550260\/24746\/uuxsxxyoahdrvsc42nq4.png",
        "mode": "responsive",
        "width": 1316,
        "height": 508,
        "caption": "**Figure 11:** Regional Frequency Band Option"
    }
}]$

For this example, we will be using EU868 Frequency Plan.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1581550281\/24746\/rwic1kz9fqehyohleddj.png",
        "mode": "responsive",
        "width": 1444,
        "height": 678,
        "caption": "**Figure 12:** Selecting the Chirpstack Channel Plan"
    }
}]$

Then, set the IP address of the ChirpStack which you want your Gateway to work with:

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1581550288\/24746\/tflteiahky98hs5mqxd2.png",
        "mode": "responsive",
        "width": 1280,
        "height": 556,
        "caption": "**Figure 13:** Default LoRaServer IP Address"
    }
}]$

$plugin[{
    "type": "callout",
    "data": {
        "text": "Unlik the other RAK boards, the RAK7246G LPWAN Developer Gateway does not have a Built-in LoRa\u00ae Server. In this document, the IP Address of the Chirpstack is shown above. If you have another ChirpStack, you can fill its IP address here too.",
        "type": "info",
        "title": "Note:"
    }
}]$

You can then open your Chirpstack webpage by using the link below as an example. Make sure to have the [IP Address] changed same with what you have input in the previous step.

$plugin[{
    "type": "code-block",
    "data": {
        "languageBlocks": [
            {
                "code": "http:\/\/[IP Address]:8080\/#\/login",
                "language": "http"
            }
        ]
    }
}]$

