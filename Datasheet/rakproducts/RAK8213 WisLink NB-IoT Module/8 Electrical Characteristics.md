---
type: page
title: Electrical Characteristics
listed: true
slug: electrical-characteristics-rak8213
---published

### Operation and Storage Temperatures

| **Parameter** | **Minimum** | **Typical** | **Maximum** | **Unit** | 
| ---- | ---- | ---- | ---- | ---- | 
| Operation Temperature Range _(1)_ | -35 | +25 | +75 | ºC | 
| Extended Temperature Range _(2)_ | -40 |  | +85 | ºC | 
| Storage Temperature Range | -40 |  | +90 | ºC | 


$plugin[{
    "type": "callout",
    "data": {
        "text": "(1) Within operation temperature range, the module is 3GPP compliant.\n\n_(2)_  Within extended temperature range, the module retains the ability to establish     and maintain a voice, SMS, data transmission, emergency call, etc. There is no     unrecoverable malfunction. There are also no effects on radio spectrum and no harm     to radio network. Only one or more parameters like Pout might reduce in their value     and exceed the specified tolerances. When the temperature returns to the normal     operating temperature levels, the module will meet 3GPP specifications again.",
        "type": "info",
        "title": "Note"
    }
}]$

### Current Consumption

Current Consumption with the **GNSS off**.

