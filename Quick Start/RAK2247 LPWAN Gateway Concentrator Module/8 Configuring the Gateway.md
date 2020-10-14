---
type: page
title: Configuring the Gateway
listed: false
slug: configuring-the-gateway
---published

Assuming you have successfully logged into your LoRa Gateway using SSH. Enter the following command in the command line:

$plugin[{
    "type": "code-block",
    "data": {
        "languageBlocks": [
            {
                "code": "$ sudo gateway-config",
                "language": "none"
            }
        ]
    }
}]$

You will now then see a page like the following picture below:

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1561006257\/14820\/gma22tuqzvzrp44m0hr4.png",
        "mode": "responsive",
        "width": 953,
        "height": 478,
        "caption": "**Figure 1:** Configuration Options for the Gateway"
    }
}]$

1. **Set pi password** - used to set/change the password of the LoRa Gateway.
2. **Set up RAK Gateway LoRa Concenterator** - used to configure the frequency, which the LoRa Gateway will operate on, and the LoRa Server which the LoRa Gateway will work with.
3. **Edit packet-forwarder config** - used to open the global_conf.json file, in order to edit LoRaWAN parameters manually.
4. **Restart packet -forwarder** - used to restart the LoRa packet forwarded process.
5. **Configure Wifi** - used to configure the Wi-Fi settings in order to connect to a network.
6. **Configure LAN** - used to configure the Ethernet adapter settings.

$plugin[{
    "type": "callout",
    "data": {
        "text": "A unique ID will be generated in for LoRa Gateway. This is also called Gateway EUI and is essential for registering the gateway with any LoRa Network Server (TTN, LoRaServer).",
        "type": "info",
        "title": "Gateway ID"
    }
}]$

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1561006365\/14820\/dd7yzksmd3nid7kgmyxt.png",
        "mode": "responsive",
        "width": 953,
        "height": 478,
        "caption": "**Figure 2:** Gateway ID in the Configuration Window"
    }
}]$

There is also another way to get your "Gateway ID", just enter the command below in the command line:

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1561006438\/14820\/otiz7f7wvnbuhljcoohf.png",
        "mode": "responsive",
        "width": 515,
        "height": 88,
        "caption": "**Figure 3**: Gateway ID using the command line"
    }
}]$

### Set a new password for the LoRa Gateway

It is a good security practice to change the default password "**raspberry**" which is the same on all Raspberry Pi devices.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1561006939\/14820\/yihlds2qtadxtzeccisg.png",
        "mode": "responsive",
        "width": 934,
        "height": 461,
        "caption": "**Figure 4:** Changing the default password"
    }
}]$

You will be asked to enter your new password twice then press "Enter".

### Set up RAK Gateway LoRa concentrator

This menu allows you to select your LoRa frequency band and one of the two available Networks Server options:

- **TTN (The Things Network)**. If you choose TTN as the LoRa Server, you will see the following page Visit this [article](https://www.thethingsnetwork.org/docs/lorawan/frequencies-by-country.html) for information on your local TTN frequency plan. This will allow you to choose the correct plan, which is selected in the following window:

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1561904511\/14820\/rmpansmtilkxreqbcueh.jpg",
        "mode": "responsive",
        "width": 1121,
        "height": 579,
        "caption": "**Figure 5:** Selecting the TTN Channel Plan"
    }
}]$

- **LoRaServer.** If you choose LoRaServer as your LoRa Server, you will see the following page:

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1561007247\/14820\/mx3qhqqcgczqpn0kko7h.png",
        "mode": "responsive",
        "width": 934,
        "height": 461,
        "caption": "**Figure 6:** Selecting the Channel Plan for LoRaServer"
    }
}]$

Just like with TTN, choose the appropriate frequency for your country. Next, you need to set the IP Address of the LoRaServer, which you want your LoRa Gateway to work with.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1561007426\/14820\/a6d6e9kc5d9qamekqc31.png",
        "mode": "responsive",
        "width": 949,
        "height": 474,
        "caption": "**Figure 7:** Default LoRaServer IP Address"
    }
}]$

The default IP Address is "127.0.0.1". If you want to use an external LoRaServer, you need to set it to its IP Address.

## Connect the LoRa Gateway to a Router

If you want to use TTN or an independent LoRaServer which may be deployed in Local area network or Internet, you need to connect your LoRa Gateway to a router first.

### Connect through Wi-Fi

If you want to connect through Wi-Fi, it can easily be done with the Wireless capabilities of the Raspberry Pi.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1561075017\/14820\/pmcso8wpscgk1zzzs8qs.png",
        "mode": "responsive",
        "width": 949,
        "height": 467,
        "caption": "**Figure 8:** Configuration options for WIFI"
    }
}]$

There are 4 options to choose from in the Wi-Fi configuration menu:

1. **Enable AP Mode/Disable Client Mode** - the LoRa Gateway will work in Wi-Fi Access Point Mode after rebooting while the Wi-Fi Client Mode will be disabled (this is the default mode).
2. **Enable Client Mode/Disable AP Mode** - the LoRa Gateway will work in Wi-Fi Client mode after rebooting, while Wi-FI AP Mode will be disabled.
3. **Modify SSID and pwd for AP Mode** - used to modify the SSID and password of the Wi-Fi AP. Only works if the Wi-Fi AP Mode is enabled.
4. **Add New SSID for Client** - this is used if you want to connect to a new Wi-Fi Network. Only works in Wi-Fi Client mode.

### Connect through Ethernet

If you want to connect to router through Ethernet Cable, do the following steps:

- Just fill a static IP Address according to the IP address of the router you want to connect. Please note that the LoRa gateway and the router must be in the same network segment, otherwise the connection will fail.
- By default, the IP Address of the LoRa Gateway's Ethernet is 192.168.10.10

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1561075065\/14820\/vwytijj41a0g4c8if72r.png",
        "mode": "responsive",
        "width": 950,
        "height": 474,
        "caption": "**Figure 9:** Default LoRa Gateway Ethernet IP Address"
    }
}]$

- Then configure the IP address of the Router. This is the LAN Interface IP address of the router:

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1561075083\/14820\/rix12hedommjzcs52sso.png",
        "mode": "responsive",
        "width": 950,
        "height": 474,
        "caption": "**Figure 10:** LAN Interface IP Address of the Router"
    }
}]$

- Press OK then reboot the LoRa Gateway using the command "`sudo reboot now`" in the command line and it will connect to the router successfully through Ethernet.

