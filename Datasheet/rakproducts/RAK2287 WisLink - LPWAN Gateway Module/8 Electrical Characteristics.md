---
type: page
title: Electrical Characteristics
listed: true
slug: electrical-characteristics-rak2287
---published

Stressing the device above one or more of the ratings listed in the Absolute Maximum Rating section may cause permanent damage. These are stress ratings only. Operating the module at these or at any conditions other than those specified in the Operating Conditions sections of the specification should be avoided. Exposure to Absolute Maximum Rating conditions for extended periods may affect device reliability.

The operating condition range defines those limits within which the functionality of the device is guaranteed. Where application information is given, it is advisory only and does not form part of the specification.

### Absolute Maximum Rating

Limiting values given below are in accordance with the Absolute Maximum Rating System (IEC 134).

| **Symbol** | **Description** | **Condition** | **Min.** | **Max.** | 
| ---- | ---- | ---- | ---- | ---- | 
| 3.3Vaux | Module supply voltage | Input DC voltage at 3.3Vaux pins | -0.3V | 3.6V | 
| USB | USB D+/D- pins | Input DC voltage at USB interface pins |  | 3.6V | 
| RESET | RAK2247 reset input | Input DC voltage at RESET input pin | -0.3V | 3.6V | 
| SPI | SPI interface | Input DC voltage at SPI interface pin | -0.3V | 3.6V | 
| GPS_PPS | GPS 1 pps input | Input DC voltage at GPS_PPS input pin | -0.3V | 3.6V | 
| Rho_ANT | Antenna ruggedness | Output RF load mismatch ruggedness at ANT1 |  | 10:1 VSWR | 
| Tstg | Storage Temperature |  | -40°C | 85°C | 


$plugin[{
    "type": "callout",
    "data": {
        "text": "The product is not protected against overvoltage or reversed voltages. If necessary, voltage spikes exceeding the power supply voltage specification, shown in the table above, must be limited to values within the specified boundaries by using appropriate protection devices.",
        "type": "info",
        "title": "Warning"
    }
}]$

### Maximum ESD

The table below lists the maximum ESD.

| **Parameter** | **Min** | **Typical** | **Max** | **Remarks** | 
| ---- | ---- | ---- | ---- | ---- | 
| **ESD_HBM** |  |  | 1000V | Charged Device Model JESD22-C101 CLASS III | 
| **ESD_CDM** |  |  | 300V | Charged Device Model JESD22-C101 CLASS III | 


$plugin[{
    "type": "callout",
    "data": {
        "text": "Although this module is designed to be as robust as possible, electrostatic discharge (ESD) can damage this module. This module must be protected at all times from ESD when handling or transporting. Static charges may easily produce potentials of several kilovolts on the human body or equipment, which can discharge without detection. Industry-standard ESD handling precautions should be used at all times.",
        "type": "info",
        "title": "Note:"
    }
}]$

### Power Consumption

| **Mode** | **Condition** | **Min.** | **Typical** | **Max.** | 
| ---- | ---- | ---- | ---- | ---- | 
| **Active-Mode(TX)** | The power of TX channel is 27dBm and 3.3V supply. | 511 mA | 512 mA | 513 mA | 
| **Active-Mode(RX )** | TX disabled and RX enabled. | 70 mA | 81.6 mA | 101 mA | 


### Power Supply Range

The table below lists the power supply range. The input voltage at **3.3Vaux** must be above the normal operating range minimum limit to switch-on the module.

| **Symbol** | **Parameter** | **Min**. | **Typical** | **Max**. | 
| ---- | ---- | ---- | ---- | ---- | 
| 3.3Vaux | Module supply operating input voltage14 | 3 V | 3.3 V | 3.6 V | 


