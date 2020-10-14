---
type: page
title: Accessing the Internet
listed: true
slug: accessing-the-internet
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

### Connect through Wi-Fi

If you want to connect through Wi-Fi, it can easily be done with the Wireless capabilities of the Raspberry Pi 4 by choosing "**5 Configure WIFI**". By default, the RAK7243 LPWAN Developer Gateway works in Wi-Fi AP Mode. In order for the gateway to connect to the router, it must work in Wi-Fi Client Mode.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1581343075\/23406\/fle7hxscizdrvsusaftu.png",
        "mode": "responsive",
        "width": 1297,
        "height": 649,
        "caption": "**Figure 2:** Configuration options for WIFI"
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

Once Wi-Fi AP Mode has been disabled by choosing "**2 Enable Client Mode/Disable AP Mode**" you can now then connect to a new Wi-Fi Network by choosing "**4 Add New SSID for Client**":

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1581343255\/23406\/fqzexcku1u6lil3qwnxw.png",
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
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1581343284\/23406\/e90mngpvgxopwnlfzevt.png",
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
        "text": "Please ensure to input the correct Wi-Fi SSID and Password or you will not be able to connect to the RAK7243 again via SSH in Wi-Fi AP Mode. If stuck in this situation, please follow this procedure listed in the [Accessing the Internet](\/quick-start\/rak7243-lorawan-developer-gateway\/accessing-the-internet#reverting-to-wi-fi-ap-mode) document which is applicable for all Raspberry Pi based gateways to work again in Wi-Fi AP mode.",
        "type": "warning",
        "title": "Warning:"
    }
}]$

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1581343308\/23406\/wrj0dc462lfiufnkja1s.png",
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
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1581343336\/23406\/wef2x5vtfnkpqihxnrys.png",
        "mode": "responsive",
        "width": 1164,
        "height": 537,
        "caption": "**Figure 6:** Password of the Wi-Fi"
    }
}]$

### Connect through Ethernet

If you want to connect to router through Ethernet Cable, do the following steps:

- In the main configuration menu, choose **“6 Configure LAN”**. This will let you set up a static IP address for the gateway’s Ethernet adapter.
- Just fill a static IP Address according to the IP address of the router you want to connect. Please note that the gateway and the router must be in the same network segment, otherwise the connection will fail.
- By default, the IP Address of the gateway's Ethernet is 192.168.10.10

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1581343376\/23406\/dh7krx7eaynhgjwryv5v.png",
        "mode": "responsive",
        "width": 1164,
        "height": 537,
        "caption": "**Figure 7:** Default gateway Ethernet IP Address"
    }
}]$

- Then configure the IP address of the Router. This is the LAN Interface IP address of the router.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1581343390\/23406\/ptp0upvteutju4bi1meq.png",
        "mode": "responsive",
        "width": 1164,
        "height": 537,
        "caption": "**Figure 8:** LAN Interface IP Address of the Router"
    }
}]$

- Press OK then the success message will appear.
- Lastly, reboot the gateway using the command "`sudo reboot`" in the command line and it will connect to the router successfully through Ethernet.

## Optional Configurations

These configurations under this section are only optional and situational.

### Reverting to Wi-Fi AP Mode

In the event that you have entered either or both incorrect Wi-Fi SSID and Password in the Wi-Fi Client Mode setup for the RAK7243 LPWAN Developer Gateway to connect to the router, follow these set of steps for you to work again in Wi-Fi AP Mode and redo the setup.

- Remove the SD Card from your RAK7243 LPWAN Developer Gateway and insert it into your PC. Your PC should be able to detect it same with the image below:

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1582254949\/23406\/u14zerb2flis1s3e96vr.png",
        "mode": "responsive",
        "width": 496,
        "height": 386,
        "caption": "**Figure 9**: Creating rak_ap file to your SD Card"
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

- Check if the rak_ap file is created succesffuly. If so, re-insert the SD Card into your RAK7243 LPWAN Developer Gateway and it should work again in Wi-Fi AP Mode.

