---
type: page
title: Connecting to LoRaServer
listed: true
slug: connecting-to-loraserver
---published

The LoRa Server project provides open-source components for building LoRaWAN networks. You can learn more about LoRaServer here: [https://www.loraserver.io/](https://www.loraserver.io/)

You can use RAK811 Breakout Board to connect with LoRaServer by following this steps:

$plugin[{
    "type": "callout",
    "data": {
        "text": "In this section, it is an assumption that you have already connected your LoRa Gateway with TTN correctly. If not, please have a look at the document of RAK LoRa Gateway.",
        "type": "info",
        "title": "Note!"
    }
}]$

OK! Let’s get started!

- Open the web page of the **[LoRaServer](https://www.loraserver.io/)** which you want to connect with and login.
- By default, there is already one or more items in this page, you can use it or create a
new item. Now, let’s create a new item by clicking the “**CREATE**” button, then filling them in.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1561856809\/17094\/rvuwppg8ngoejml0ncmr.jpg",
        "mode": "full",
        "width": 1872,
        "height": 727,
        "caption": "**Figure 1**: LoRaServer Applications"
    }
}]$

- Click "**CREATE APPLICATION**”.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1561856848\/17094\/ucrphj98kfxxjbevpsrc.jpg",
        "mode": "responsive",
        "width": 1867,
        "height": 743,
        "caption": "**Figure 2**: Creating the Application"
    }
}]$

- Click the new item name “**RAK811**”:

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1561856884\/17094\/x8tutan4wi3jb8yucynm.jpg",
        "mode": "responsive",
        "width": 1874,
        "height": 716,
        "caption": "**Figure 3**: Applications page in LoRaServer"
    }
}]$

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1561856935\/17094\/z0hooihszu0uexhvk6cg.jpg",
        "mode": "responsive",
        "width": 1874,
        "height": 713,
        "caption": "**Figure 4**: RAK811 Application"
    }
}]$

- Add a LoRa node device into LoRaServer by clicking the “CREATE” button:

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1561856960\/17094\/ep7h37x6nathi9t7o9en.jpg",
        "mode": "responsive",
        "width": 1837,
        "height": 696,
        "caption": "**Figure 5**: Adding a LoRa Node Device"
    }
}]$

- Fill them in. You can generate a Device EUI automatically by clicking the Device EUI icon, or you can write the correct Device EUI in the edit box.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1561857048\/17094\/xjfznprvswebabqrlmuy.jpg",
        "mode": "full",
        "width": 1887,
        "height": 745,
        "caption": "**Figure 6**: Filling the Device Parameters"
    }
}]$

$plugin[{
    "type": "callout",
    "data": {
        "text": "If you want to join in OTAA mode, select \u201cDeviceProfile_OTAA\u201d in\nthe \u201cDevice-profile\u201d item. If you want to join in ABP mode and CN470 frequency, then, select \u201cDeviceProfile_ABP_CN470\u201d in the \u201cDevice-Profile\u201d item. If you want to\njoin in ABP mode and other frequencies except AS923 and CN470, you should select \u201cDeviceProfile_ABP\u201d in the \u201cDevice-profile\u201d item.",
        "type": "info",
        "title": "Note!"
    }
}]$

### I. Join in OTAA mode

- To join LoRaServer in OTAA mode, select “**DeviceProfile_OTAA**”.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1561874665\/17094\/v3hcaslrfqd33bs44pnz.jpg",
        "mode": "responsive",
        "width": 1833,
        "height": 814,
        "caption": "**Figure 7**: Selecting OTAA Activation Mode in LoRaServer"
    }
}]$

- Press “**CREATE DEVICE**” button. You may write the application key by yourself or generate it automatically by clicking the icon highlighted in the image. 

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1561874660\/17094\/wo9srzyshijok1wqegpz.jpg",
        "mode": "responsive",
        "width": 1832,
        "height": 525,
        "caption": "**Figure 8**: Application Key Generation"
    }
}]$

- Click "**SET DEVICE KEYS**” button. Now,  you’ve completed the configuration on LoRaServer.
- The Device EUI which was set in the previous section to your RAK811 Breakout Board as "dev_eui" is the same in the image highlighted below.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1561874677\/17094\/kzilukfs93t2a9zscnke.jpg",
        "mode": "responsive",
        "width": 1834,
        "height": 597,
        "caption": "**Figure 9**: Device EUI Code"
    }
}]$

- Same with the Application Key, which was set in the previous section as "app_key" is the same with the image highlighted.  

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1561874701\/17094\/fozijzdyji0afuxrpwnc.jpg",
        "mode": "responsive",
        "width": 1834,
        "height": 524,
        "caption": "**Figure 10**: Application Key LoRaWAN"
    }
}]$

$plugin[{
    "type": "callout",
    "data": {
        "text": "The Application EUI which was into RAK811 Breakout Board as \u201capp_eui\u201d is not needed for LoRaServer.",
        "type": "info",
        "title": "Note"
    }
}]$

- Next, let’s configure RAK811 Breakout Board by using AT commands.
- To do this, connect your RAK811 Breakout Board to a PC, power it on and open RAK Serial
Port Tool on your desktop.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1561874925\/17094\/eavhe1ajd2ivlokyuyn6.jpg",
        "mode": "300",
        "width": 521,
        "height": 575,
        "caption": "**Figure 11**: RAK811 Serial Port"
    }
}]$

