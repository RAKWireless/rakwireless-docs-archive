---
type: page
title: Connecting to a Network
listed: true
slug: connecting-to-a-network
---published

If you want to use TTN or an independent ChirpStack, which may be deployed in a local area network or in a remote one, you need to connect your Gateway to a networking device that will allow you connectivity to the internet (a router for example).There are 2 options offered for this purpose.

### Connect through Wi-Fi

If you want to connect through Wi-Fi, it can easily be done with the Wireless capabilities of the Raspberry Pi 3B+ or Raspberry Pi 4 by choosing "**5 Configure WIFI**". By default, the RAK2287 Concentrator Module WisLink Series works in Wi-Fi AP Mode. In order for the gateway to connect to the router, it must work in Wi-Fi Client Mode.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1581341288\/13822\/hmd7dh5xqhsohdndsmfb.png",
        "mode": "responsive",
        "width": 1297,
        "height": 649,
        "caption": "**Figure 1:** Configuration options for WIFI"
    }
}]$

There are 5 options to choose from in the Wi-Fi configuration menu:

1. **Enable AP Mode/Disable Client Mode** - the gateway will work in Wi-Fi Access Point Mode after rebooting while the Wi-Fi Client Mode will be disabled (this is the default mode).
2. **Enable Client Mode/Disable AP Mode** - the gateway will work in Wi-Fi Client mode after rebooting, while Wi-FI AP Mode will be disabled.
3. **Modify SSID and pwd for AP Mode** - used to modify the SSID and password of the Wi-Fi AP. Only works if the Wi-Fi AP Mode is enabled.
4. **Add New SSID for Client** - this is used if you want to connect to a new Wi-Fi Network. Only works in Wi-Fi Client mode.
5. **Change Wi-Fi Country** - this is used to modify the Resident Country to match with Wi-Fi standards.

$plugin[{
    "type": "callout",
    "data": {
        "text": "In order to enable Wi-Fi Client Mode, you have to disable first the AP Mode.",
        "type": "warning",
        "title": "Warning"
    }
}]$

Once Wi-Fi AP Mode has been disabled by choosing "**2 Enable Client Mode/Disable AP Mode**", you can now then connect to a new Wi-Fi Network by choosing "**4 Add New SSID for Client**":

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1581341303\/13822\/g40iqrnisj1ksvjm9esn.png",
        "mode": "responsive",
        "width": 1297,
        "height": 649,
        "caption": "**Figure 2:** Add a new SSID"
    }
}]$

- Start by selecting your country of residence:

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1581341313\/13822\/wkvqbwaxeimcrwhsp4aw.png",
        "mode": "responsive",
        "width": 1312,
        "height": 707,
        "caption": "**Figure 3:** Selecting Country of Residence"
    }
}]$

- Enter the SSID of the network you want to connect:

$plugin[{
    "type": "callout",
    "data": {
        "text": "Please ensure to input the correct Wi-Fi SSID and Password or you will not be able to connect to the RAK2287 Concentrator Module WisLink Series again via SSH in Wi-Fi AP Mode. If stuck in this situation, please follow this procedure listed in [Connecting to a Network](\/quick-start\/rak2287-concentrator-module-wislink-series\/connecting-to-a-network#reverting-to-wi-fi-ap-mode) document which is applicable for all Raspberry Pi based gateways to work again in Wi-Fi AP mode.",
        "type": "warning",
        "title": "Warning:"
    }
}]$

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1581341322\/13822\/uzlp8e0qhnkv1ovfdatx.png",
        "mode": "responsive",
        "width": 1164,
        "height": 537,
        "caption": "**Figure 4:** SSID of the Network you want to connect to."
    }
}]$

- Enter also the password. Just leave it empty if None.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1581341332\/13822\/bqvoknbp5qcydoiaqpfy.png",
        "mode": "responsive",
        "width": 1164,
        "height": 537,
        "caption": "**Figure 5:** Password of the Wi-Fi"
    }
}]$

### Connect through Ethernet

If you want to connect to router through Ethernet Cable, do the following steps:

- In the main configuration menu, choose **“6 Configure LAN”**. This will let you set up a static IP address for the Gateway’s Ethernet adapter.
- Just fill a static IP Address according to the IP address of the router you want to connect. Please note that the LoRaWAN® gateway and the router must be in the same network segment, otherwise the connection will fail.
- By default, the IP Address of the gateway's Ethernet is `192.168.10.10`

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1581341343\/13822\/qfayodkpvgzivmiba7jq.png",
        "mode": "responsive",
        "width": 1164,
        "height": 537,
        "caption": "**Figure 6:** Default gateway Ethernet IP Address"
    }
}]$

- Then configure the IP address of the Router. This is the LAN Interface IP address of the router.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1581341352\/13822\/mlvdzjp1u7euvpivjqsr.png",
        "mode": "responsive",
        "width": 1164,
        "height": 537,
        "caption": "**Figure 7:** LAN Interface IP Address of the Router"
    }
}]$

- Press OK then the success message will appear.
- Lastly, reboot the gateway using the command "`sudo reboot`" in the command line and it will connect to the router successfully through Ethernet.

## Optional Configurations

These configurations under this section are only optional and situational.

### Reverting to Wi-Fi AP Mode

In the event that you have entered either or both incorrect Wi-Fi SSID and Password in the Wi-Fi Client Mode setup for the RAK2287 Concentrator Module WisLink Series to connect to the router, follow these set of steps for you to work again in Wi-Fi AP Mode and redo the setup.

- Remove the SD Card from your RAK2287 Concentrator Module WisLink Series and insert it into your PC. Your PC should be able to detect it same with the image below:

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1582262395\/13822\/g551j6ugudcuvml24o3w.png",
        "mode": "responsive",
        "width": 496,
        "height": 386,
        "caption": "**Figure 8**: Creating rak_ap file to your SD Card"
    }
}]$

- Using your "**Command Prompt**" or "**Terminal**", navigate to your SD Card and type this command to generate the "**rak_ap**" file.

$plugin[{
    "type": "code-block",
    "data": {
        "languageBlocks": [
            {
                "code": "cd > rak_ap",
                "language": "none"
            }
        ]
    }
}]$

- Check if the rak_ap file is created successfully. If so, re-insert the SD Card into your RAK2287 Concentrator Module WisLink Series and it should work again in Wi-Fi AP Mode.

