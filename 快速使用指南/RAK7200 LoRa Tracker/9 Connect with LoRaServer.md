---
type: page
title: Connect with LoRaServer
listed: true
slug: connect-with-loraserver
---published

The LoRa Server project provides open-source components for building LoRaWAN networks. You can learn more about LoRaServer here: [https://www.loraserver.io/](https://www.loraserver.io/)

You can use RAK7200 LoRa Tracker to connect with LoRaServer by following this steps:

$plugin[{
    "type": "callout",
    "data": {
        "text": "In this section, it is an assumption that you have already connected your LoRa Gateway with TTN correctly. If not, please have a look at the document of RAK LoRa Gateway.",
        "type": "info",
        "title": "Note"
    }
}]$

 OK! Let’s get started!

1.Open the web page of the **[LoRaServer](https://www.loraserver.io/)** which you want to connect with and login. 

2.By default, there is already one or more items in this page, you can use it or create a new item. Now, let’s create a new item by clicking the “**CREATE**” button.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1563606414\/17852\/p4azdumgi2r9nr8ubfmr.jpg",
        "mode": "responsive",
        "width": 1872,
        "height": 727,
        "caption": "**Figure 1.** LoRaServer Applications"
    }
}]$

3.Fill up the necessary information then Click "**CREATE APPLICATION**"

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1564062476\/17852\/ps8yq2qkgzcxzqgwjhrt.jpg",
        "mode": "responsive",
        "width": 1875,
        "height": 710,
        "caption": "**Figure 2.** Creating the Application"
    }
}]$

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1564062997\/17852\/x2dacsqxayqpki5kdqrh.jpg",
        "mode": "responsive",
        "width": 1870,
        "height": 723,
        "caption": "**Figure 3.** Applications page in LoRaServer"
    }
}]$

4.Click the new Item name "RAK7200_test"

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1564062965\/17852\/ovogtwoqcbuwnewbcurn.jpg",
        "mode": "responsive",
        "width": 1869,
        "height": 733,
        "caption": "**Figure 4.** RAK7200 Application"
    }
}]$

5.**Add**a LoRa node device into LoRaServer by clicking the “**CREATE**” button:

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1564063073\/17852\/ggpj5gvtnhgbmohyfniy.jpg",
        "mode": "responsive",
        "width": 1835,
        "height": 705,
        "caption": "**Figure 5.** Adding a LoRa Node Device"
    }
}]$

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1564063087\/17852\/omsz1vr2nfxtzxgomj9p.jpg",
        "mode": "responsive",
        "width": 1872,
        "height": 753,
        "caption": "**Figure 6.** Filling the Device Parameters"
    }
}]$

6.Fill them in. You can generate a **Device EUI** automatically by clicking the Device EUI icon, or you can write the correct Device EUI in the edit box.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1564063118\/17852\/tzor7mj24hu9duddpqju.jpg",
        "mode": "responsive",
        "width": 1834,
        "height": 735,
        "caption": "**Figure 7:** Generating Device EUI Automatically"
    }
}]$

$plugin[{
    "type": "callout",
    "data": {
        "text": "If you want to join in OTAA mode, select \u201c**DeviceProfile_OTAA**\u201d in the \u201cDevice-profile\u201d item. If you want to join in ABP mode and CN470 frequency, then, select \u201c**DeviceProfile_ABP_CN470**\u201d in the \u201cDevice-Profile\u201d item. If you want to join in ABP mode and other frequencies except AS923 and CN470, you should select \u201c**DeviceProfile_ABP**\u201d in the \u201cDevice-profile\u201d item.",
        "type": "info",
        "title": "Note"
    }
}]$

### Join in OTAA Mode

1.To join LoRaServer in OTAA mode, select “**DeviceProfile_OTAA**”.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1564063406\/17852\/nintfxx4e4rzxbymubee.jpg",
        "mode": "responsive",
        "width": 1827,
        "height": 733,
        "caption": "**Figure 8:** Selecting OTAA Activation Mode in LoRaServer"
    }
}]$

2.Press “**CREATE DEVICE**” button. You may write the application key by yourself or generate it automatically by clicking the icon highlighted in the image.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1564063918\/17852\/n3ruu94pjc4sz6iiamx6.jpg",
        "mode": "responsive",
        "width": 1829,
        "height": 708,
        "caption": "**Figure 9:** Application Key Generation"
    }
}]$

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1564063808\/17852\/a56bieelhtppzrhekiu6.jpg",
        "mode": "responsive",
        "width": 1864,
        "height": 725,
        "caption": "**Figure 10:** Generated Application Key"
    }
}]$

3.Click "**SET DEVICE KEYS**” button. Now, you’ve completed the configuration on LoRaServer.

- The Device EUI which was set in the previous section to your RAK7200 LoRa Tracker as "dev_eui" is the same in the image highlighted below

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1564064010\/17852\/kngd3ykqxorz3jfspc3b.jpg",
        "mode": "responsive",
        "width": 1832,
        "height": 706,
        "caption": "**Figure 11:** Device EUI Code"
    }
}]$

