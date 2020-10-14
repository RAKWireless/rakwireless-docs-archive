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

You will now then see a page like the following picture below:

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1581316724\/13874\/ivnbudjlcg1xm2noagvl.png",
        "mode": "responsive",
        "width": 1506,
        "height": 745,
        "caption": "**Figure 1:** Configuration Options for the Gateway"
    }
}]$

1. **Set pi password** - used to set/change the password of the gateway.
2. **Set up RAK Gateway LoRa Concentrator** - used to configure the frequency, which the gateway will operate on, and the LoRaWAN® Server which the gateway will work with.
3. **Restart packet -forwarder** - used to restart the LoRa® packet forwarded process.
4. **Edit packet-forwarder config-** used to open the global_conf.json file, in order to edit LoRaWAN®  parameters manually.
5. **Configure Wifi** - used to configure the Wi-Fi settings in order to connect to a network.
6. **Configure APN Name -** used to configure the APN name of pppd.
7. **Configure LTE Module -** (Online for the Cellular Version) - used to configure automatic LTE network connection on startup.
8. **Configure LAN** - used to configure the Ethernet adapter settings.

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
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1581318706\/13874\/ddvo78vfjxamrr5jnftl.png",
        "mode": "responsive",
        "width": 679,
        "height": 149,
        "caption": "**Figure 2**: Gateway ID using the command line"
    }
}]$

## Setting a new password for the Gateway

It is a good security practice to change the default password "**raspberry**" which is the same on all Raspberry Pi devices.

**1.**First, choose "**1 Set pi password**" option referred on the image below.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1581316739\/13874\/lb4lcpcxk9vuhg8xxwkv.png",
        "mode": "responsive",
        "width": 1506,
        "height": 745,
        "caption": "**Figure 3:** Set Pi Password"
    }
}]$

**2.**Next, press "**Yes**" and you will be asked to enter your new password twice then press "**Enter**".

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1581316747\/13874\/puwtmxjqflai90ejzwj4.png",
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
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1581316760\/13874\/vm2z749vmvlt92sksnek.png",
        "mode": "responsive",
        "width": 1185,
        "height": 429,
        "caption": "**Figure 5:** Successful Password Change"
    }
}]$

## Set up RAK Gateway LoRa® Concentrator

This menu allows you to select your LoRa® frequency band and one of the two available Networks Server options by choosing "**2 Setup RAK Gateway LoRa**®** concentrator**"

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1581316797\/13874\/ktnjwl2w33wsmzgth2oh.png",
        "mode": "responsive",
        "width": 1506,
        "height": 745,
        "caption": "**Figure 6**:  Choosing Setup RAK Gateway LoRa\u00ae concentrator"
    }
}]$

You can choose one of two supported LoRa® Servers here: **TTN** or
**ChirpStack**.

### Server is TTN

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1581317660\/13874\/ul588xl3su91f9xlqkd9.png",
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
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1581317672\/13874\/n2dwbzss4hzqxsevyeqg.jpg",
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
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1581317680\/13874\/oz0vetzytinpkrmnklmz.png",
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
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1581317689\/13874\/wxplmfajuroo8dcgaadk.png",
        "mode": "responsive",
        "width": 1248,
        "height": 629,
        "caption": "**Figure 10:** Server Is TTN"
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
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1581317699\/13874\/sdcqyojrwjtpfe3mtj46.png",
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
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1581317715\/13874\/cnm6bvyeuxzzj2uyoes0.png",
        "mode": "responsive",
        "width": 1228,
        "height": 513,
        "caption": "**Figure 12:** Default LoRaServer IP Address"
    }
}]$

$plugin[{
    "type": "callout",
    "data": {
        "text": "The default IP Address is **`127.0.0.1`**which means you will be using the Built-in LoRa\u00ae Server. If you want to use an independent LoRa Server\nrunning on another device or a cloud based LoRa Server, you need to\nset it to the corresponding IP address",
        "type": "info",
        "title": "Note:"
    }
}]$

- If you have instead selected "**Chirpstack ADR Configure**" you can enable/disable the Adaptive Data Rate (ADR) functionality:

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1581317722\/13874\/brnbjhabtzzav0bnf52r.png",
        "mode": "responsive",
        "width": 1331,
        "height": 675,
        "caption": "**Figure 13:** Chirpstack ADR Enable\/Disable"
    }
}]$