Now, let us join our RAK811 using the OTAA activation mode.

- If the join mode is not in OTAA, just set the LoRa join mode to OTAA and LoRa class to Class A by typing the AT commands shown in the picture below.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1561875390\/17094\/awuodzx5wyzdzqcn7izd.jpg",
        "mode": "responsive",
        "width": 1053,
        "height": 574,
        "caption": "**Figure 12**: Setting of LoRaWAN mode and class"
    }
}]$

- Type the following AT command to set the: **Frequency/Region to EU868, Device EUI, Application EUI and Application Key**:

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1561875400\/17094\/x1mgqhhog658mxuk0kry.jpg",
        "mode": "responsive",
        "width": 1053,
        "height": 588,
        "caption": "**Figure 13**: Setting of Frequency and Device EUI"
    }
}]$

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1561875428\/17094\/jyqrqhlb4lkosdts7jhp.jpg",
        "mode": "responsive",
        "width": 1053,
        "height": 588,
        "caption": "**Figure 14**: Setting of Application EUI and Key"
    }
}]$

- Then, join in OTAA mode.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1561875456\/17094\/rrwb7y83gp6thfefa7gk.jpg",
        "mode": "300",
        "width": 530,
        "height": 585,
        "caption": "**Figure 15**: Joining in OTAA"
    }
}]$

- Joined Successfully!
- You can view the "**JoinRequest**" and "**JoinAccept**" on LoRaServer page:

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1561875490\/17094\/p6iptnuccrmolbk0nwfu.jpg",
        "mode": "responsive",
        "width": 1884,
        "height": 490,
        "caption": "**Figure 16**: Join Request of the Device in the LoRaServer"
    }
}]$

- Let’s try sending data from our RAK811 Breakout Board to the LoRaServer by typing the command below in the serial port.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1561875545\/17094\/jreuwo9ltr8wxuvwxqvx.jpg",
        "mode": "300",
        "width": 529,
        "height": 589,
        "caption": "**Figure 17**: Sending Data to LoRaServer"
    }
}]$

- You can see the message on LoRaServer page:

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1561875556\/17094\/no5gx6ecj6rtuhh7mjmf.jpg",
        "mode": "responsive",
        "width": 1873,
        "height": 613,
        "caption": "**Figure 18**: Message Received in LoraServer"
    }
}]$

### II. Join in ABP mode

- If you select “Device_Profile_ABP” or “DeviceProfile_ABP_CN470”, it means you want
to join LoRaServer in ABP mode.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1561875615\/17094\/chabxwk3jf1c5hgnwydg.jpg",
        "mode": "responsive",
        "width": 1830,
        "height": 806,
        "caption": "**Figure 19**: Switching to ABP Mode"
    }
}]$

- Then you can see that there are some parameters for ABP in the “**ACTIVATION**” item:

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1561875627\/17094\/hxmidezt50lfcremnvie.jpg",
        "mode": "responsive",
        "width": 1831,
        "height": 848,
        "caption": "**Figure 20**: ABP Parameters"
    }
}]$

Next, we will use these parameters to set our RAK811 Breakout Board by using AT
command.

- OK! Now, let’s join in ABP mode and set EU868 frequency as an example.
- If the join mode is not in ABP, just set the LoRa join mode to ABP and LoRa class to Class A by typing the following commands in RAK811 Serial Port.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1561875955\/17094\/gqtphxufiuzjjce7ntju.jpg",
        "mode": "responsive",
        "width": 1053,
        "height": 588,
        "caption": "**Figure 21**: Setting of LoRaWAN Mode and Class"
    }
}]$

- Type the following AT command to set the: Frequency/Region to EU868, Device Address, Network Session Key and App Session Key

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1561876029\/17094\/oyg2rw7k88vkzkspa0qt.jpg",
        "mode": "responsive",
        "width": 1053,
        "height": 588,
        "caption": "**Figure 22**: Setting of Frequency and Device Address"
    }
}]$

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1561876038\/17094\/bmtgvr18se6bjmwr4bwg.jpg",
        "mode": "responsive",
        "width": 1053,
        "height": 588,
        "caption": "**Figure 23**: Setting of Device EUI and Network Key"
    }
}]$

- Then, join in ABP mode.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1561876724\/17094\/ign9kaim1g4ldroipnuc.jpg",
        "mode": "300",
        "width": 525,
        "height": 585,
        "caption": "**Figure 24**: Joining of ABP"
    }
}]$

- Now, try sending data from our Board to the LoRa Server

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1561876069\/17094\/zle3r38ayhz3ibdauemh.jpg",
        "mode": "300",
        "width": 532,
        "height": 587,
        "caption": "**Figure 25**: Sending Data to LoRaServer"
    }
}]$

- You can see the data which is just sent from RAK811 Breakout Board on LoRaServer
page:

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1561876750\/17094\/urs2wgxcrb7ldawjddsm.jpg",
        "mode": "responsive",
        "width": 1883,
        "height": 517,
        "caption": "**Figure 26**: Message Status in LoRaServer"
    }
}]$

- That’s all about “Join in ABP mode” with LoRaServer.

Great! You have successfully finished connecting your RAK811 Breakout Board to the LoRaServer.

