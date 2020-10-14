---
type: page
title: Configuring the Gateway
listed: true
slug: configuring-the-gateway
---published

Assuming you have logged into your LoRa Gateway using SSH successfully. Enter the following command in the command line:

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

You will now then see a page like the picture below:

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1560735002\/-1\/vtoil9zv7lvp1aq3s00x.png",
        "mode": "responsive",
        "width": 950,
        "height": 474,
        "caption": "**Figure 1:** Configuration Options for the Gateway"
    }
}]$

1. **Set pi password** - used to set/change the password of the LoRa Gateway.
2. **Set up RAK Gateway LoRa concentrator** - used to configure the frequency, which the LoRa Gateway will operate on, and the LoRa Server which the LoRa Gateway will work with.
3. **Edit packet-forwarder config** - used to open the global_conf.json file, in order to edit LoRaWAN parameters manually.
4. **Restart packet -forwarder** - used to restart the LoRa packet forwarded process.
5. **Configure WIFI** - used to configure the Wi-Fi settings in order to connect to a network.
6. **Configure LAN** - used to configure the Ethernet adapter settings.
7. **Configure APN name** - used to configure the APN name of pppd.
8. **Configure LTE Module** (Online for the Cellular Version) - used to configure automatic LTE network connection on startup.

$plugin[{
    "type": "callout",
    "data": {
        "text": "A unique ID will be generated for the LoRa Gateway. This is also called Gateway EUI and is essential for registering the gateway with any LoRa Network Server (TTN, LoRaServer).",
        "type": "info",
        "title": "Gateway ID"
    }
}]$

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1560735472\/13874\/pasahzg2uehgcwvuoug8.png",
        "mode": "responsive",
        "width": 950,
        "height": 474,
        "caption": "**Figure 2:** Gateway ID in the Configuration Window"
    }
}]$

There is also another way to get your "Gateway ID", just enter the command below in the command line:

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1560831107\/13874\/cbeiwceyy9oylikm2zqv.png",
        "mode": "responsive",
        "width": 515,
        "height": 88,
        "caption": "**Figure 3**: Gateway ID using the command line"
    }
}]$

### Set a new password for the LoRa Gateway

It is a good security practice to change the default password "raspberry" which is the same on all Raspberry Pi devices.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1560735604\/13874\/tkgwbj8twyf6ygsud75j.png",
        "mode": "responsive",
        "width": 934,
        "height": 461,
        "caption": "**Figure 4:** Changing the default password"
    }
}]$

You will be asked to enter your new password twice then press Enter.

### Set up RAK Gateway LoRa concentrator

This menu allows you to select your LoRa frequency band and one of the two available Networks Server options:

- **TTN (The Things Network)**. If you choose TTN as the LoRa Server, you will see the following page:

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1560768085\/13874\/trlhpcbwoxabgklbmh1c.png",
        "mode": "responsive",
        "width": 949,
        "height": 474,
        "caption": "**Figure 5:** Server Plan Configuration"
    }
}]$

Visit this [**article**](https://www.thethingsnetwork.org/docs/lorawan/frequencies-by-country.html) for information on your local TTN frequency plan. This will allow you to choose the correct plan, which is selected in the following window:

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1561414416\/13874\/zm6chseryxbgk8xxrakr.jpg",
        "mode": "responsive",
        "width": 1121,
        "height": 579,
        "caption": "**Figure 6:** Selecting the TTN Channel Plan"
    }
}]$

- **LoRaServer.** If you choose LoRaServer as your LoRa Server, you will see the following page:

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1560736586\/13874\/fvqytmylr8rmbz2fugsr.png",
        "mode": "responsive",
        "width": 934,
        "height": 461,
        "caption": "**Figure 7:** Selecting the Channel Plan for LoRaServer"
    }
}]$

Just like with TTN, choose the appropriate frequency for your country. Next, you need to set the IP Address of the LoRaServer, which you want your LoRa Gateway to work with.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1560831172\/13874\/ycavbx7p5xzwhdmpzyak.png",
        "mode": "responsive",
        "width": 934,
        "height": 461,
        "caption": "**Figure 8:** Default LoRaServer IP Address"
    }
}]$

