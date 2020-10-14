---
type: page
title: LoRa® P2P Mode
listed: true
slug: lora-p2p-mode
---published

This document show how to communicate **two (2) RAK811 LPWAN Evaluation Boards** via LoRa® P2P Mode. We will be using EU868 as our frequency, although it is applicable to other standard bands.

1- First, find two RAK811 LPWAN Evaluation Board which can work on EU868 frequency and make sure their firmware version isn’t less than V3.0.0.1.

2- Next, connect these two RAK811 LPWAN Evaluation Board with PC through UART, and open two serial port tool on PC.

3- Now, configure them to both work in LoRa P2P mode as follow:

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1579524515\/21924\/wiyvchxtiv4tgr3izuff.png",
        "mode": "responsive",
        "width": 1375,
        "height": 899,
        "caption": "**Figure 1**: P2P Initialization"
    }
}]$

4- Then configure LoRa® P2P parameters for both of them as follow for example:

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1572052347\/-1\/vctdlxrvu3lx48qfgxi9.jpg",
        "mode": "responsive",
        "width": 959,
        "height": 585,
        "caption": "**Figure 2**: Configuring P2P in both RAK811 Nodes"
    }
}]$

5- OK! Try to send a message from WisNode 1 to WisNode 2:

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1572052436\/-1\/og3igkq8zhfftiaunbt6.jpg",
        "mode": "responsive",
        "width": 910,
        "height": 581,
        "caption": "**Figure 3**: Message sent and received status in the two Nodes"
    }
}]$

6- Successfully! Now, send more messages.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1572052454\/-1\/jsqpvwg7m8cwl7zr4zf5.jpg",
        "mode": "responsive",
        "width": 921,
        "height": 586,
        "caption": "**Figure 4**: Succeeding Messages sent to the other Node"
    }
}]$

Yehey! You have successfully finished your RAK811 LPWAN Evaluation Board Set Up. You are now ready to develop the coolest project that could potentially change the world.

