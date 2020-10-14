---
type: page
title: Electrical Characteristics
listed: true
slug: electrical-characteristics-rak831
---published

Listed in this document are the different electrical characteristics of RAK831 LPWAN Gateway.

$plugin[{
    "type": "callout",
    "data": {
        "text": "Stress exceeding of one or more of the limiting values listed under \u201cAbsolute Maximum Ratings\u201d may cause permanent damage to the radio module.",
        "type": "warning",
        "title": "Note:"
    }
}]$

## Absolute Maximum Ratings

| **Parameter** | **Condition** | **Min** | **Typ**. | **Max** | **Unit** | 
| ---- | ---- | ---- | ---- | ---- | ---- | 
| Supply Voltage(VDD) |  | -0.3 | 5.0 | 5.5 | V | 
| Operating Temperature |  | -40 |  | +85 | ℃ | 
| RF Iuput Power |  |  |  | -15 | dBm | 


$plugin[{
    "type": "callout",
    "data": {
        "text": "With RF output power level above +15 dBm, a minimum distance to a transmitter should be 1 meter to avoid too large input level.",
        "type": "warning",
        "title": "Note:"
    }
}]$

## Global Electrical Characteristics

| **Parameter** | **Condition** | **Min** | **Typ**. | **Max** | **Unit** | 
| ---- | ---- | ---- | ---- | ---- | ---- | 
| Supply Voltage(VDD) |  | 4.8 | 5.0 | 5.2 | V | 
| Current Consumption | RX Current |  | 100 |  | mA | 
|  | TX Currentz |  | 80 |  | mA | 


At **T=25℃,VDD=5V(Typ.)** if nothing else stated

| **Parameter** | **Condition** | **Min** | **Typ**. | **Max** | **Unit** | 
| ---- | ---- | ---- | ---- | ---- | ---- | 
| Logic low input threshold(VIL) | “0”logic input |  |  | 0.4 | V | 
| Logic high input threshold(VIH) | “1”logic input | 2.9 |  | 3.3 | V | 
| Logic low output level(VOL) | “0”logic output,2mA sink |  |  | 0.4 | V | 
| Logic high output level(VOH) | “1”logic output,2mA source | 2.9 |  | 3.3 | V | 


