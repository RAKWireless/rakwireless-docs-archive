---
type: page
title: Connect the RAK7431 to the Sensor
listed: true
slug: connect-the-rak7431-to-the-sensor
---published

### Power Interface Configuration

The RAK7431 device can be powered either by:

- DC (VIN/GND) terminals
- Micro USB. 

The DC screw terminals are supporting 8 to 48 VDC. The Micro USB port can be used to power the RAK7431, up to 5 V / 500 mA DC. At the same time, the USB port is used as the configuration port for the device. Using the USB cable to connect the RAK7431 to a computer’s USB port, you can import your configuration settings. 

$plugin[{
    "type": "callout",
    "data": {
        "text": "The\nMicro USB port can be used only for powering the device. It cannot provide\npower to VOUT and power other devices in the RS485 network.",
        "type": "info",
        "title": "Note:"
    }
}]$

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1597125591\/41157\/eifpgdzzkigiujfsx8as.png",
        "mode": "responsive",
        "width": 1388,
        "height": 778,
        "caption": "**Figure 1**: RAK7431 bridge with connected sensor and power supply"
    }
}]$

### Data Interface Configuration

The RAK7431 - RS485 serial interface can support up to **16 RS485 devices**. VOUT on the data interface can supply external power to the RS485 connected devices (only when the device is powered from the DC input). The VOUT output voltage is the same as the DC input voltage VIN.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1597125913\/41157\/z3wzawpxynqs4xfqsc44.jpg",
        "mode": "responsive",
        "width": 694,
        "height": 645,
        "caption": "**Figure 2**: RAK7431 Interface pin definition"
    }
}]$