The default IP Address is "127.0.0.1". If you want to use an external LoRaServer, you need to set it to its IP Address.

## Connect the LoRa Gateway to a Router

There are 3 ways on how you can connect your RAK7243C Pilot Gateway to the Internet.

1. **Connect through Wi-Fi**
2. **Connect through Ethernet**
3. **Connect through LTE (only for the Cellular Version)**

### Connect through Wi-Fi

If you want to connect through Wi-Fi, it can easily be done with the Wireless capabilities of the Raspberry Pi.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1560779801\/13874\/imjn5t5p0xy6e03y5gmw.png",
        "mode": "responsive",
        "width": 949,
        "height": 467,
        "caption": "**Figure 9:** Configuration options for WIFI"
    }
}]$

There are 4 options to choose from in the Wi-Fi configuration menu:

1. **Enable AP Mode/Disable Client Mode** - the LoRa Gateway will work in Wi-Fi Access Point Mode after rebooting while the Wi-Fi Client Mode will be disabled (this is the default mode).
2. **Enable Client Mode/Disable AP Mode** - the LoRa Gateway will work in Wi-Fi Client mode after rebooting, while Wi-Fi AP Mode will be disabled.
3. **Modify SSID and pwd for AP Mode** - used to modify the SSID and password of the Wi-Fi AP. Only works if the Wi-Fi AP Mode is enabled.
4. **Add New SSID for Client** - this is used if you want to connect to a new Wi-Fi Network. Only works in Wi-Fi Client mode.

### Connect through Ethernet

If you want to connect to a router through an Ethernet Cable, do the following:

- Just fill a static IP Address according to the IP address of the router you want to connect. Please note that the LoRa Gateway and the router must be in the same network segment, otherwise the connection will fail.
- By default, the IP Address of the LoRa Gateway's Ethernet is 192.168.10.10

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1560831409\/13874\/nvv8xtju1tzbmeh6u0fx.png",
        "mode": "responsive",
        "width": 950,
        "height": 474,
        "caption": "**Figure 10:** Default LoRa Gateway Ethernet IP Address"
    }
}]$

- Then configure the IP address of the Router. This is the LAN Interface IP address of the router:

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1560831441\/13874\/tvt6ir6jye3dxtm5cvwx.png",
        "mode": "responsive",
        "width": 950,
        "height": 474,
        "caption": "**Figure 11:** LAN Interface IP Address of the Router"
    }
}]$

- Press OK then reboot the LoRa Gateway using the command "`sudo reboot now`" in the command line and it will connect to the router successfully through Ethernet.

### Connect through LTE (Only for the Cellular Version)

If you want to deploy your LoRa Gateway to a place where there is no option of connecting to the internet through Wi-Fi or Ethernet, you can still do this through LTE. 

- First, make sure you have already inserted a suitable SIM Card into the RAK7243C Pilot Gateway. If not, turn off the gateway using the command "`sudo shutdown now`" and insert the card. 
- Login to your gateway using SSH and enter the command "`gateway-config`" and choose Item 8. Configure LTE Module.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1560832837\/13874\/nosizcqpao91okofggv9.png",
        "mode": "responsive",
        "width": 950,
        "height": 474,
        "caption": "**Figure 12:** Configure LTE Module Option"
    }
}]$

You will see 2 items:

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1560832877\/13874\/umyjmcaejiqjiej3ymoy.png",
        "mode": "responsive",
        "width": 950,
        "height": 474,
        "caption": "**Figure 13:** Enable LTE Automatic Dial-up"
    }
}]$

There are 2 configuration Options for the LTE Module:

1. **Enable LTE Automatic Dial-up** - the LoRa Gateway will connect to LTE Automatically, when it boots.
2. **Disable LTE Automatic Dial-up** - the LoRa Gateway will not connect to LTE Automatically.

