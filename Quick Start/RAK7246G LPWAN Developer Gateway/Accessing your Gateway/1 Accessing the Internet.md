---
type: page
title: Accessing the Internet
listed: true
slug: accessing-the-internet
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

1. **Set pi password** - used to set/change the password of the Gateway.
2. **Set up RAK Gateway LoRa® Concentrator** - used to configure the frequency, which the Gateway will operate on, and the LoRaWAN® Server which the Gateway will work with.
3. **Restart packet -forwarder** - used to restart the LoRa® packet forwarded process.
4. **Edit packet-forwarder config-** used to open the global_conf.json file, in order to edit LoRaWAN®  parameters manually.
5. **Configure Wifi** - used to configure the Wi-Fi settings in order to connect to a network.

### Connect through Wi-Fi

If you want to connect through Wi-Fi, it can easily be done with the Wireless capabilities of the Raspberry Pi Zero W by choosing "**5 Configure WIFI**". By default, the RAK7246G LPWAN Developer Gateway works in Wi-Fi AP Mode. In order for the Gateway to connect to the router, it must work in Wi-Fi Client Mode.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1581550305\/24746\/qmqjjpdyietin4zntdi3.png",
        "mode": "responsive",
        "width": 1297,
        "height": 649,
        "caption": "**Figure 2:** Configuration options for WIFI"
    }
}]$

There are 5 options to choose from in the Wi-Fi configuration menu:

1. **Enable AP Mode/Disable Client Mode** - the Gateway will work in Wi-Fi Access Point Mode after rebooting while the Wi-Fi Client Mode will be disabled (this is the default mode).
2. **Enable Client Mode/Disable AP Mode** - the Gateway will work in Wi-Fi Client mode after rebooting, while Wi-FI AP Mode will be disabled.
3. **Modify SSID and pwd for AP Mode** - used to modify the SSID and password of the Wi-Fi AP. Only works if the Wi-Fi AP Mode is enabled.
4. **Add New SSID for Client** - this is used if you want to connect to a new Wi-Fi Network. Only works in Wi-Fi Client mode.
5. **Change Wi-Fi Country** - this is used to modify the Resident Country to match with Wi-Fi standards.

$plugin[{
    "type": "callout",
    "data": {
        "text": "In order to enable Wi-Fi Client Mode, you have to disable first the Wi-Fi AP Mode.",
        "type": "warning",
        "title": "Note:"
    }
}]$

Once Wi-Fi AP Mode has been disabled by choosing "**2 Enable Client Mode/Disable AP Mode**", you can now then connect to a new Wi-Fi Network by choosing "**4 Add New SSID for Client**":

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1581550315\/24746\/wb51hj0sorlmy33jvmkb.png",
        "mode": "responsive",
        "width": 1297,
        "height": 649,
        "caption": "**Figure 3:** Add a new SSID"
    }
}]$

- Start by selecting your country of residence:

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1581550322\/24746\/zecx2qr6beujecjixysf.png",
        "mode": "responsive",
        "width": 1312,
        "height": 707,
        "caption": "**Figure 4:** Selecting Country of Residence"
    }
}]$

- Enter the SSID of the network you want to connect:

$plugin[{
    "type": "callout",
    "data": {
        "text": "Please ensure to input the correct Wi-Fi SSID and Password or you will\nnot be able to connect to the RAK7246G again via SSH in Wi-Fi AP Mode. If stuck\nin this situation, please follow this procedure listed in the [Accessing the Internet](\/quick-start\/rak7246g-lorawan-developer-gateway\/accessing-the-internet#reverting-to-wi-fi-ap-mode) document which is applicable for all Raspberry Pi based gateways to work again in\nWi-Fi AP mode.",
        "type": "warning",
        "title": "Warning:"
    }
}]$

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1581550340\/24746\/rtn8e9rpxj9b6wg0e67g.png",
        "mode": "responsive",
        "width": 1164,
        "height": 537,
        "caption": "**Figure 5:** SSID of the Network you want to connect to."
    }
}]$

- Enter also the password. Just leave it empty if None.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1581550347\/24746\/tnxkktgzlst8oz1unltu.png",
        "mode": "responsive",
        "width": 1164,
        "height": 537,
        "caption": "**Figure 6:** Password of the Wi-Fi"
    }
}]$

- Lastly, reboot the Gateway using the command "`sudo reboot`" in the command line and it will connect to the router successfully.

## Optional Configurations

These configurations under this section are only optional and situational.

### Reverting to Wi-Fi AP Mode

In the event that you have entered either or both incorrect Wi-Fi SSID and Password in the Wi-Fi Client Mode setup for the RAK7246G LPWAN Developer Gateway to connect to the router, follow these set of steps for you to work again in Wi-Fi AP Mode and redo the setup.

- Remove the SD Card from your RAK7246G LPWAN Developer Gatewayand insert it into your PC. Your PC should be able to detect it same with the image below:

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1582243235\/24746\/ihabldjwc3wds0enjiil.png",
        "mode": "responsive",
        "width": 496,
        "height": 386,
        "caption": "**Figure 7**: Cx`"
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

- Check if the rak_ap file is created successfully. If so, re-insert the SD Card into your RAK7246G LPWAN Developer Gateway and it should work again in Wi-Fi AP Mode.

