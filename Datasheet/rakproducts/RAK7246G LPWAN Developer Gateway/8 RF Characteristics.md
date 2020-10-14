---
type: page
title: RF Characteristics
listed: false
slug: rf-characteristics-rak7246g
---published

### Transmitter RF Characteristics

The RAK2246 has an excellent transmitter performance. It is highly recommended, to use an optimized configuration for the power level configuration, which is part of the HAL. This results in a mean RF output power level and current consumption:

| **MIX Control** | **DIG Gain** | **Nominal RF Power Level [dBm]** | 
| ---- | ---- | ---- | 
| 8 | 0 | 10 | 
| 9 | 0 | 12 | 
| 10 | 0 | 14 | 
| 11 | 0 | 16 | 
| 12 | 0 | 18 | 
| 13 | 0 | 19 | 
| 14 | 0 | 20 | 
| 15 | 0 | 21 | 


**T=25°C, VDD=5V (Typ.) if nothing else stated**

| **Parameter** | **Condition** | **Min** | **Typ.** | **Max** | **Unit** | 
| ---- | ---- | ---- | ---- | ---- | ---- | 
| Frequency Range |  | 863 |  | 870 | MHz | 
| Modulation Techniques | FSK/LoRa® |  |  |  |  | 
| TX Frequency Variation vs. Temperature | Power Level Setting: 20dBm | -3 |  | +3 | KHz | 
| [TX Power Variation](TX Power Variation)<br> vs. Temperature |  | -5 |  | +5 | dB | 
| TX Power Variation |  | -1.5 |  | +1.5 | dB | 


$plugin[{
    "type": "callout",
    "data": {
        "text": "Also supports 915 Frequency Range.",
        "type": "info",
        "title": "Note"
    }
}]$

### Receiver RF Characteristics

It is highly recommended, to use optimized RSSI calibration values, which is part of the HAL v3.1. For both, Radio 1 and Radio 2, the RSSI-Offset should be set to -169.0. (It is highly recommended, to use optimized RSSI calibration values, which is part of the HAL v3.1. For both, Radio 1 and Radio 2, the RSSI-Offset should be set to -169.0. )

The following table gives typically sensitivity level of the RAK2246:

| **Signal Bandwidth [KHz]** | **Spreading Factor** | **Sensitivity [dBm]** | 
| ---- | ---- | ---- | 
| 125 | 12 | -141 | 
| 125 | 7 | -128 | 
| 250 | 12 | -137 | 
| 250 | 7 | -124 | 
| 500 | 12 | -135 | 
| 500 | 7 | -121 | 


### RF Key Components

This section introduces the key components in the RAK2246 in order to help developers to utilize the system at its fullest in their designs.

**1. DC-DC regulator**

The system power supply is provided by an external 5V DC power supply. All the key components and related clock crystals are powered by two DC-DC regulators (MP1496) which output 1.8V and 3.3V in order to meet the normal working conditions. The MP1496 is a high-frequency, synchronous, rectified, step-down, switch-mode converter with built-in power MOSFETs. It offers a very compact solution to achieve a 2A continuous output current with excellent load and line regulation over a wide input supply range.

**2. FEM**

The FEM chosen is a SKYWORKS SKY66422, which integrates a PA, LNA and a Switch. It can achieve a 20 dBm max output power in order to deliver sufficient RX performance. The frequency range it can cover from is 860MHZ~930MHz.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1582526766\/26044\/qbxfrqry28q2p8ozhicz.jpg",
        "mode": "responsive",
        "width": 626,
        "height": 477,
        "caption": "**Figure 1:** System Architecture"
    }
}]$