$plugin[{
    "type": "callout",
    "data": {
        "text": "By default, the LoRa Gateway will connect to LTE Automatically, when it boots. If you want to disable it, choose \"Disable LTE Automatic Dial-up\"",
        "type": "info",
        "title": "Note"
    }
}]$

- Now let's configure the LTE Network operator's information. You should make sure that the state of the LTE Connecting Automatically is disabled as of now!
- Open the built in serial port tool, by execute the following command:

$plugin[{
    "type": "code-block",
    "data": {
        "languageBlocks": [
            {
                "code": "$ sudo minicom -D \/dev\/ttyAMA0 -b 115200",
                "language": "none"
            }
        ]
    }
}]$

- It will then enter minicom:

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1560833154\/13874\/qf18z1zgvvoacjd7a3hp.png",
        "mode": "600",
        "width": 743,
        "height": 289,
        "caption": "**Figure 14:** Minicom in the Serial Port Tool"
    }
}]$

- Try to enter the command "at" , if it returns OK, it means that you have opened the Serial Port Successfully!

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1560833239\/13874\/dioy303nvbjlyfdeb5me.png",
        "mode": "600",
        "width": 720,
        "height": 374,
        "caption": "**Figure 15:** AT Command in Minicom"
    }
}]$

$plugin[{
    "type": "callout",
    "data": {
        "text": "If you can't see \"at\" in the terminal, try to press \"Ctrl + A\" , then press \"Z\", then lastly press \"E\".",
        "type": "warning",
        "title": "Note"
    }
}]$

- Now, execute the AT Command "`at+cops=?`" to query all LTE Networks around you. It may take several seconds. When it is done, you can see some information like this: 

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1560833808\/13874\/buugxhru20wkf7j1w66u.png",
        "mode": "responsive",
        "width": 729,
        "height": 212,
        "caption": "**Figure 16:** Querying LTE Networks"
    }
}]$

- The picture above is just a demo, when we use it in China. You can see there are 3 LTE Network Operators, including China Mobile, China Unicom and China Telecom.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1560833564\/13874\/gsx7d4uu2kywn0nw0dz1.png",
        "mode": "responsive",
        "width": 725,
        "height": 222,
        "caption": "**Figure 17:** Querying LTE Network Sample Test"
    }
}]$

- Execute the AT Command "at+cops=1,0,XXX,YYY" to set the information of the LTE Network operator which you want to use. "XXX" is the operator identification name (ex: CHINA MOBILE, CHN-UNICOM, CHN-CT). "YYY" is the last number of the information for each operator - 0 for CHINA MOBILE.
- If it returns "OK", it means you have set it successfully!

## Configure APN Name

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1560834301\/13874\/x2pabz5t6ree7tqhiw4o.png",
        "mode": "responsive",
        "width": 722,
        "height": 364,
        "caption": "**Figure 18:** APN Name"
    }
}]$

You should set the APN name for the pppd process too. The default APN Name is "HOLOGRAM". If you want to modify it, please note that the value must be a true and valid APN Name,then set the appropriate baud rate, the default value is 115200.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1560834649\/13874\/idco4u9mrep7kn4qhwyg.png",
        "mode": "responsive",
        "width": 722,
        "height": 364,
        "caption": "**Figure 19:** Default Baud Speed - 115200"
    }
}]$

- To test the LTE Function, execute the following command :

$plugin[{
    "type": "code-block",
    "data": {
        "languageBlocks": [
            {
                "code": "$ sudo pppd call gprs",
                "language": "none"
            }
        ]
    }
}]$

- A log will be displayed. At the end of it, you can see the local and remote IP address and the primary and secondary DNS:

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1560835253\/13874\/rrjfulheqoghaxyjk4nk.png",
        "mode": "responsive",
        "width": 503,
        "height": 121,
        "caption": "**Figure 20:** Primary and Secondary DNS Address"
    }
}]$

- If you see valid addresses as in the image above, it means that the LoRa Gateway has connected to the LTE Network successfully! 
- The last thing you should not forget to do, is to enable the LTE Connecting automatically when it starts.

