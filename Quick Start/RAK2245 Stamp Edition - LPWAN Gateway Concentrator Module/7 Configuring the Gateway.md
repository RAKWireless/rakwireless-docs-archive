---
type: page
title: Configuring the Gateway
listed: true
slug: configuring-the-gateway
---published

Assuming you have successfully logged into your gateway using SSH, enter the following command in the command line:

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
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1581341786\/15989\/tdvxaiqw3kzn13hawchq.png",
        "mode": "responsive",
        "width": 1351,
        "height": 670,
        "caption": "**Figure 1**: Configuration Options for the Gateway"
    }
}]$

1. **Set pi password** - used to set/change the password of the gateway.
2. **Set up RAK Gateway LoRa Concenterator** - used to configure the frequency, which the gateway will operate on, and the LoRa® Server which the gateway will work with.
3. **Edit packet-forwarder config-** used to open the global_conf.json file, in order to edit LoRaWAN® parameters manually.
4. **Restart packet -forwarder** - used to restart the LoRa® packet forwarded process.
5. **Configure Wifi** - used to configure the Wi-Fo settings in order to connect to a network.
6. **Configure LAN** - used to configure the Ethernet adapter settings.

$plugin[{
    "type": "callout",
    "data": {
        "text": "A unique ID will be generated in for gateway. This is also called Gateway EUI and is essential for registering the gateway with any LoRa\u00ae Network Server (TTN, Chirpstack).",
        "type": "info",
        "title": "Gateway ID"
    }
}]$

There is also another way to get your "Gateway ID", just enter the command below in the command line:

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1581341794\/15989\/f03ijojvwe5w3zt6tjec.png",
        "mode": "responsive",
        "width": 676,
        "height": 173,
        "caption": "**Figure 2**: Gateway ID using the command line"
    }
}]$

## Set a new password for the Gateway

It is a good security practice to change the default password "**raspberry**" which is the same on all Raspberry Pi devices.

**1.**First, choose "**1 Set pi password**" option referred on the image below.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1581341803\/15989\/qgyeekjep9ew26gae8er.png",
        "mode": "responsive",
        "width": 1351,
        "height": 670,
        "caption": "**Figure 3:** Set Pi Password"
    }
}]$

**2.**Next, press "**Yes**" and you will be asked to enter your new password twice then press "**Enter**".

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1581341814\/15989\/lkxgb6gnw0jfcyijsz4a.png",
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
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1581341826\/15989\/ey2uuvxzbotxesld4rbd.png",
        "mode": "responsive",
        "width": 1185,
        "height": 429,
        "caption": "**Figure 5:** Successful Password Change"
    }
}]$

## Set up RAK Gateway LoRa® concentrator

This menu allows you to select your LoRa® frequency band and one of the two available Networks Server options by choosing "**2 Setup RAK Gateway LoRa® concentrator**".

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1581341911\/15989\/hdt5witlefhgxso1nyce.jpg",
        "mode": "responsive",
        "width": 1337,
        "height": 656,
        "caption": "**Figure 6**: Choosing Setup RAK Gateway LoRa\u00ae concentrator"
    }
}]$

You can choose one of two supported LoRa® Servers here: **TTN** or **ChirpStack**.

### Server is TTN

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1581341919\/15989\/qsddpkzi6ymsqxha59c1.png",
        "mode": "responsive",
        "width": 1248,
        "height": 629,
        "caption": "**Figure 7:** Server Is TTN"
    }
}]$

- **TTN (The Things Network)** - If you choose TTN as the LoRa® Server, you will see the following page. Visit this [article](https://www.thethingsnetwork.org/docs/lorawan/frequencies-by-country.html) for more information on your local TTN frequency plan. This will allow you to choose the correct plan

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1581341927\/15989\/hv28mtqnkmvcvppwoqh8.jpg",
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
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1581341935\/15989\/sb4qkln2jjswm2geyiwp.png",
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
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1581341946\/15989\/orau1hsti7dngudqohup.png",
        "mode": "responsive",
        "width": 1248,
        "height": 629,
        "caption": "**Figure 10:** Server Is Chirpstack"
    }
}]$

**ChirpStack** - If you choose Chirpstack as your LoRa® Server, you will see the following page with two options available:

- **ChirpStack Channel Plan Configuration** - used to configure your Regional Frequency Band.
- **ChirpStack ADR Configure** - used to enable/disable the Adaptive Data Rate (ADR) functionality.

First, select option 1 for configuring your Regional Frequency Band

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1581341981\/15989\/okcf7wuywmusb0oos5mw.png",
        "mode": "responsive",
        "width": 1242,
        "height": 546,
        "caption": "**Figure 11:** Regional Frequency Band Option"
    }
}]$

Then, set the IP address of the ChirpStack which you want your gateway to work with:

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1581342000\/15989\/jiut8slqwomg2nel9lho.png",
        "mode": "responsive",
        "width": 1228,
        "height": 513,
        "caption": "**Figure 12:** Default ChirpStack IP Address"
    }
}]$

$plugin[{
    "type": "callout",
    "data": {
        "text": "The default IP Address is **`127.0.0.1`**which means you will be using the Built-in LoRa\u00ae Server. If you want to use an independent LoRa\u00ae Server running on another device or a cloud based LoRa\u00ae Server, you need to set it to the corresponding IP address",
        "type": "info",
        "title": "Note:"
    }
}]$

- If you have instead selected "**Chirpstack ADR Configure**" you can enable/disable the Adaptive Data Rate (ADR) functionality:

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1581342018\/15989\/sx6la0lcjcf7d4qf9wqe.png",
        "mode": "responsive",
        "width": 1331,
        "height": 675,
        "caption": "**Figure 13:** Chirpstack ADR Enable\/Disable"
    }
}]$

