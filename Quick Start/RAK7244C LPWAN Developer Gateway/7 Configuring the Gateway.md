---
type: page
title: Configuring the Gateway
listed: true
slug: configuring-the-gateway
---published

Assuming you have successfully logged into your Gateway using SSH. Enter the following command in the command line:

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
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1581347618\/23720\/qcn1lnkdzyojoqy8wz3m.png",
        "mode": "responsive",
        "width": 1506,
        "height": 745,
        "caption": "**Figure 1:** Configuration Options for the Gateway"
    }
}]$

1. **Set pi password** - used to set/change the password of the Gateway.
2. **Set up RAK Gateway LoRa® Concentrator** - used to configure the frequency, which the Gateway will operate on, and the LoRaWAN® Server which the Gateway will work with.
3. **Restart packet -forwarder** - used to restart the LoRa® packet forwarded process.
4. **Edit packet-forwarder config-** used to open the global_conf.json file, in order to edit LoRaWAN®  parameters manually.
5. **Configure Wifi** - used to configure the Wi-Fi settings in order to connect to a network.
6. **Configure APN Name -** used to configure the APN name of pppd.
7. **Configure LTE Module -** (Online for the Cellular Version) - used to configure automatic LTE network connection on startup.
8. **Configure LAN** - used to configure the Ethernet adapter settings.

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
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1581347724\/23720\/u8sxormeyp9cozs1hkyx.png",
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
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1581347769\/23720\/hpj9nf27qfh3uebkvo6i.png",
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
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1581351454\/23720\/rl0ecvyqmbghl274ripv.png",
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
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1581351463\/23720\/dozzxg0ye5j2611qnr2x.png",
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
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1581351487\/23720\/scq6o7syajqxw1nwgewz.png",
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
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1581351495\/23720\/usqdo7kdhd3jwotjypcz.png",
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
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1581351528\/23720\/slfeve56zzv1alrum9zd.jpg",
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
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1581351522\/23720\/d34annlyfogazuplxmpz.png",
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
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1581351626\/23720\/ffanxpymfagrwan7skxl.png",
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
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1581351637\/23720\/ovjxc2pew9tb3m6a11kk.png",
        "mode": "responsive",
        "width": 1242,
        "height": 546,
        "caption": "**Figure 11:** Regional Frequency Band Option"
    }
}]$

Then, set the IP address of the ChirpStack which you want your LoRaWAN® Gateway to work with:

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1581351648\/23720\/a5qxtsqr17bgeuu9bfls.png",
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
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1581352158\/23720\/haloipphjfxjokqdjpzw.png",
        "mode": "responsive",
        "width": 1331,
        "height": 675,
        "caption": "**Figure 13:** Chirpstack ADR Enable\/Disable"
    }
}]$

