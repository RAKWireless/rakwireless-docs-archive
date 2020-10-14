---
type: page
title: Electrical Characteristics
listed: false
slug: electrical-characteristics-rak2245-pi-hat
---published

The following are the electrical characteristics of RAK2245 Pi HAT. Please [contact us ](mailto:fomi@rakwireless.com)if you need other details for your project

### Absolute Maximum Rating

The values and range given below are all in accordance with Absolute Maximum Rating System (IEC 134)

| **Parameter** | **Description** | **Min.** | **Typ.** | **Max** | 
| ---- | ---- | ---- | ---- | ---- | 
| **Supply Voltage (VDD)** | Input DC Voltage | -0.3V | 5.0V | 5.5V | 
| **Operating Temperature** | Temperature Range | -40°C |  | +85°C | 
| **RF Input Power** |  |  |  | -15dBm | 


$plugin[{
    "type": "callout",
    "data": {
        "text": "With RF output power level above +15 dBm a minimum distance to a transmitter should be 1m for avoiding too large input level.",
        "type": "info",
        "title": "Note"
    }
}]$

### Maximum ESD

The table below lists the maximum ESD

| **Parameter** | **Min** | **Typical** | **Max** | **Remarks** | 
| ---- | ---- | ---- | ---- | ---- | 
| **ESD sensitivity for all pins except ANT1** |  |  | 1kV | Human Body Model according to JESD22-A114 | 
| **ESD sensitivity for ANT1** |  |  | 1kV | Human Body Model according to JESD22-A114 | 
| **ESD immunity for ANT1** |  |  | 4kV | Contact Discharge according to IEC 61000-4-2 | 
|  |  |  | 8kV | Air Discharge according to IEC 61000-4-2 | 


$plugin[{
    "type": "callout",
    "data": {
        "text": "The module is an Electrostatic Sensitive Device and require special precautions when handling.",
        "type": "info",
        "title": "Note"
    }
}]$

### Operating Conditions

The table below lists the operation temperature range.

| **Parameter** | **Min.** | **Typical** | **Max** | **Remarks** | 
| ---- | ---- | ---- | ---- | ---- | 
| **Normal Operating Temperature** | -40°C | +25°C | +85°C | Fully functional and meets 3GPP specifications | 


### Power Consumption

| **Mode** | **Condition** | **Min** | **Typical** | **Max** | 
| ---- | ---- | ---- | ---- | ---- | 
| **Active-Mode (TX)** | TX Enabled and RX Disabled |  | 336mA |  | 
| **Active-Mode (RX)** | TX Disabled and RX Enabled |  | 360mA |  | 


