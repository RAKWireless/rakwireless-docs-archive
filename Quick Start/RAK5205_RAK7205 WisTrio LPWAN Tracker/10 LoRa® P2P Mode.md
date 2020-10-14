---
type: page
title: LoRa® P2P Mode
listed: true
slug: lora-p2p-mode
---published

In this section, I’ll show how to use LoRa® P2P mode. We will be using EU868 as our frequency, although it is applicable to other standard bands.

**1.**First, find two **RAK5205 LPWAN Tracker** which can work on EU868 frequency and make sure their firmware version isn’t less than **V3.0.0.1**.

**2.** Next, connect these two RAK5205 LPWAN Tracker with PC through UART, and open two serial port tool on PC.

**3.** Now, configure them to both work in LoRaP2P mode as follow:

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
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1564555453\/-1\/qytvsg9mx3y4drl7pwrg.png",
        "mode": "responsive",
        "width": 491,
        "height": 629,
        "caption": "**Figure 1**: P2P Initialization"
    }
}]$

**4.** Then configure LoRaP2P parameters for both of them as follow for example:

$plugin[{
    "type": "code-block",
    "data": {
        "languageBlocks": [
            {
                "code": "at+set_config=lorap2p:869525000:7:0:1:5:5",
                "language": "none"
            }
        ]
    }
}]$

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1564555476\/-1\/fyoulppnh8gdz3vawjv7.jpg",
        "mode": "responsive",
        "width": 959,
        "height": 585,
        "caption": "**Figure 2**: Configuring P2P in both RAK5205 Nodes"
    }
}]$

**5.** OK! Try to send a message from LPWAN Breakout Module 2 (the right one) to LPWAN Breakout Module 1 (the left one):

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
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1564555525\/-1\/khjhkisjuxtjb5oxps94.png",
        "mode": "responsive",
        "width": 910,
        "height": 581,
        "caption": "**Figure 3**: Message sent and received status in the two Nodes"
    }
}]$

**6.** Successfully! Now, send more messages.

$plugin[{
    "type": "code-block",
    "data": {
        "languageBlocks": [
            {
                "code": "at+send=lorap2p:12345678901234567890",
                "language": "none"
            }
        ]
    }
}]$

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1564555560\/-1\/ckbymbjhypol3p0q1bjp.jpg",
        "mode": "responsive",
        "width": 921,
        "height": 586,
        "caption": "**Figure 4**: Succeeding Messages sent to the other Node"
    }
}]$

Yehey! You have successfully  finished your RAK5205 LPWAN Tracker Set Up. You are now ready to develop the coolest project that could potentially change the world.

