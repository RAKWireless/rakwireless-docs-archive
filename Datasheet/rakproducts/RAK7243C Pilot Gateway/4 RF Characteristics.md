---
type: page
title: RF Characteristics
listed: true
slug: rf-characteristics-rak7243c
---published

### Operating Frequencies

The Pilot Gateway supports all LoRaWAN® frequency channels as below. Which is easy to configure while building the firmware from the source code.

| **Region** | **Frequency (MHz)** | 
| ---- | ---- | 
| Europe | EU433, EU868 | 
| China | CN470 | 
| North America | US915 | 
| Asia | AS923, AS920 | 
| Australia | AU915 | 
| Korea | KR920 | 
| India | IN865 | 


### LoRa® RF Characteristics

### Transmitter RF Characteristics

The RAK2245 has an excellent transmitter performance. It is highly
recommended to use an optimized configuration for the power level
configuration, which is part of the HAL. This results in a mean RF output power
level and current consumption

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


- T=25℃, VDD=5V(Typ.) if nothing else stated.

| **Parameter** | **Condition** | **Min** | **Typ.** | **Max** | 
| ---- | ---- | ---- | ---- | ---- | 
| **Frequency Range** |  | 863 Mhz |  | 870 Mhz | 
| **Modulation Techniques** | FSK/LoRa™ |  |  |  | 
| **TX Frequency Variation <br>vs. Temperature** | Power Level<br>Setting : 20 | -3 Khz |  | +3 Khz | 
| **TX Power Variation <br>vs. Temperature** | Power Level<br>Setting : 20 | -5 dBm |  | +5 dBm | 
| **TX Power Variation** |  | -1.5 dBm |  | +1.5 dBm | 


### Receiver RF Characteristics

It is highly recommended, to use optimized RSSI calibration values, which is
part of the HAL v3.1. For both, Radio 1 and 2, the RSSI-Offset should be set - 169.0. The following table gives typically sensitivity level of the RAK2245.

| **Signal Bandwidtth (Khz)** | **Spreading Factor** | **Sensitivity (dBm)** | 
| ---- | ---- | ---- | 
| 125 | 12 | -139 | 
| 125 | 7 | -126 | 
| 250 | 12 | -136 | 
| 250 | 7 | -123 | 
| 500 | 12 | -134 | 
| 500 | 7 | -120 | 


### Cellular Frequency

The Pilot Gateway supports different frequency bands according to the modular mounted on the board.

### BG96 Module

BG96 is a series of LTE Cat M1/Cat NB1/EGPRS module offering a maximum data rate of 300Kbps downlink and 375Kbps uplink.

| **Frequency** | **BG96** | 
| ---- | ---- | 
| **LTE (FDD-LTE)** | B1 / B2 / B3 / B4 / B5 / B8 / B12 / B13 / B18 / B19 / B20 / B26 / B28 | 
| **LTE (TDD-LTE)** | B39 (for CAT M1 only) | 
| **EGPRS** | 850 / 900 / 1800 / 1900 MHz | 


### EG91 Module

Quectel EG91 is a series of LTE category 1 module optimized specially for M2M and IoT applications. It delivers M2M-optimized speeds of 10Mbps downlink and 5Mbps uplink. These make EG91 an ideal solution for numerous IoT applications that are not reliant on high-speed connectivity but still require the longevity and reliability of LTE networks.

| **Frequency** | **EG91-E** | **EG91-NA** | 
| ---- | ---- | ---- | 
| **LTE FDD** | B1 / B3 / B7 / B8 / B20 / B28A | B2 / B4 / B5 / B12 / B13 | 
| **WCDMA** | B1 / B8 | B2 / B4 / B5 | 
| **GSM /EDGE** | 900 / 1800 MHz |  | 
| **Region** | Europe | North America | 


### EG95 Module

Quectel EG95 is a series of LTE category 4 module optimized specially for M2M and IoT applications. Adopting 3GPP Rel. 11 LTE technology, it delivers 150Mbps downlink and 50Mbps uplink data rates.

| **Frequency** | **EG95-E** | **EG95-NA** | 
| ---- | ---- | ---- | 
| **LTE FDD** | B1 / B3 / B7 / B8 / B20 / B28A | B2 / B4 / B5 / B12 / B13 | 
| **WCDMA** | B1 / B8 | B2 / B4 / B5 | 
| **GSM / EDGE** | 900 / 1800 MHz |  | 
| **Region** | Europe | North America | 


