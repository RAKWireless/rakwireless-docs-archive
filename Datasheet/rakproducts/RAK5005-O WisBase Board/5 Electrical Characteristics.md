---
type: page
title: Electrical Characteristics
listed: false
slug: electrical-characteristics-rak5005-o
---draft

### Absolute Maximum Ratings

Shown in the table below are the Absolute Maximum ratings of the device. The stress ratings are the functional operation of the device. 

$plugin[{
    "type": "callout",
    "data": {
        "text": "1.If the stress rating goes above what is listed may cause permanent damage to the device. \n\n2.Under the listed conditions is not advised.\n\n3.Exposure to maximum rating conditions may affect the device reliability.",
        "type": "warning",
        "title": "Warning"
    }
}]$

| **Ratings** | Maximum Value | Unit | 
| ---- | ---- | ---- | 
| Power Supply on the USB port (**Vbus**) | –0.3 to 5.5 | V | 
| Battery Voltage (**Vbat**) | –0.3 to 4.3 | V | 
| Solar Panel Voltage (**Vconn**) | –0.3 to 5.5 | V | 
| IOs of WisConnector | –0.3 to VDD+0.3 | V | 
| ESD | 2000 | V | 


$plugin[{
    "type": "callout",
    "data": {
        "text": "The RAK5005-O, as any electronic equipment, is sensitive to electrostatic discharge (ESD). Improper handling can cause permanent damage to module.",
        "type": "info",
        "title": "Info"
    }
}]$

### Current Consumption

The RAK5005-O designs for low power IoT products and the power supply use low grounding current regulator, when there is no module on RAK5005-O, the leakage current is lower than 2µA. With MCU and sensor on it, the sleep current is lower than 10µA. When the LoRa module is transmitting, the current may reach to 130mA.

| **Conditions** | **Current** | **Unit** | 
| ---- | ---- | ---- | 
| Leakage current, without any module on RAK5005-O | 2 | µA | 
| Idle current, with MCU and sensor are in sleep mode | 10 | µA | 
| Working current, with LoRa module is transmitting | 130 | µA | 


### Battery and Solar Panel Specification

The RAK5005-O WisBase board can be powered by a battery, connected to the P1 connector. The nominal operating voltage of the battery should be within the range showed in the following table.

| **Minimum** | **Typical** | **Maximum** | **Unit** | 
| ---- | ---- | ---- | ---- | 
| 3.3 | 3.7 | 4.3 | V | 


If a rechargeable battery is used, the USB connector is used as a charging port. The voltage and current fed to the battery through the port should not exceed to its charging limits, as shown in the table below.

| **Parameter** | **Value** | 
| ---- | ---- | 
| Charging Voltage | 4.5 – 5.5V | 
| Charging Current | 500 mA | 


A suitable Li-Ion battery should have the following parameters as shown in the table below:

| **Parameter** | **Value** | 
| ---- | ---- | 
| Standard Voltage | 3.7V | 
| Chargine VOltage | 4.2V | 
| Capacity | As required | 
| Discharge current | At least 500mA | 


$plugin[{
    "type": "callout",
    "data": {
        "text": "If a non-rechargeable battery is connected to the RAK5005-O, rework the hardware by removing the R17 on the bottom of RAK5005-O to disconnect the charger circuit. Otherwise, the USB port with try to charge the battery, and will damage the non-rechargeable battery, might damage the board, and is considered a fire or explode hazard.",
        "type": "info",
        "title": "Info"
    }
}]$

### Solar Panel Connector

A 5V Solar panel can be connected to the board via the P2 connector to also serves the purpose of charging the battery.

