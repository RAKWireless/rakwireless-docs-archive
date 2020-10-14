---
type: page
title: Connecting to The Things Network (TTN)
listed: true
slug: connecting-to-the-things-network--ttn-
---published

The Things Network is about enabling low power devices to use long range [g](https://www.thethingsnetwork.org/docs/gateways/)ateways to connect to an open-source, decentralized network to exchange data with Application. Learn more about the Things Network [here](https://www.thethingsnetwork.org/docs/). In this section, we’ll do some practice to show how to connect RAK811 Breakout
Board with TTN.

1-  First, connect RAK811 Breakout Board with your PC and open the serial port tool on your PC.

2-  Open the serial port by clicking the following button:

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1561803308\/16639\/ktjvx0hhwkjzpsjilnpk.png",
        "mode": "responsive",
        "width": 540,
        "height": 660,
        "caption": "**Figure 1**: RAK811 Serial Port"
    }
}]$

$plugin[{
    "type": "callout",
    "data": {
        "text": "In this section, it is an assumption that you have connected your LoRa gateway with TTN correctly. If not, please have a look at the document of RAK LoRa Gateway.",
        "type": "info",
        "title": "Note!"
    }
}]$

3- Now go to the [TTN Website](https://www.thethingsnetwork.org/) and Log in.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1561803344\/16639\/qqgjugwxugejlkqjbvwa.png",
        "mode": "responsive",
        "width": 1149,
        "height": 562,
        "caption": "**Figure 2**: The Things Network Homepage"
    }
}]$

4- Choose "**Console**" located at the top right corner. Then, Click "**Application**".

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1561803298\/16639\/w5ehxtzkmvxphnhd1pwo.jpg",
        "mode": "responsive",
        "width": 1794,
        "height": 819,
        "caption": "**Figure 3**: TTN Console page"
    }
}]$

5- Press the "add application" button.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1561803365\/16639\/epxu14paovzcg8lgxdq6.jpg",
        "mode": "responsive",
        "width": 1822,
        "height": 446,
        "caption": "**Figure 4**: TTN Applications Page"
    }
}]$

6- Create your own Application by filling up with correct contents.

$plugin[{
    "type": "callout",
    "data": {
        "text": "Your Device ID is a unique ID of lower case, alphanumeric characters and nonconsecutive - and _.",
        "type": "info",
        "title": "Note!"
    }
}]$

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1561818653\/16639\/zvmw2u11xkvclrvxxajq.jpg",
        "mode": "responsive",
        "width": 1789,
        "height": 786,
        "caption": "**Figure 5**: TTN Adding Application Page"
    }
}]$

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1561819022\/16639\/lsywg3vctikdpcaaofyk.jpg",
        "mode": "responsive",
        "width": 1789,
        "height": 885,
        "caption": "**Figure 6**: Filling in TTN Parameters"
    }
}]$

7- Then press the “Add application” button at the bottom of this page, and you can see the following page:

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1561820243\/16639\/tbimbpc6pmjljmly09rg.jpg",
        "mode": "responsive",
        "width": 1783,
        "height": 919,
        "caption": "**Figure 7**: TTN Application Information Page"
    }
}]$

- At the middle of this page, you can find the box named “**DEVICES**”:

8- Click “**register device**”:

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1561820260\/16639\/nxo1mxbweflugbuiywdb.jpg",
        "mode": "responsive",
        "width": 1361,
        "height": 262,
        "caption": "**Figure 8**: Registering Device in TTN"
    }
}]$

9- Fill in the "**Device ID"** . Click the icon in the **“Device EUI**”, then a code is generated automatically.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1561820656\/16639\/kvdksm7bfnqpxpjqx9fs.jpg",
        "mode": "responsive",
        "width": 1789,
        "height": 885,
        "caption": "**Figure 9**: Filling up of Device Information"
    }
}]$

10- Then press the “**Register**” button at the bottom of this page to finish.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1561821087\/16639\/m18yecedpvuxsyoe808f.jpg",
        "mode": "responsive",
        "width": 1781,
        "height": 838,
        "caption": "**Figure 10**: Device Overview in TTN"
    }
}]$

When you connect the RAK811 to a LoRa Gateway, we need some amount of security and trust to be established amongst them. There are two connection modes, and we distinguish between them using the criteria of security and ease of implementation. These are the Over-The-Air Activation (OTAA) and Activation By Personalization (ABP).

### I. Join in OTAA mode

From the previous section, it can be seen that the default activation for TTN is OTAA. In joining OTAA, these three parameters are necessary: Device EUI, Application EUI and App Key.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1561821307\/16639\/w2hihmtvlrnmmrkhtahj.jpg",
        "mode": "responsive",
        "width": 1834,
        "height": 858,
        "caption": "**Figure 11**: Device OTAA Parameters"
    }
}]$

Now, let us join our RAK811 using the OTAA activation mode.

$plugin[{
    "type": "callout",
    "data": {
        "text": "The default LoRa work mode is LoRaWAN 1.0.2, while the default LoRa join mode is OTAA, and the default LoRa class is Class A.",
        "type": "info",
        "title": "Note"
    }
}]$

