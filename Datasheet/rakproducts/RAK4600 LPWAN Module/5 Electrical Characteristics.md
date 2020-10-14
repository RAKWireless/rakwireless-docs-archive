---
type: page
title: Electrical Characteristics
listed: true
slug: electrical-characteristics---rak4600-lora-module
---published

## Electrical Consumption

Several current consumption ratings are provided below for detailed RAK4600 LPWAN Module usage. Please refer to the values below for your preferred values for specific simulations and calculations.

### Typical Current Consumption

Shown in the table provided below is the typical current consumption of the RAK4600 LPWAN Module.

| **Item** | **Current Consumption** | **Condition** | 
| ---- | ---- | ---- | 
| **LoRa® TX** @20dBm | 125mA | LoRa® @ PA_BOOST & BT sleep | 
| **LoRa® TX** @17dBm | 92mA | LoRa® @ PA_BOOST & BT sleep | 
| **BT TX** @4dBm | 9mA | BT Tx mode & LoRa® sleep | 
| **LoRa® RX** @37.5Kbps | 17mA |  | 
| **BT RX** @2Mbps | 11.5mA |  | 
| **Node Sleep** | 2.0uA | The whole board is in sleep mode | 


### Laboratory Testing

The figures below are the average current consumption based on the different test cases.

**Equipments**:

- Oscilloscope
- RAK4600 LPWAN Module

**LoRa® Packet Sending**

The RAK4600 LPWAN Module takes **92.291 ms** to send a LoRa® packet which consumes **119 mA** of current. 

- **Sending Time**: 92.291 ms
- **Current consumption**: 119 mA

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1583723578\/22250\/awyqt4s9r3469vtgai1p.jpg",
        "mode": "responsive",
        "width": 1074,
        "height": 803,
        "caption": "**Figure 1**: Oscilloscope Screen Capture of LoRa\u00ae Packet Sending"
    }
}]$

**LoRa® Packet Receiving**

The RAK4600 LPWAN Module takes **30.052 ms** to receive a LoRa® packet which consumes **13.8 mA** of current. 

- **Receiving Time**: 30.052 ms
- **Current consumption**: 13.8 mA

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1583730496\/22250\/ufgf8mxmibztzhezvr6l.jpg",
        "mode": "responsive",
        "width": 1073,
        "height": 803,
        "caption": "**Figure 2**: Oscilloscope Screen Capture of LoRa\u00ae Packet Receiving"
    }
}]$

**Sleep Mode**

The RAK4600 LPWAN Module when in sleep mode consumes **11.2 uA** of current.

- **Current consumption**: 11.2 uA

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1583731893\/22250\/bpm1nbybf4exvnop89yo.jpg",
        "mode": "responsive",
        "width": 1072,
        "height": 801,
        "caption": "**Figure 3**: Oscilloscope Screen Capture of RAK4600 LPWAN Module in sleep mode"
    }
}]$

