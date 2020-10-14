---
type: page
title: Connecting to LoRaServer
listed: true
slug: connecting-to-loraserver
---published

The LoRa Server project provides open-source components for building LoRaWAN networks. You can learn more about LoRaServer here: [https://www.loraserver.io/](https://www.loraserver.io/)

You can use RAK811 WisNode LoRa to connect with LoRaServer according to the following steps:

$plugin[{
    "type": "callout",
    "data": {
        "text": "In this section, it is an assumption that you have already connected your LoRa Gateway with TTN correctly. If not, please have a look at the document of RAK LoRa Gateway.",
        "type": "info",
        "title": "Note:"
    }
}]$

1.Open the web page of the **[LoRaServer](https://www.loraserver.io/)** which you want to connect with and login.

2.By default, there is already one or more items in this page, you can use it or create a new item. Now, let’s create a new item by clicking the “**CREATE**” button, then filling them in.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1562291715\/17310\/yplvkhjyrxm9sapww3ol.jpg",
        "mode": "responsive",
        "width": 1872,
        "height": 727,
        "caption": "**Figure 1.** LoRaServer Applications"
    }
}]$

3.Fill up the necessary information then Click "**CREATE APPLICATION**”.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1562291783\/17310\/qac4e0nktbhbck5nkemv.jpg",
        "mode": "responsive",
        "width": 1867,
        "height": 743,
        "caption": "**Figure 2.** Creating the Application"
    }
}]$

4.Click the new item name “**RAK811**”:

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1562291834\/17310\/isa3mwtqta79ubxd1ejs.jpg",
        "mode": "responsive",
        "width": 1874,
        "height": 716,
        "caption": "**Figure 3.** Applications page in LoRaServer"
    }
}]$

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1562291872\/17310\/lqbxn6ks165ggzgkbptt.jpg",
        "mode": "responsive",
        "width": 1874,
        "height": 713,
        "caption": "**Figure 4.** RAK811 Application"
    }
}]$

5.**Add** a LoRa node device into LoRaServer by clicking the “**CREATE**” button:

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1562291931\/17310\/vezamba2ziomcud2zb7f.jpg",
        "mode": "responsive",
        "width": 1837,
        "height": 696,
        "caption": "**Figure 5.** Adding a LoRa Node Device"
    }
}]$

6.Fill them in. You can generate a **Device EUI** automatically by clicking the Device EUI icon, or you can write the correct Device EUI in the edit box.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1562292567\/17310\/rot3ti2fdwthpqgksapr.jpg",
        "mode": "responsive",
        "width": 1887,
        "height": 745,
        "caption": "**Figure 6.** Filling the Device Parameters"
    }
}]$

$plugin[{
    "type": "callout",
    "data": {
        "text": "If you want to join in OTAA mode, select \u201c**DeviceProfile_OTAA**\u201d in the \u201cDevice-profile\u201d item. If you want to join in ABP mode and CN470 frequency, then, select \u201c**DeviceProfile_ABP_CN470**\u201d in the \u201cDevice-Profile\u201d item. If you want to join in ABP mode and other frequencies except AS923 and CN470, you should select \u201c**DeviceProfile_ABP**\u201d in the \u201cDevice-profile\u201d item.",
        "type": "info",
        "title": "Note:"
    }
}]$

### Join in OTAA mode

1.To join LoRaServer in OTAA mode, select “**DeviceProfile_OTAA**”.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1562293246\/17310\/dan8euazz75yhver4kbm.jpg",
        "mode": "responsive",
        "width": 1833,
        "height": 814,
        "caption": "**Figure 7.** Selecting OTAA Activation Mode in LoRaServer"
    }
}]$

2.Press “**CREATE DEVICE**” button. You may write the application key by yourself or generate it automatically by clicking the icon highlighted in the image.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1562293333\/17310\/hde51a7qezaoxhk5dfn1.jpg",
        "mode": "responsive",
        "width": 1832,
        "height": 525,
        "caption": "**Figure 8.** Application Key Generation"
    }
}]$

3.Click "**SET DEVICE KEYS**” button. Now, you’ve completed the configuration on LoRaServer.

- The Device EUI which was set in the previous section to your RAK811 WisNode LoRa as "dev_eui" is the same in the image highlighted below.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1562293480\/17310\/qrecsywmyrijsinf2ira.jpg",
        "mode": "responsive",
        "width": 1834,
        "height": 597,
        "caption": "**Figure 9.** Device EUI Code"
    }
}]$

- Same with the Application Key, which was set in the previous section as "app_key" is the same with the image highlighted.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1562294805\/17310\/rtywsssnzbfs10az1vmw.jpg",
        "mode": "responsive",
        "width": 1834,
        "height": 524,
        "caption": "**Figure 10.** Application Key LoRaWAN"
    }
}]$

$plugin[{
    "type": "callout",
    "data": {
        "text": "The Application EUI which was into RAK811 Breakout Board as \u201c**app_eui**\u201d is not needed for LoRaServer.",
        "type": "info",
        "title": "Note:"
    }
}]$

4.Next, let’s **configure** RAK811 WisNode LoRa by using **AT commands**. To do this, connect your RAK811 Breakout Board to a PC, power it on and open **RAK Serial Port Tool** on your computer.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1562295055\/17310\/nbnx0ntgtufnt6yz7cd8.jpg",
        "mode": "responsive",
        "width": 521,
        "height": 575,
        "caption": "**Figure 11.** RAK Serial Port Tool"
    }
}]$