If the join mode is not in OTAA, just set the LoRa join mode to OTAA and LoRa class to Class A. Open your RAK811 Firmware and type the following commands. 

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1561847563\/16639\/ncdlfcwzdgqtkmdsymj2.jpg",
        "mode": "responsive",
        "width": 1046,
        "height": 573,
        "caption": "**Figure 12**: Setting of LoRa Mode and Class"
    }
}]$

- Type the following AT command to set the: **Frequency/Region to EU868, Device EUI, Application EUI and Application Key**:

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1561848594\/16639\/uecai1mzhd8gr5piyhmc.jpg",
        "mode": "responsive",
        "width": 1051,
        "height": 575,
        "caption": "**Figure 13**: Setting of Frequency and Device EUI"
    }
}]$

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1561848633\/16639\/edho4pbk0pdlm3lcufch.jpg",
        "mode": "responsive",
        "width": 1061,
        "height": 576,
        "caption": "**Figure 14**.:Setting of App EUI and App Key"
    }
}]$

- Then, join in OTAA mode.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1561848737\/16639\/dw2kbzqrqiye5salp0ho.jpg",
        "mode": "300",
        "width": 530,
        "height": 587,
        "caption": "**Figure 15**: Joinng OTAA Mode"
    }
}]$

- Joined Successfully! Now, try sending data from our RAK811 Breakout Board to TTN.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1561848849\/16639\/px8ed8bacurn4efwd1zi.jpg",
        "mode": "300",
        "width": 528,
        "height": 585,
        "caption": "**Figure 16**: Sending Data to TTN from RAK811"
    }
}]$

- We can view the data sent from the Breakout Board to our The Things Network  Application Data

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1561849007\/16639\/gketo3xxtors4hbsw4h3.jpg",
        "mode": "responsive",
        "width": 1780,
        "height": 601,
        "caption": "**Figure 17**: View Sent Data through TTN"
    }
}]$

Great! That's all about OTAA Mode. 

### II. Join in ABP mode

- To join the ABP mode, go to device settings and switch the activation method to ABP.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1561849665\/16639\/vnhdqwblvmzkhomq65tn.jpg",
        "mode": "responsive",
        "width": 1198,
        "height": 618,
        "caption": "**Figure 18**: Switching the Activation Method to ABP"
    }
}]$

- Set the Device Address, Network Session Key and App Session Key.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1561849704\/16639\/oxwuaapf29nc3rcs8hmd.jpg",
        "mode": "responsive",
        "width": 1788,
        "height": 923,
        "caption": "**Figure 19**: Setting the ABP Parameters"
    }
}]$

- These three parameters will be used on RAK811 Breakout Board:

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1561849717\/16639\/gaph6eos8h2geqvmzz0y.jpg",
        "mode": "responsive",
        "width": 1713,
        "height": 875,
        "caption": "**Figure 20**: ABP Parameters Codes"
    }
}]$

OK! Now, let’s join in ABP mode and set EU868 frequency as an example.

- If the join mode is not in ABP, just set the LoRa join mode to ABP and LoRa class to Class A. Open your RAK811 Firmware and type the following commands. 

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1561850175\/16639\/oj45s6qxzuqbirwpqvlp.jpg",
        "mode": "responsive",
        "width": 855,
        "height": 459,
        "caption": "**Figure 21**: Setting of LoRa Mode and Class"
    }
}]$

- Type the following AT command to set the: **Frequency/Region to EU868, Device Address, Network Session Key and App Session Key**:

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1561850190\/16639\/dgpu0z8zuksawdbp8t0b.jpg",
        "mode": "responsive",
        "width": 839,
        "height": 460,
        "caption": "**Figure 22**: Setting of Frequency and Device Address"
    }
}]$

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1561850214\/16639\/qpb2wrqewi1byqtvrpvg.jpg",
        "mode": "responsive",
        "width": 1073,
        "height": 592,
        "caption": "**Figure 23**: Setting of Network and Application Key"
    }
}]$

- Then, join in ABP mode.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1561850245\/16639\/rvonlh2oszjgytlhz5tv.jpg",
        "mode": "300",
        "width": 528,
        "height": 587,
        "caption": "**Figure 24**: Joining in ABP Mode"
    }
}]$

$plugin[{
    "type": "callout",
    "data": {
        "text": "Actually, it is no need to join in ABP mode. But you still need to set this ATcommand to valid the parameters which you just set for ABP mode.",
        "type": "info",
        "title": "Note"
    }
}]$

- Joined Successfully. Now, try sending data from our RAK811 Breakout Board to TTN.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1561850267\/16639\/n6prjfkfeyukng6jvl5l.jpg",
        "mode": "300",
        "width": 524,
        "height": 583,
        "caption": "**Figure 25**: Sending Data to TTN"
    }
}]$

- We can view the data sent from the Breakout Board to our The Things Network  Application Data

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1561850293\/16639\/g8szqmcpnnfefqhnpncn.jpg",
        "mode": "responsive",
        "width": 1776,
        "height": 547,
        "caption": "**Figure 26**: Received Message in TTN Site"
    }
}]$

Up next: You will learn about the steps in connecting your device to LoRaServer.