| **Parameter** | **Description** | **Condition** | **Typical**_(1)_ | **Unit** | 
| ---- | ---- | ---- | ---- | ---- | 
| **IVBAT** | **Leakage Current** | Power off mode | 8 | µA | 
|  | **PSM** | Power Saving Mode @Real Network | 10 | µA | 
|  | **Rock Bottom Sleep**_(2)_ | AT+CFUN=0 @Sleep State | 0.8 | mA | 
|  | **Sleep State**_(3)_ | DRX=1.28s @ Instrument | 1.5 | mA | 
|  |  | DRX=1.28s @ Instrument | 1.96 | mA | 
|  |  | e-I-DRX=20.48s @ Instrument | 1.2 | mA | 
|  |  | e-I-DRX=20.48s @ Instrument | 1.1 | mA | 
|  |  | @Real 2G Network | 2.0 | mA | 
|  | **Idle State** | DRX=1.28s @ Instrument | 15 | mA | 
|  |  | DRX=1.28s @ Instrument | 15 | mA | 
|  |  | e-I-DRX=20.48s @ Instrument | 15 | mA | 
|  |  | e-I-DRX=20.48s @ Instrument | 15 | mA | 
|  |  | @Real 2G Network | 15 | mA | 
|  | **LTE Cat M1 Data Transfer (GNSS OFF)** | LTE-FDD B1 @23.31dBm | 220 | mA | 
|  |  | LTE-FDD B2 @23.05dBm | 208 | mA | 
|  |  | LTE-FDD B3 @23.09dBm | 214 | mA | 
|  |  | LTE-FDD B4 @23.19dBm | 214 | mA | 
|  |  | LTE-FDD B5 @23.22dBm | 210 | mA | 
|  |  | LTE-FDD B8 @21.83dBm | 203 | mA | 
|  |  | LTE-FDD B12 @21.88dBm | 215 | mA | 
|  |  | LTE-FDD B13 @21.96dBm | 197 | mA | 
|  |  | LTE-FDD B18 @23.04dBm | 212 | mA | 
|  |  | LTE-FDD B19 @23.13dBm | 211 | mA | 
|  |  | LTE-FDD B20 @23.07dBm | 209 | mA | 
|  |  | LTE-FDD B25 @23.01dBm | 211 | mA | 
|  |  | LTE-FDD B26 @TBD | TBD | mA | 
|  |  | LTE-FDD B28 @22.52dBm | 215 | mA | 
|  |  | LTE-TDD B39 @TBD | TBD | mA | 
|  | **LTE Cat NB1 Data Transfer (GNSS OFF)** | LTE-FDD B1 @22.8dBm | 170 | mA | 
|  |  | LTE-FDD B2 @22.6dBm | 171 | mA | 
|  |  | LTE-FDD B3 @22.6dBm | 161 | mA | 
|  |  | LTE-FDD B4 @22.6dBm | 161 | mA | 
|  |  | LTE-FDD B5 @22.9dBm | 156 | mA | 
|  |  | LTE-FDD B8 @22.7dBm | 170 | mA | 
|  |  | LTE-FDD B12 @23dBm | 170 | mA | 
|  |  | LTE-FDD B13 @22.9dBm | 167 | mA | 
|  |  | LTE-FDD B18 @23.1dBm | 159 | mA | 
|  |  | LTE-FDD B19 @22.9dBm | 155 | mA | 
|  |  | LTE-FDD B20 @22.7dBm | 157 | mA | 
|  |  | LTE-FDD B25 @23dBm | 165 | mA | 
|  |  | LTE-FDD B26 @TBD | TBD | mA | 
|  |  | LTE-FDD B28 @22.5dBm | 163 | mA | 
|  | **GPRS Data Transfer (GNSS OFF)** | GSM850 4UL 1DL @30.17dBm | 575 | mA | 
|  |  | GSM850 3UL 2DL @32dBm | 533 | mA | 
|  |  | GSM850 2UL 3DL @32.74dBm | 402 | mA | 
|  |  | GSM850 1UL 4DL @32.52dBm | 220 | mA | 
|  |  | EGSM900 4UL 1DL @30.54dBm | 586 | mA | 
|  |  | EGSM900 3UL2DL @31.36dBm | 556 | mA | 
|  |  | EGSM900 2UL 3DL @32.62dBm | 399 | mA | 
|  |  | EGSM900 1UL 4DL @32.75dBm | 228 | mA | 
|  |  | DCS1800 4UL 1DL @29.81dBm | 543 | mA | 
|  |  | DCS1800 3UL 2DL @30.09dBm | 426 | mA | 
|  |  | DCS1800 2UL 3DL @30.1dBm | 301 | mA | 
|  |  | DCS1800 1UL4DL @30.34dBm | 182 | mA | 
|  |  | PCS1900 4UL 1DL @29.64dBm | 516 | mA | 
|  |  | PCS1900 3UL 2DL @29.86dBm | 404 | mA | 
|  |  | PCS1900 2UL 3DL @29.7dBm | 281 | mA | 
|  |  | PCS1900 1UL 4DL @29.94dBm | 171 | mA | 
|  | **EDGE Data Transfer (GNSS OFF)** | GSM850 4UL1DL @26.02dBm | 403 | mA | 
|  |  | GSM850 3UL 2DL @26.11dBm | 312 | mA | 
|  |  | GSM850 2UL 3DL @26.57dBm | 224 | mA | 
|  |  | GSM850 1UL 4DL @26.92dBm | 224 | mA | 
|  |  | EGSM900 4UL 1DL @25.92dBm | 136 | mA | 
|  |  | EGSM900 3UL 2DL @26.11dBm | 391 | mA | 
|  |  | EGSM900 2UL 3DL @26.16dBm | 301 | mA | 
|  |  | EGSM900 1UL 4DL @26.88dBm | 217 | mA | 
|  |  | DCS1800 4UL 1DL @24.7dBm | 133 | mA | 
|  |  | DCS1800 3UL 2DL @25.97dBm | 373 | mA | 
|  |  | DCS1800 2UL 3DL @25.03dBm | 286 | mA | 
|  |  | DCS1800 1UL 4DL @25.03dBm | 208 | mA | 
|  |  | PCS1900 4UL1DL @24.92dBm | 127 | mA | 
|  |  | PCS1900 3UL 2DL @24.86dBm | 375 | mA | 
|  |  | PCS1900 2UL 3DL @25.17dBm | 288 | mA | 
|  |  | PCS1900 1UL 4DL @25.31dBm | 207 | mA | 
|  | *_LTE Voice (GNSS OFF) *_ | Voice @LTE Cat M1 network | 108 | mA | 


$plugin[{
    "type": "callout",
    "data": {
        "text": "_(1)_**Typical value** means the average current consumption value. \n\n_(2)_**Rock Bottom Sleep** means the operation is performed with **AT+CFUN=0** and     **AT+QSLCK=1** (DTR pin at high level). \n\n_(3)_**Sleep state** with UART connected and USB disconnected. The module can enter         sleep mode through executing the **AT+QSCLK=1** command via the UART interface and then         controlling the module\u2019s DTR pin.",
        "type": "info",
        "title": "Note"
    }
}]$

**GNSS** Current Consumption:

