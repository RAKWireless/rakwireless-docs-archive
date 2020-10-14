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

You will now then see a page like the following picture below:

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1583820362\/26838\/pgz9vj3jtvdmollkanqc.png",
        "mode": "responsive",
        "width": 1506,
        "height": 745,
        "caption": "**Figure 1:** Configuration Options for the Gateway"
    }
}]$

1. **Set pi password** - used to set/change the password of the gateway.
2. **Set up RAK Gateway LoRa®** Concentrator** - used to configure the frequency, which the gateway will operate on, and the LoRaWAN® Server which the gateway will work with.
**
3. **Restart packet -forwarder** - used to restart the LoRa® packet forwarded process.
4. **Edit packet-forwarder config-** used to open the global_conf.json file, in order to edit LoRaWAN® parameters manually.
5. **Configure Wifi** - used to configure the Wi-Fi settings in order to connect to a network.
6. **Configure APN Name -** used to configure the APN name of pppd.
7. **Configure LTE Module -** (Online for the Cellular Version) - used to configure automatic LTE network connection on startup.
8. **Configure LAN** - used to configure the Ethernet adapter settings.

### Connect through Wi-Fi

If you want to connect through Wi-Fi, it can easily be done with the Wireless capabilities of the Raspberry Pi 3B+ by choosing "**5 Configure Wifi**". By default, the RAK7243C LPWAN Developer Gateway works in Wi-Fi AP Mode. In order for the Gateway to connect to the router, it must work in Wi-Fi Client Mode.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1583820427\/26838\/bzvol7clyvogrlfcf6mm.png",
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
        "title": "Warning:"
    }
}]$

Once Wi-Fi AP Mode has been disabled by choosing "**2 Enable Client Mode/Disable AP Mode**", you can now then connect to a new Wi-Fi Network by choosing "**4 Add New SSID for Client**":

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1583820648\/26838\/oedelnm55crlacr1qezp.png",
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
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1583820820\/26838\/tho0wgcekiybxiyw1lg1.png",
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
        "text": "Please ensure to input the correct Wi-Fi SSID and Password or you will not be able to connect to the RAK7243C again via SSH in Wi-Fi AP Mode. If stuck in this situation, please follow this procedure listed in the [Accessing the Internet](\/quick-start\/rak7243c-lorawan-developer-gateway\/accessing-the-internet#reverting-to-wi-fi-ap-mode) document which is applicable for all Raspberry Pi based gateways to work again in Wi-Fi AP mode.",
        "type": "warning",
        "title": "Warning:"
    }
}]$

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1583820872\/26838\/d2h64zg2aqhpwtzektci.png",
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
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1583820896\/26838\/toenoesnbmrz1eeza4yq.png",
        "mode": "responsive",
        "width": 1164,
        "height": 537,
        "caption": "**Figure 6:** Password of the Wi-Fi"
    }
}]$

### Connect through Ethernet

If you want to connect to router through Ethernet Cable, do the following steps:

- In the main configuration menu, choose **“6 Configure LAN”**. This will let you set up a static IP address for the Gateway’s Ethernet adapter.
- Just fill a static IP Address according to the IP address of the router you want to connect. Please note that the gateway and the router must be in the same network segment, otherwise the connection will fail.
- By default, the IP Address of the gateway's Ethernet is `192.168.10.10`

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1583820933\/26838\/q7cisano0ckdjzfmrjwn.png",
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
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1583820962\/26838\/rfflmexk4jeyay8yyfp9.png",
        "mode": "responsive",
        "width": 1164,
        "height": 537,
        "caption": "**Figure 8:** LAN Interface IP Address of the Router"
    }
}]$

- Press OK then the success message will appear.
- Lastly, reboot the gateway using the command "`sudo reboot`" in the command line and it will connect to the router successfully through Ethernet.

### Connecting through an LTE Network

