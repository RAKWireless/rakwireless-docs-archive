---
type: page
title: Connecting to Cellular Network
listed: true
slug: connectin-to-cellular-network
---published

This document is a sample guide on how to connect you RAK8212 iTracker Pro to a Cellular Network.

1.Insert a SIM Card into your RAK8212 iTracker Pro .

2.Make sure that your
RAK8212 iTracker Pro is connected to your mobile device over BLE according to the [auto$](/rak8212-itracker-pro/configuring-your-rak8212) document.

3.Now, send “**at+scan=cellular**” from Mobile device over BLE to RAK8212 iTracker Pro as shown in the image below:

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1580196459\/21936\/kzxbfaxur2zen98rb4c2.jpg",
        "mode": "responsive",
        "width": 307,
        "height": 626,
        "caption": "**Figure 1**: AT+command for scanning Cellular Network"
    }
}]$

4.Wait for about 20 seconds, and you should see  some information similar to the image shown below in the RTT Viewer:

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1580196466\/21936\/izdlr0fc2sywzr9zvlja.jpg",
        "mode": "responsive",
        "width": 1122,
        "height": 601,
        "caption": "**Figure 2**: Cellular Network Scan in RTT Viewer"
    }
}]$

$plugin[{
    "type": "callout",
    "data": {
        "text": "There may be several\nCellular operator\u2019s network signal detected upon scanning. In this document, the cellular networks available are CHINA MOBILE and CHN-UNICOM Cellular network.",
        "type": "info",
        "title": "Note:"
    }
}]$

