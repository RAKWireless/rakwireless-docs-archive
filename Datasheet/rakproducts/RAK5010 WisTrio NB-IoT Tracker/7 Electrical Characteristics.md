---
type: page
title: Electrical Characteristics
listed: true
slug: electrical-characteristics-rak5010-wistrio-nb-iot-tracker
---published



### Absolute Maximum Ratings

Stresses above those listed as “absolute maximum ratings” may cause permanent damage to the device. This is a stress rating, functional operation of the device under these conditions is not advised. Exposure to maximum rating conditions may affect device reliability.


| **Ratings** | **Maximum Value (V)** | 
| ---- | ---- | 
| Vbus, power supply onUBS port | -0.3 - 5.5 | 
| Vbat, battery voltage | -0.3 - 4.3 | 
| Vconn solar panel voltage | -0.3 - 5.5 | 
| IOs of J-link (J9) | -0.3 - 1.9 | 
| IOs of BG96, nRF52840 - J10 and J12 | -0.3 -VREF | 
| ESD | 2000 | 

$plugin[{
    "type": "callout",
    "data": {
        "text": "The RAK5010, as any electronic equipment is sensitive to electrostatic discharge (ESD), improper handling can cause permanent damage to module.",
        "type": "warning",
        "title": "Warning!"
    }
}]$



### Current Consumption


| **Conditions** | **Current** | 
| ---- | ---- | 
| The nRF52840 isRunning, the BG96 transmits data @ NB1, 23dBm | 200 mA | 
| BLE transmits @ 0dBm,the BG96 is in power saving mode | 7 mA | 
| The nRF52840 is insleep mode, the BG96 is in power saving mode | 13 µA | 

$plugin[{
    "type": "callout",
    "data": {
        "text": "For\nthe above results to be reached, the nRF52840's regulator has to be in DC-DC\nmode and all the sensors have to be in sleep mode.",
        "type": "info",
        "title": "Note"
    }
}]$



### Power Requirements

The RAK5010 tracker board can be powered by a battery, connected to the P2. The nominal operational voltage of the battery should be within the range in the table:


| **Min.** | **Type** | **Max.** | **Unit** | 
| ---- | ---- | ---- | ---- | 
| 3.3 | 3.7 | 4.3 | V | 

If a rechargeable
battery is used, the USB connector is used as a charging port. The voltage and
current fed to the battery through the port should not exceed the ones in the
table below.


| **Parameter** | **Value** | 
| ---- | ---- | 
| Charging Voltage | 4.5-5.5 V | 
| Charging Current | 500 mA | 

A suitable Li-Ion battery would have the following parameters:


| **Parameter** | **Value** | 
| ---- | ---- | 
| Standard Voltage | 3.7 V | 
| Charging Voltage | 4.2 V | 
| Capacity | As required | 
| Discharge Current | 2A | 

$plugin[{
    "type": "callout",
    "data": {
        "text": "If\na non-rechargeable battery is connected to the RAK5010, please never power USB\nport, it will damage the battery, might damage the board and is considered a fire\nhazard.",
        "type": "info",
        "title": "Note"
    }
}]$


_A 5V Solar panel can be connected to the board
via the P1 connector to serve for the purpose of charging the battery._


$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1583746281\/18970\/zgpiejkvfwbsdrgrntaz.jpg",
        "mode": "responsive",
        "width": 768,
        "height": 809,
        "caption": "**Figure 1**: Battery Charging via Solar Panel"
    }
}]$



### Laboratory Testings

The figures below are the average current consumptions based on the different test cases.

**Equipments**:

- Oscilloscope
- RAK5010 WisTrio NB-IoT Tracker

**LoRa® Packet Sending**

The RAK5010 WisTrio NB-IoT Tracker takes **489.733 ms** to send a LoRa® packet which consumes **64.9 mA** of current.

- **Sending Time**: 489.733 ms
- **Current consumption**: 64.9 mA


$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1583833433\/18935\/yv0boh4rb6zwi5rgmck6.jpg",
        "mode": "responsive",
        "width": 1660,
        "height": 1007,
        "caption": "**Figure 1**: Oscilloscope Screen Capture of LoRa\u00ae Packet Sending"
    }
}]$


**Sleep Mode**

The RAK5010 WisTrio NB-IoT Tracker when in sleep mode consumes **20.5 uA** of current.

- **Current consumption**: 20.5 uA


$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1583833598\/18935\/f1i08phmcueg00pvi3hm.jpg",
        "mode": "responsive",
        "width": 1679,
        "height": 914,
        "caption": "**Figure 2**: Oscilloscope Screen Capture of RAK4600 LoRa\u00ae Module in sleep mode"
    }
}]$




