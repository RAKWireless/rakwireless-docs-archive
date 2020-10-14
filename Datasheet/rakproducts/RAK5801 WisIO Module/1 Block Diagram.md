---
type: page
title: Block Diagram
listed: false
slug: block-diagram-rak5801
---draft

The RAK5801 module was designed to convert 4-20mA current signals into voltage signals by applying a resistor. As shown in Figure 1, this voltage signal is conditioned with an operational amplifier to the level supported by an analog input of an MCU. Inside of the MCU, the analog signal is then digitalized by an ADC.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1595482189\/32358\/u4w741tavlbzyuxyo8uh.png",
        "mode": "responsive",
        "width": 837,
        "height": 386,
        "caption": "**Figure 1**: RAK5801 Block Diagram"
    }
}]$

Once the signal is digitalized, you can recover the original current value by applying the following relation:

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1595483092\/32358\/lvg9fdvmomei5a8un9py.jpg",
        "mode": "responsive",
        "width": 225,
        "height": 43,
        "caption": null
    }
}]$

Where:

_**I** = Original Current_

_**U** = ADC Reading_