The RAK7243C comes with the RAK2013 Cellular making it capable of connecting through LTE network. In this section, you will learn on how to connect your gateway to an LTE network.

**1.**First, insert a SIM card of the appropriate type and size into the SIM card slot. Power on the Gateway.

**2.** Then, log into the Gateway through SSH, and
enter the command:

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

**3.** Next, in the main configuration menu choose “**7 Configure LTE Module**”:

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1582609485\/24014\/s4wdcqiwukl5evm7fyhm.png",
        "mode": "responsive",
        "width": 1506,
        "height": 745,
        "caption": "**Figure 9:** Configure LTE Module"
    }
}]$

Two configuration options are available for your LTE.

1. **Enable LTE Automatic Dial-up** - the default option and is used to enable automatic connection during start-up.
2. **Disable LTE Automatic Dial-up** - used to disable automatic connection during start-up.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1582609491\/24014\/qzy2znqy3rn32asplaki.png",
        "mode": "responsive",
        "width": 1232,
        "height": 528,
        "caption": "**Figure 10**: LTE Configuration Options"
    }
}]$

After that, you need to configure the LTE network operator’s information. Make sure to disable the automatic connection on start-up feature before starting.

**4.** Execute the command below in the console to start minicom tool:

$plugin[{
    "type": "code-block",
    "data": {
        "languageBlocks": [
            {
                "code": "sudo minicom -D \/dev\/ttyAMA0 -b 115200",
                "language": "none"
            }
        ]
    }
}]$

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1577037695\/23815\/hsnj9bmmt4hm7jjivlfn.png",
        "mode": "responsive",
        "width": 633,
        "height": 203,
        "caption": "**Figure 11**: Minicom Tool"
    }
}]$

**5.** Then, try entering the command “**at**” in the tool, if it returns with “**OK**”, it means you have opened the serial port successfully:

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1577037131\/23815\/e2nnhzfcsvrzawsnjc3x.png",
        "mode": "responsive",
        "width": 642,
        "height": 247,
        "caption": "**Figure 12**: AT Command in Minicom"
    }
}]$

$plugin[{
    "type": "callout",
    "data": {
        "text": "If you cannot see the \u201cat\u201d, which you just entered,\ntry to hold \u201cCTRL+A\u201d, then press \u201cZ\u201d, then press \u201cE\u201d. This should allow you to\ngo to the command entering mode.",
        "type": "info",
        "title": "Note:"
    }
}]$

**6.** Next, execute the AT command “**`at+cops=?`**” to look for all available LTE networks in range:

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1577037567\/23815\/gnqzfqfiyr9midcxzykr.png",
        "mode": "responsive",
        "width": 631,
        "height": 280,
        "caption": "**Figure 13**: AT Command for LTE Network Query"
    }
}]$

This may take a couple of seconds. After that, you'll see the available LTE Network information similar to the image below.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1576218280\/-1\/a2dffmeci1qkvarbnh4h.jpg",
        "mode": "responsive",
        "width": 1192,
        "height": 341,
        "caption": "**Figure 14**: LTE Network Example"
    }
}]$

$plugin[{
    "type": "callout",
    "data": {
        "text": "The image above shows the available LTE network in China. These information may vary depending on the available network in your region. For instance in China, the available  network are \u201cCHINA MOBILE\u201d, \u201cCHN-UNICOM\u201d, or \u201cCHN-CT\u201d.",
        "type": "info",
        "title": "Note:"
    }
}]$

**7.**Next, execute the AT command below to set the information of the LTE network operator that you want to use.

- XXX - this parameter is set to describe the network operator. For example, "CHINA MOBILE”, “CHN-UNICOM”, or “CHN-CT”
- **YYY** - this parameter is set as the last value of every operator. Choose the network with 0 value as this is the currently used network.

Now let’s take this LTE network in Europe (Bulgaria) as an example:

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1576234424\/23815\/mtzbhqbruxtqqtg0993z.jpg",
        "mode": "responsive",
        "width": 918,
        "height": 49,
        "caption": "**Figure 15**: Sample LTE Networks in EU"
    }
}]$