| **Description** | **Conditions** | **Typical** | **Unit** | 
| ---- | ---- | ---- | ---- | 
| Searching (AT+CFUN=0) | Cold Start @Passive Antenna | 41.7 | mA | 
|  | Lost State @Passive Antenna | 42.0 | mA | 
| Tracking (AT+CFUN=0) | Instrument Environment | 21.7 | mA | 
|  | Open Sky @Passive Antenna | 36.0 | mA | 
|  | Open Sky @Active Antenna | 35.0 | mA | 


### RF Output Power

 The following table shows the RF output power of RAK8213:

| **Frequency** | **Max** | **Min** | 
| ---- | ---- | ---- | 
| LTE-FDD B1/B2/B3/B4/B5/B8/B12/B13/B18/B19/B20/B25/ B26/B28 | 23dBm±2dB |  | 
| LTE-TDD B39 | 23dBm±2dB |  | 
| GSM850/EGSM900 | 33dBm±2dB | 5dBm±5dB | 
| DCS1800/PCS1900 | 30dBm±2dB | 0dBm±5dB | 
| GSM850/EGSM900 (8-PSK) | 27dBm±3dB | 5dBm±5dB | 
| DCS1800/PCS1900 (8-PSK) | 26dBm±3dB | 0dBm±5dB | 


### RF Receiving Sensitivity

$plugin[{
    "type": "callout",
    "data": {
        "text": "The values for the sensitivity in the table are all in **dBm.**",
        "type": "info",
        "title": "Note"
    }
}]$

| **Network** | **Band** | **Primary** | **Diversity** | **Cat M1/ 3GPP** | **Cat NB1**_(1)_**/3GPP** | **GSM/3GPP** | 
| ---- | ---- | ---- | ---- | ---- | ---- | ---- | 
| **LTE** | LTE-FDD B1 | Supported | Not Supported | -107.0/-102.7 | -112.5/-107.5 |  | 
|  | LTE-FDD B2 |  |  | -106.7/-100.3 | -112.5/-107.5 |  | 
|  | LTE-FDD B3 |  |  | -106.8/-99.3 | -113/-107.5 |  | 
|  | LTE-FDD B4 |  |  | -106.9/-102.3 | -112.5/-107.5 |  | 
|  | LTE-FDD B5 |  |  | -107.0/-100.8 | -114/-107.5 |  | 
|  | LTE-FDD B8 |  |  | -107.3/-99.8 | -113/-107.5 |  | 
|  | LTE-FDD B12 |  |  | -107.7/-99.3 | -113.5/-107.5 |  | 
|  | LTE-FDD B13 |  |  | -106.5/-99.3 | -112/-107.5 |  | 
|  | LTE-FDD B18 |  |  | -107.5/-102.3 | -113.5/-107.5 |  | 
|  | LTE-FDD B19 |  |  | -107.1/-102.3 | -114/-107.5 |  | 
|  | LTE-FDD B20 |  |  | -107.2/-99.8 | -114/-107.5 |  | 
|  | LTE-FDD B26 |  |  | TBD/-100.3 | TBD/-107.5 |  | 
|  | LTE-FDD B28 |  |  | -107.2/-100.8 | -113/-107.5 |  | 
|  | LTE-FDD B39 |  |  | TBD /-103 | Not Supported |  | 
| **GSM** | GSM850/<br>EGSM900 | Supported | Not<br><br>Supported |  |  | -109/-102 | 
|  | DCS1800/<br>PCS1900 |  |  |  |  | -108.5/-102 | 


$plugin[{
    "type": "callout",
    "data": {
        "text": "(1) LTE Cat NB1 receiving sensitivity without repetitions.",
        "type": "info",
        "title": "Note"
    }
}]$

### Electrostatic Discharge

The module is not protected against **electrostatics discharge (ESD)** in general.     Consequently, it is subject to ESD handling precautions that typically apply to ESD     sensitive components. Proper ESD handling and packaging procedures must be applied     throughout the processing, handling and operation of any application that incorporates     the module.  

 The following table shows the electrostatic discharge characteristics of RAK8213:

| **Tested Interfaces** | **Contact Discharge** | **Air Discharge** | **Unit** | 
| ---- | ---- | ---- | ---- | 
| 3.3Vaux, GND | ±10 | ±15 | kV | 
| Main/GNSS Antenna <br><br>Interfaces | ±10 | ±15 | kV | 


