---
type: page
title: RF Characteristics
listed: true
slug: rf-characteristics-rak2245-stamp-edition
---published

### Operating Frequencies

The board supports the following LoRaWAN® frequency channels shown in the table below. The frequency parameter is easy to configure as you go through the device configuration setup.

|  |  | 
| ---- | ---- | 
| Europe | EU433, EU868 | 
| China | CN470 | 
| North America | US915 | 
| Asia | AS923, AS920 | 
| Australia | AU915 | 
| Korea | KR920 | 
| India | IN865 | 


### Transmitter RF Characteristics

The RAK2245 Stamp Edition - LPWAN Gateway Concentrator Module has an excellent transmitter performance. It is highly
recommended to use an optimized configuration for the power level
configuration, which is part of the HAL. This results in a mean RF output power
level and current consumption.

| **PA Control** | **DAC Control** | **MIX Control** | **DIG Gain** | **Normal RF Power Level (dBm)** | 
| ---- | ---- | ---- | ---- | ---- | 
| 0 | 3 | 8 | 0 | -6 | 
| 0 | 3 | 10 | 0 | -3 | 
| 0 | 3 | 14 | 0 | 0 | 
| 1 | 3 | 9 | 3 | 4 | 
| 1 | 3 | 8 | 0 | 8 | 
| 1 | 3 | 9 | 0 | 10 | 
| 1 | 3 | 11 | 0 | 12 | 
| 1 | 3 | 12 | 0 | 14 | 
| 1 | 3 | 13 | 0 | 16 | 
| 2 | 3 | 12 | 0 | 17 | 
| 2 | 3 | 13 | 0 | 19 | 
| 2 | 3 | 14 | 0 | 20 | 
| 3 | 3 | 10 | 0 | 0 | 
| 3 | 3 | 11 | 0 | 0 | 
| 3 | 3 | 12 | 0 | 25 | 
| 3 | 3 | 13 | 0 | 26 | 
| 3 | 3 | 14 | 0 | 27 | 


- At T=25°C, Vdd = 5V (Typical) if nothing else stated

| **Parameter** | **Condition** | **Min** | **Typical** | **Max** | 
| ---- | ---- | ---- | ---- | ---- | 
| Frequency Range |  | 863 MHz |  | 870 MHz | 
| Modulation Techniques | FSK/LoRa® |  |  |  | 
| TX Frequency Variation vs Temperature | Power Level Setting: 20 | -3 Khz |  | +3 Khz | 
| TX Power Variation vs. Temperature |  | -5 dBm |  | +5 dBm | 
| TX Power Variation |  | -1.5 dBm |  | +1.5 dBm | 


### Receiver RF Characteristics

It is recommended to use optimized RSSI calibration values which is part of HAL v3.1. For both Radio 1 and 2, the RSSI-offset should be set to -169. The following table shows typical sensitivity level of RAK2245 Stamp Edition -LPWAN Gateway Concentrator Module.

| **Signal Bandwidth (KHz)** | **Spreading Factor** | **Sensitivity (dBm)** | 
| ---- | ---- | ---- | 
| 125 | 12 | -139 | 
| 125 | 7 | -126 | 
| 250 | 12 | -136 | 
| 250 | 7 | -123 | 
| 500 | 12 | -134 | 
| 500 | 7 | -120 | 