Then, using the sample AT command described above, the command will be:

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1576218397\/-1\/dgcsdrvgw5yyjlxfhzdn.jpg",
        "mode": "responsive",
        "width": 918,
        "height": 99,
        "caption": "**Figure 16**: Sample AT Command for LTE Network"
    }
}]$

After then, you will receive "OK" which means you have successfully configured the LTE network.

$plugin[{
    "type": "callout",
    "data": {
        "text": "In order for you to exit Minicom. Press Enter, Ctrl + A then press Q. A pop up will appear and choose Yes.",
        "type": "info",
        "title": "How to Quit Minicom?"
    }
}]$

**8.**Proceed to setting the **APN name** for the **pppd**
process. From the main configuration menu choose “**6
Configure APN name**”.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1582609501\/24014\/mgnltetmph7fql2dyptt.png",
        "mode": "responsive",
        "width": 1420,
        "height": 707,
        "caption": "**Figure 17:** Configure APN Name"
    }
}]$

**9.** Then, you will see the window option below where you can change the APN Name or retain its default name.

$plugin[{
    "type": "callout",
    "data": {
        "text": "If you want to modify the APN Name, make it sure it is a real and valid APN Name.",
        "type": "info",
        "title": "Note:"
    }
}]$

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1582609507\/24014\/wxlr9qc1jvgrtdqokbj0.png",
        "mode": "responsive",
        "width": 1192,
        "height": 533,
        "caption": "**Figure 18**: APN Name"
    }
}]$

**10.** Lastly, set the baud rate. The default value is 115200.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1582609512\/24014\/sje1mevpfizxspzka0jf.png",
        "mode": "responsive",
        "width": 1192,
        "height": 533,
        "caption": "**Figure 19**: Baud Rate Setting"
    }
}]$

Great! You have finished configuring your LTE network. Now, let's test and verify the connection.

**1.** Execute the command. in the terminal.

$plugin[{
    "type": "code-block",
    "data": {
        "languageBlocks": [
            {
                "code": "sudo pppd call gprs",
                "language": "none"
            }
        ]
    }
}]$

There will be a series of log but after that, you will see the the following information at the end of the log.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1576218535\/-1\/i3bmpsoxp2urhnag3vyx.jpg",
        "mode": "responsive",
        "width": 451,
        "height": 100,
        "caption": "**Figure 20**: IP address Information"
    }
}]$

You will be assigned with an IP address (local and remote) along with the DNS addresses. Having these information signifies that your connection has successfully established.

Also, do not forget to re-enable the automatic LTE connection on start up

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1582609516\/24014\/q4viffhbutonrx71vwjs.png",
        "mode": "responsive",
        "width": 1232,
        "height": 528,
        "caption": "**Figure 21**: Enabling the Automatic LTE Connection during Start-Up"
    }
}]$

## Optional Configurations

These configurations under this section are only optional and situational.

### Reverting to Wi-Fi AP Mode

In the event that you have entered either or both incorrect Wi-Fi SSID and Password in the Wi-Fi Client Mode setup for the RAK7243C LPWAN Developer Gateway to connect to the router, follow these set of steps for you to work again in Wi-Fi AP Mode and redo the setup.

- Remove the SD Card from your RAK7243C LPWAN Developer Gateway and insert it into your PC. Your PC should be able to detect it same with the image below:

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1583821091\/26838\/oyjadnh8ouvogrgpfox0.png",
        "mode": "responsive",
        "width": 496,
        "height": 386,
        "caption": "**Figure 22**: Creating rak_ap file to your SD Card"
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

- Check if the rak_ap file is created succesffuly. If so, re-insert the SD Card into your RAK7243C LPWAN Developer Gateway and it should work again in Wi-Fi AP Mode.

