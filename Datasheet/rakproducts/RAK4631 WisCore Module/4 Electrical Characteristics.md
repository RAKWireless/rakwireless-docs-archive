---
type: page
title: Electrical Characteristics
listed: true
slug: electrical-characteristics-rak4631
---published

### Power Consumption

| **Item** | **Power Consumption** | **Condition** | 
| ---- | ---- | ---- | 
| Tx mode LoRa @20dBm | 125mA | LoRa @ PA_BOOST&BT sleep | 
| Tx mode LoRa @17dBm | 92mA | LoRa @ PA_BOOST&BT sleep | 
| Tx mode BT@4dBm | 9mA | BT Tx mode & Lora sleep | 
| Rx mode LoRa @37.5Kbps | 17mA | LoRa @ Receive mode &BT sleep | 
| Rx mode BT@2Mbps | 11.5mA | BT Rx mode & Lora sleep | 
| Sleep mode | 2.0uA | LoRa&BT sleep | 


### Absolute Maximum Ratings

| **Symbol** | **Description** | **Min.** | **Nom.** | **Max.** | **Unit** | 
| ---- | ---- | ---- | ---- | ---- | ---- | 
| VBAT_SX | LoRa chip supply voltage | -0.5 |  | 3.9 | V | 
| VBAT_SX_IO | LoRa chip supply for I/O pins | -0.5 |  | 3.9 | V | 
| VDD_NRF | MCU power supply | -0.3 |  | 3.9 | V | 
| VBUS | USB supply voltage | -0.3 |  | 5.8 | V | 
| VBAT_NRF | MCU high voltage power supply | -0.3 |  | 5.8 | V | 


### Recommended Operating Conditions

| **Symbol** | **Description** | **Min.** | **Nom.** | **Max.** | **Unit** | 
| ---- | ---- | ---- | ---- | ---- | ---- | 
| VBAT_SX | SX1262 supply voltage | 2.0 | 3.3 | 3.7 | V | 
| VBAT_SX___IO | SX1262 supply for I/O pins | 2.0 | 3.3 | 3.7 | V | 
| VDD_NRF | NRF52840 power supply | 2.0 | 3.3 | 3.6 | V | 
| VBUS | VBUS USB supply voltage | 4.35 | 5.0 | 5.5 | V | 
| VBAT_NRF | NRF52840 high voltage power supply | 2.5 |  | 5.5 | V | 


