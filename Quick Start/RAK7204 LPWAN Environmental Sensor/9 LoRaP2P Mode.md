---
type: page
title: LoRaP2P Mode
listed: true
slug: lorap2p-mode
---published

The setup process for the RAK7204 LPWAN Environmental Sensor in LoRaP2P Mode is just the same with the process with the RAK811 Wisnode. These are the steps that you need to follow for this mode:

1. First, find two RAK7204 LPWAN Environmental Sensor which can work on EU868 frequency and make sure their firmware version isn’t less than V3.0.0.1.
2. Next, connect these two RAK7204 LPWAN Environmental Sensor with PC through USB cable, and open two serial port tool on PC.
3. Now, configure them to both work in LoRaP2P mode as follow:

$plugin[{
    "type": "code-block",
    "data": {
        "languageBlocks": [
            {
                "code": "at+set_config=lora:work_mode:1",
                "language": "none"
            }
        ]
    }
}]$

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1567416751\/18997\/esrws29ubqsdrtzhxoyl.jpg",
        "mode": "responsive",
        "width": 545,
        "height": 705,
        "caption": "**Figure 1:**  LoRaP2P Mode"
    }
}]$

Then configure LoRaP2P parameters for both of them as follow for example:

$plugin[{
    "type": "code-block",
    "data": {
        "languageBlocks": [
            {
                "code": "at+set_config=lorp2p:869525000:7:0:1:5:5",
                "language": "none"
            }
        ]
    }
}]$

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1567416800\/18997\/be2eudcfjshdfpp70dh3.jpg",
        "mode": "responsive",
        "width": 1100,
        "height": 672,
        "caption": "**Figure 2:** LoRaP2P Configuration"
    }
}]$

OK! Try to send a message from RAK7204 - 2 (the right one) to RAK7204 - 1 (the left one):

$plugin[{
    "type": "code-block",
    "data": {
        "languageBlocks": [
            {
                "code": "at+send=lorap2p:1234567890",
                "language": "none"
            }
        ]
    }
}]$

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1567416833\/18997\/hxqc6l5zeadhs5yd5ucz.jpg",
        "mode": "responsive",
        "width": 1106,
        "height": 698,
        "caption": "**Figure 3:** Test Message Sent"
    }
}]$

**Success!** You can send more messages:

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1567416864\/18997\/xiafisnstyg1641kojgl.jpg",
        "mode": "responsive",
        "width": 1102,
        "height": 699,
        "caption": "**Figure 4:** More message sent"
    }
}]$

Similarly, you can send message from RAK7204 1 to RAK7204 2 surely. Just try it freely. Great! We’ve done it, and that’s all about how to use
LoRaP2P on RAK811 WisNode.

You can use RAK7204 LoRaP2P mode according to it.

### ADR and DR

You can open the ADR feature of RAK7204 by using the following AT command:

$plugin[{
    "type": "code-block",
    "data": {
        "languageBlocks": [
            {
                "code": "at+set_config=lora:adr:1",
                "language": "none"
            }
        ]
    }
}]$

or you can close the ADR feature of RAK7204 by using this AT command: 

$plugin[{
    "type": "code-block",
    "data": {
        "languageBlocks": [
            {
                "code": "at+set_config=lora:adr:0",
                "language": "none"
            }
        ]
    }
}]$

There is also an AT command which is used to set the DataRate(DR):

| **AT Command** | **Description** | 
| ---- | ---- | 
| at+set_config=lora:dr:X | Set the DR of the Node<br><br>**X** : the<br>number of DR. Generally, the value of X can be 0~5. More details, please check<br>the LoRaWAN® 1.0.2 specification. | 


For example, if you want to set the current DR to DR0, you just do as follow: 

$plugin[{
    "type": "code-block",
    "data": {
        "languageBlocks": [
            {
                "code": "at+set_config=lora:dr:0",
                "language": "none"
            }
        ]
    }
}]$

