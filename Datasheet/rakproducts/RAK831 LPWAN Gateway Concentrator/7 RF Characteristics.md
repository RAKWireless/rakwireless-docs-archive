---
type: page
title: RF Characteristics
listed: false
slug: rf-characteristics-rak831
---published

### Transmitter RF Characteristics

The RAK831 has an excellent transmitter performance . It is highly recommended to use the optimized configuration for the power level configuration, which is part of the HAL. This results in a mean RF output power level and current consumption.

| **PA Control** | **DAC Control** | **MIX Control** | **DIG Gain** | **Nominal RF Power Level [dBm]** | 
| ---- | ---- | ---- | ---- | ---- | 
| 0 | 3 | 8 | 0 | -5 | 
| 0 | 3 | 9 | 0 | -3 | 
| 0 | 3 | 11 | 0 | 0 | 
| 0 | 3 | 15 | 0 | 3 | 
| 1 | 3 | 9 | 0 | 6 | 
| 1 | 3 | 11 | 0 | 10 | 
| 1 | 3 | 12 | 0 | 11 | 
| 2 | 3 | 8 | 0 | 12 | 
| 2 | 3 | 9 | 0 | 13 | 
| 1 | 3 | 15 | 0 | 14 | 
| 2 | 3 | 10 | 0 | 15 | 
| 2 | 3 | 11 | 0 | 16 | 
| 2 | 3 | 11 | 0 | 17 | 
| 2 | 3 | 12 | 0 | 18 | 
| 2 | 3 | 13 | 0 | 19 | 
| 2 | 3 | 14 | 0 | 20 | 


At **T=25℃,VDD=5V(Typ.)** if nothing else stated:

$plugin[{
    "type": "callout",
    "data": {
        "text": "The table below is for 868 MHz RAK831 LPWAN gateway. Other frequencies are also supported such as 433 MHz,470 MHz, and 915 MHz Frequency Range.",
        "type": "info",
        "title": "Note:"
    }
}]$

| **Parameter** | **Condition** | **Min** | **Typ.** | **Max** | **Unit** | 
| ---- | ---- | ---- | ---- | ---- | ---- | 
| Frequency Range |  | 863 |  | 870 | MHz | 
| Modulation Techniques | FSK/LoRaWAN® |  |  |  |  | 
| TX Frequency Variation vs. Temperature | Power Level Setting:20 | -3 |  | +3 | KHz | 
| TX Power Variation vs. Temperature | Power Level Setting:20 | -5 |  | +5 | dB | 
| TX Power Variation |  | -1.5 |  | +1.5 | dB | 


### Receiver RF Characteristics

It is highly recommended to use optimized RSSI calibration values, which is part of the HAL v3.1. For both, Radio 1 and 2, **the RSSI-Offset should be set -169.0**.

The following table gives typically sensitivity level of the RAK831 :

| **Signal Bandwidth/[KHz]** | **Spreading Factor** | **Sensitivity/[dBm]** | 
| ---- | ---- | ---- | 
| 125 | 12 | -137 | 
| 125 | 7 | -126 | 
| 250 | 12 | -136 | 
| 250 | 7 | -123 | 
| 500 | 12 | -134 | 
| 500 | 7 | -120 | 


