---
type: page
title: RF Characteristics
listed: true
slug: rf-characteristics-rak7244
---published

### Operating Frequencies

All models of the Developer Gateway support all the LoRaWAN® bands.

| **Region** | **Frequency (MHz)** | 
| ---- | ---- | 
| Europe | EU433, EU868 | 
| China | CN470 | 
| Russia | RU864 | 
| India | IN865 | 
| North America | US915 | 
| Australia | AU915 | 
| Korea | KR920 | 
| Asia | AS923 | 


### LoRa® RF Characteristics

### Transmitter RF Characteristics

The RAK2245 has an excellent transmitter performance. It is highly recommended to use an optimized configuration for the power level configuration, which is part of the HAL. These results are in a mean RF output power level and current consumption.

| **PA Control** | **DAC Control** | **MIX Control** | **DIG Gain** | **Nominal RF Power Level (dBm)** | 
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


T = 25℃ at VDD = 5V (Typ.) as default if nothing else stated.

| **Parameter** | **Condition** | **Min** | **Typ.** | **Max** | 
| ---- | ---- | ---- | ---- | ---- | 
| **Frequency Range** |  | 863 Mhz |  | 870 Mhz | 
| **Modulation Techniques** | FSK/LoRaTM |  |  |  | 
| **TX Frequency Variation<br>vs. Temperature** | Power Level Setting : 20 | -3 Khz |  | +3 Khz | 
| **TX Power Variation<br>vs. Temperature** | Power Level Setting : 20 | -5 dBm |  | +5 dBm | 
| **TX Power Variation** |  | -1.5 dBm |  | +1.5 dBm | 


## Receiver RF Characteristics

It is highly recommended to use optimized RSSI calibration values, which is part of the HAL v3.1. For both, Radio 1 and 2, the RSSI-Offset should be set to -169.0. The following table gives typically the sensitivity level of the RAK2245.

| **Signal Bandwidtth (Khz)** | **Spreading Factor** | **Sensitivity (dBm)** | 
| ---- | ---- | ---- | 
| 125 | 12 | -139 | 
| 125 | 7 | -126 | 
| 250 | 12 | -136 | 
| 250 | 7 | -123 | 
| 500 | 12 | -134 | 
| 500 | 7 | -120 | 


### Cellular Frequency Bands

The Quectel EG95 is part of the LTE CAT4 module series that are specially optimized for Machine to Machine (M2M) and Internet of Things (IoT) applications. Adopted from 3GPP Rel. 11 LTE technology, which delivers data rates of 150Mbps downlink and 50Mbps uplink.

| **Frequency** | **EG95-E** | **EG95-NA** | 
| ---- | ---- | ---- | 
| **LTE FDD** | B1 / B3 / B7 / B8 / B20 / B28A | B2 / B4 / B5 / B12 / B13 | 
| **WCDMA** | B1 / B8 | B2 / B4 / B5 | 
| **GSM / EDGE** | 900 / 1800 MHz |  | 
| **Region** | Europe | North America | 