- Same with the Application Key, which was set in the previous section as "app_key" is the same with the image highlighted

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1564064050\/17852\/gwiogolmd39wukj1cfsv.jpg",
        "mode": "responsive",
        "width": 1829,
        "height": 705,
        "caption": "**Figure 12:**Application Key LoRaWAN"
    }
}]$

$plugin[{
    "type": "callout",
    "data": {
        "text": "The Application EUI which was into RAK7200 LoRa Tracker as \u201c**app_eui**\u201d is not needed for LoRaServer.",
        "type": "info",
        "title": "Note"
    }
}]$

1. Next, let’s **configure** RAK7200 by using **AT commands**. To do this, connect your RAK7200 to a PC, power it on and open **RAK Serial Port Tool** on your computer.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1564064301\/17852\/zpihqbih3iricqa87snz.jpg",
        "mode": "600",
        "width": 676,
        "height": 824,
        "caption": "**Figure 13:** RAK Serial Port Tool"
    }
}]$

- Now, let us join our RAK811 using the OTAA activation mode.

5.If the join mode is not in OTAA, just set the LoRa join mode to **OTAA** and LoRa class to **Class A** by typing the AT commands shown in the picture below.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1564064516\/17852\/v8ziigiduse7yzb7is7t.jpg",
        "mode": "responsive",
        "width": 1342,
        "height": 826,
        "caption": "**Figure 14:** Setting of LoRaWAN mode and class"
    }
}]$

6.Type the following AT command to set your respective:**Frequency/Region , Device EUI, Application EUI and Application Key**:

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1564065488\/17852\/unymliivsdqq4b9gktff.jpg",
        "mode": "responsive",
        "width": 1342,
        "height": 826,
        "caption": "**Figure 15.** Setting of Frequency and Device EUI"
    }
}]$

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1564065572\/17852\/xalqvvq11yamdcyw4wdy.jpg",
        "mode": "responsive",
        "width": 1342,
        "height": 826,
        "caption": "**Figure 16:** Setting of Application EUI and Key"
    }
}]$

7.Then, **join** in OTAA mode.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1564065951\/17852\/jkq0onpgztq1rsqwpj1h.jpg",
        "mode": "600",
        "width": 678,
        "height": 820,
        "caption": "**Figure 17:** Joining in OTAA"
    }
}]$

- **Joined Successfully!**

8.You can view the "**JoinRequest**" and "**JoinAccept**" on LoRaServer page:**
**

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1564065979\/17852\/ykxpp4jnanif4bkw7cf6.jpg",
        "mode": "responsive",
        "width": 1870,
        "height": 734,
        "caption": "**Figure 18:** Join Request of the Device in the LoRaServer"
    }
}]$

### Join in ABP Mode

1.If you select “**Device Profile ABP**” or “**DeviceProfile_ABP_CN470**”, it means you want to join LoRaServer in **ABP mode**.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1564066225\/17852\/aenpgcuags16kocl7zm6.jpg",
        "mode": "responsive",
        "width": 1834,
        "height": 739,
        "caption": "**Figure 19:** Switching to ABP Mode"
    }
}]$

2.Then you can see that there are some parameters for ABP in the “**ACTIVATION**” item:

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1564067127\/17852\/ykocin7wnj0gufuv1ow3.jpg",
        "mode": "responsive",
        "width": 1830,
        "height": 769,
        "caption": "**Figure 20:** ABP Parameters"
    }
}]$

3.Next, let’s use these parameters to set RAK7200 by using **AT command**.

4.If the join mode is not in ABP, just set the LoRa join mode to **ABP** and LoRa class to **Class A** by typing the following commands in RAK Serial Port Tool

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1564067527\/17852\/elfrqiagntf6ec8vd1o0.jpg",
        "mode": "responsive",
        "width": 1342,
        "height": 826,
        "caption": "**Figure 21:** Setting of LoRaWAN Mode and Class"
    }
}]$

5.Type the following AT command to set your respective: **Frequency/Region**, **Device Address**, **Network Session Key** and **App Session Key**.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1564067839\/17852\/sva7nmvy1j9ab83qqcs4.jpg",
        "mode": "responsive",
        "width": 1342,
        "height": 826,
        "caption": "**Figure 22:** Setting of Frequency and Device Address"
    }
}]$

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1564067856\/17852\/qcorwrdxobjkgyiihgf0.jpg",
        "mode": "responsive",
        "width": 1342,
        "height": 826,
        "caption": "**Figure 23:** Setting of Device EUI and Network Key"
    }
}]$

- Then Join in ABP Mode

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1564067990\/17852\/uqcf4aa3f4jcncgtokio.jpg",
        "mode": "600",
        "width": 678,
        "height": 820,
        "caption": "**Figure 24:** Joining of ABP"
    }
}]$

You can see the data which is just sent from RAK7200 on LoRaServer page:

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1564068079\/17852\/pikpqbqtbhiiw4wapsia.jpg",
        "mode": "responsive",
        "width": 1834,
        "height": 710,
        "caption": "**Figure 25:**  Message Status in LoRaServer"
    }
}]$