- Now, let us join our RAK811 using the OTAA activation mode.

5.If the join mode is not in OTAA, just set the LoRa join mode to **OTAA** and LoRa class to **Class A** by typing the AT commands shown in the picture below.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1562295144\/17310\/uqrcr7xqyuekxraklxdq.jpg",
        "mode": "responsive",
        "width": 1053,
        "height": 574,
        "caption": "**Figure 12.** Setting of LoRaWAN mode and class"
    }
}]$

6.Type the following AT command to set the:**Frequency/Region to EU868, Device EUI, Application EUI and Application Key**:

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1562295217\/17310\/fcswnsyvq3m0y67wr2uv.jpg",
        "mode": "responsive",
        "width": 1053,
        "height": 588,
        "caption": "**Figure 13.** Setting of Frequency and Device EUI"
    }
}]$

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1562295252\/17310\/iohqjwnifyj7rs3ctbwo.jpg",
        "mode": "responsive",
        "width": 1053,
        "height": 588,
        "caption": "**Figure 14.** Setting of Application EUI and Key"
    }
}]$

7.Then, **join** in OTAA mode.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1562295506\/17310\/es7cpew86vr15nh5uvi4.jpg",
        "mode": "responsive",
        "width": 530,
        "height": 585,
        "caption": "**Figure 15.** Joining in OTAA"
    }
}]$

- **Joined Successfully!**

8.You can view the "**JoinRequest**" and "**JoinAccept**" on LoRaServer page:

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1562295602\/17310\/suwh9jzt0lrgevnnsbhi.jpg",
        "mode": "responsive",
        "width": 1884,
        "height": 490,
        "caption": "**Figure 16.** Join Request of the Device in the LoRaServer"
    }
}]$

9.Let’s try sending data from our RAK811 WisNode LoRa to the LoRaServer by typing the command below in the serial port.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1562295718\/17310\/snnzhvftmtyeio7emfpq.jpg",
        "mode": "responsive",
        "width": 529,
        "height": 589,
        "caption": "**Figure 17.** Sending Data to LoRaServer"
    }
}]$

You can see the message on LoRaServer page:

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1562295768\/17310\/goqdnusqpbagkb8fmrdq.jpg",
        "mode": "responsive",
        "width": 1873,
        "height": 613,
        "caption": "**Figure 18.** Message Received in LoraServer"
    }
}]$

### Join in ABP mode

1.If you select “**Device Profile  ABP**” or “**DeviceProfile_ABP_CN470**”, it means you want to join LoRaServer in **ABP mode**.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1562295935\/17310\/koe2ruobetxigbxx7ulq.jpg",
        "mode": "responsive",
        "width": 1830,
        "height": 806,
        "caption": "**Figure 19.** Switching to ABP Mode"
    }
}]$

2.Then you can see that there are some parameters for ABP in the “**ACTIVATION**” item:

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1562295993\/17310\/zll0rkgao0x2affiyptz.jpg",
        "mode": "responsive",
        "width": 1831,
        "height": 848,
        "caption": "**Figure 20.** ABP Parameters"
    }
}]$

3.Next, let’s use these parameters to set WisNode LoRa by using **AT command**. Let's join in **ABP** mode and set **EU868** frequency as an example.

4.If the join mode is not in ABP, just set the LoRa join mode to **ABP** and LoRa class to **Class A** by typing the following commands in RAK Serial Port Tool

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1562296273\/17310\/j2cjeo57ns8vv88owur5.jpg",
        "mode": "responsive",
        "width": 1053,
        "height": 588,
        "caption": "**Figure 21.** Setting of LoRaWAN Mode and Class"
    }
}]$

5.Type the following AT command to set your respective: **Frequency/Region**, **Device Address**, **Network Session Key** and **App Session Key**.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1562296401\/17310\/jt0hbf4uiqoo5izwuidv.jpg",
        "mode": "responsive",
        "width": 1053,
        "height": 588,
        "caption": "**Figure 22.** Setting of Frequency and Device Address"
    }
}]$

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1562296433\/17310\/aygmq0sz7m42tn5aqxct.jpg",
        "mode": "responsive",
        "width": 1053,
        "height": 588,
        "caption": "**Figure 23.** Setting of Device EUI and Network Key"
    }
}]$

6.Then, **join** in ABP mode.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1562296498\/17310\/mlerk3xq7winotkxzqf1.jpg",
        "mode": "responsive",
        "width": 525,
        "height": 585,
        "caption": "**Figure 24.** Joining of ABP"
    }
}]$

- Now, try sending data from our WisNode LoRa to the LoRa Server

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1562296565\/17310\/mie6hccw28vkifnfpiyi.jpg",
        "mode": "responsive",
        "width": 532,
        "height": 587,
        "caption": "**Figure 25.** Sending Data to LoRaServer"
    }
}]$

You can see the data which is just sent from RAK811 WisNode LoRa on LoRaServer page:

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1562296625\/17310\/u4dxovqn0bkmtwopgcpi.jpg",
        "mode": "responsive",
        "width": 1883,
        "height": 517,
        "caption": "**Figure 26.** Message Status in LoRaServer"
    }
}]$

