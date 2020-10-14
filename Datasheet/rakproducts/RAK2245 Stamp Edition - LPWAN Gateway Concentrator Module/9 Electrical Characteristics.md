---
type: page
title: Electrical Characteristics
listed: true
slug: electrical-characteristics-rak2245-stamp-edition
---published

The following are the electrical characteristics of RAK2245 Stamp Edition - LPWAN Gateway Concentrator Module. For further details, contact [**RAKwireless**](mailto:fomi@rakwireless.com).

### Absolute Maximum Rating

The values and range given below are all in accordance with the Absolute Maximum Rating System (IEC 134).

| **Parameter** | **Description** | **Min** | **Typical** | **Max** | 
| ---- | ---- | ---- | ---- | ---- | 
| **Supply Voltage (VDD)** | Input DC Voltage | -0.3V | 5.0V | 5.5V | 
| **Operating Temperature** | Temperature Range | -40°C |  | +85°C | 
| **RF Input Power** |  |  |  | -15dBm | 


$plugin[{
    "type": "callout",
    "data": {
        "text": "Stress exceeding one or more of the limiting values listed under \"Absolute Maximum Ratings\" may\ncause permanent damage to the radio module.",
        "type": "info",
        "title": "Note"
    }
}]$

### Maximum ESD

The table below shows the maximum ESD.

| **Parameter** | **Min** | **Typical** | **Max** | **Remarks** | 
| ---- | ---- | ---- | ---- | ---- | 
| **ESD sensitivity for all pins except ANT** |  |  | 1000V | Human Body Model according to JESD22-A 114 | 
| **ESD sensitivity for ANT** |  |  | 1000V | Human Body Model according to JESD22-A 114 | 
| **ESD immunity for ANT** |  |  | 4000V | Contact Discharge according to IEC 61000-4-2 | 
|  |  |  | 8000V | Air Discharge according to IEC 61000-4-2 | 


$plugin[{
    "type": "callout",
    "data": {
        "text": "The module is an Electrostatic Sensitive Device and require special precautions when\nhandling.",
        "type": "info",
        "title": "Note"
    }
}]$

### Power Consumption

| **Mode** | **Condition** | **Min** | **Typical** | **Max** | 
| ---- | ---- | ---- | ---- | ---- | 
| **Active-Mode (TX)** | TX Enabled and RX Disabled |  | 336mA |  | 
| **Active-Mode (RX)** | TX Disabled and RX Enabled |  | 360mA |  | 


