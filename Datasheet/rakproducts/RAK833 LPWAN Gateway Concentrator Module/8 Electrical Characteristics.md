---
type: page
title: Electrical Characteristics
listed: true
slug: electrical-characteristics-rak833
---published

## Absolute Maximum Rating

The limiting values given below are in accordance with the **Absolute Maximum Rating System (IEC 134)**.

$plugin[{
    "type": "callout",
    "data": {
        "text": "Stressing the device above one or more of the ratings listed in the Absolute Maximum Rating section may cause permanent damage. These are stress ratings only. Operating the module at these or any conditions other than those specified in the Operating Conditions section of the specification should be avoided. Exposure to Absolute Maximum Rating conditions for extended periods may affect device reliability.",
        "type": "warning",
        "title": "Warning:"
    }
}]$

| **Symbol** | **Description** | **Condition** | **Min**. | **Max.** | **Unit** | 
| ---- | ---- | ---- | ---- | ---- | ---- | 
| 3.3Vaux | Module supply voltage | Input DC voltage at 3.3Vaux pins | –0.3 | 3.6 | V | 
| USB | USB D+/D- pins | Input DC voltage at<br>USB interface pins |  | 3.6 | V | 
| SPDT_SEL | Port select | Input DC voltage at<br>SPDT_SEL input pins | –0.3 | 3.6 | V | 
| RESET | RAK833 reset input | Input DC voltage at<br>RESET input pin | –0.3 | 3.6 | V | 
| SPI | SPI interface | Input DC voltage at<br>SPI interface pin | –0.3 | 3.6 | V | 
| GPS_PPS | GPS 1 pps input | Input DC voltage at<br>GPS_PPS input pin | –0.3 | 3.6 | V | 
| Rho_ANT | Antenna ruggedness | Output RF load<br>mismatch ruggedness at ANT1 |  | 10:1 | VSWR | 
| Tstg | Storage Temperature |  | –40 | 85 | °C | 


$plugin[{
    "type": "callout",
    "data": {
        "text": "**The product is not protected against over-voltage or reversed voltages**. If necessary, voltage spikes exceeding the power supply voltage specification, shown in the table above, must be limited to values within the specified boundaries by using appropriate protection devices.",
        "type": "warning",
        "title": "Warning:"
    }
}]$

## Maximum Electrostatic Discharge (ESD)

$plugin[{
    "type": "callout",
    "data": {
        "text": "RAK833 LPWAN Gateway Concentrator Module are **Electrostatic Sensitive Devices** and require special\nprecautions when handling.",
        "type": "info",
        "title": "Note:"
    }
}]$

| **Parameter** | **Min** | **Typical** | **Max** | **Unit** | **Remarks** | 
| ---- | ---- | ---- | ---- | ---- | ---- | 
| ESD sensitivity for all pins except ANT1 |  |  | 1000 | V | Human Body Model according to JESD22-A114 | 
| ESD sensitivity for ANT1 |  |  | 1000 | V | Human Body Model according to JESD22-A114 | 
| ESD immunity for ANT1 |  |  | 4000 | V | Contact Discharge according to IEC 61000-4-2 | 
|  |  |  | 8000 | V | Air Discharge according to IEC 61000-4-2 | 


## Operating Conditions

Unless otherwise indicated, all operating condition specifications are at an ambient temperature of **25°C**.

$plugin[{
    "type": "callout",
    "data": {
        "text": "Operation beyond the operating conditions is not recommended and extended exposure beyond them may affect device reliability.",
        "type": "warning",
        "title": "Warning:"
    }
}]$

### Operating Temperature Range

| **Parameter** | **Min**. | **Typical** | **Max**. | **Unit** | **Remarks** | 
| ---- | ---- | ---- | ---- | ---- | ---- | 
| Normal operating temperature | –20 | +25 | +65 | °C | Normal operating temperature range<br><br>(fully functional and meet 3GPP specifications) | 
| Extended operating temperature | –40 |  | +85 | °C | Extended operating temperature range<br><br>(RF performance may be affected outside normal<br><br>operating range, though module is fully functional) | 


### Supply/power pins

Input voltage at **3.3Vaux** must be above the normal operating range minimum limit to switch-on the module.

| **Symbol** | **Parameter** | **Min.** | **Typical** | **Max.** | **Unit** | 
| ---- | ---- | ---- | ---- | ---- | ---- | 
| 3.3Vaux | Module supply operating input voltage | 3.00 | 3.30 | 3.60 | V | 


### Current consumption

| **Mode** | **Condition** | **Min** | **Type** | **Max** | **Unit** | 
| ---- | ---- | ---- | ---- | ---- | ---- | 
| Idle-Mode | All of the chip on the board enter idle mode or shutdown. | 60 | 100 |  | uA | 
| Active-Mode (TX) | The power of TX channel is 23dBm and 3.3V supply. |  | TBD |  | mA | 
| Active-Mode (RX ) | TX disabled and shutdown PA. |  | TBD |  | mA | 


