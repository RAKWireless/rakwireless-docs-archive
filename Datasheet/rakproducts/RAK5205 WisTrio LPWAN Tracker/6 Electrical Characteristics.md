---
type: page
title: Electrical Characteristics
listed: true
slug: electrical-characteristics-rak5205
---published

### Working Mode

The board supports to enable the GPS low power mode, it has a 3-axis MEMS Sensor LIS3DH, which can detect the user's motion status, when the device is stationary, it will enter the low power sleep mode, reducing the overall power consumption and increase battery life. The power consumption as shown in the following table.

| **Mode** | **Power Consumption** | 
| ---- | ---- | 
| Sleep Mode | 14.5µA (Minimum) | 
| Normal Mode | 174mA (Maximum) @ 20dBm and GPS Enabled | 


### Power Requirements

The RAK5205 LPWAN Tracker Board has an operating voltage of 3.7V. It can be powered by micro USB with 5V Max.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1563168019\/17645\/o6kt2mf83avccxb0eilp.png",
        "mode": "600",
        "width": 766,
        "height": 275,
        "caption": "**Figure 1:** Powered by Micro USB"
    }
}]$

The board can also be powered by a 3.7V Li-Ion battery. You can connect a 5V solar panel charger to recharge the Li-Ion battery.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1563168073\/17645\/ae5ovwpb0m2etbfukvp5.png",
        "mode": "300",
        "width": 563,
        "height": 747,
        "caption": "**Figure 2:** RAK5205 With 5V Solar Panel, Plastic Enclosure and Li-ion Battery"
    }
}]$

