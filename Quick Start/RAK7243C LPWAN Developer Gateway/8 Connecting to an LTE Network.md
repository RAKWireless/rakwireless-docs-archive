---
type: page
title: Connecting to an LTE Network
listed: false
slug: connecting-to-an-lte-network
---published

The RAK7243C comes with the RAK2013 Cellular making it capable of connecting through LTE network. In this section, you will learn on how to connect your Gateway to an LTE network.

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
        "caption": "**Figure 1:** Configure LTE Module"
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
        "caption": "**Figure 2**: LTE Configuration Options"
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
        "caption": "**Figure 3**: Minicom Tool"
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
        "caption": "**Figure 4**: AT Command in Minicom"
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
        "caption": "**Figure 5**: AT Command for LTE Network Query"
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
        "caption": "**Figure 6**: LTE Network Example"
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
        "caption": "**Figure 7**: Sample LTE Networks in EU"
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
        "caption": "**Figure 8**: Sample AT Command for LTE Network"
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
        "caption": "**Figure 9:** Configure APN Name"
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
        "caption": "**Figure 10**: APN Name"
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
        "caption": "**Figure 11**: Baud Rate Setting"
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
        "caption": "**Figure 12**: IP address Information"
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
        "caption": "**Figure 13**: Enabling the Automatic LTE Connection during Start-Up"
    }
}]$

Alright, you had successfully connect through the three interfaces: Wi-Fi, Ethernet and Cellular, so let us proceed on how to extract the application data through the different servers.

