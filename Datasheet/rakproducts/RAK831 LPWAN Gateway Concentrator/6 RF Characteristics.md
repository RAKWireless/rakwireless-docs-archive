---
type: page
title: RF Characteristics
listed: true
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


### RF Key Components

This section introduces the key components in RAK831 and helps the developer to utilize the system to realize its system-level design.

**1.LDO**

The system power supply is provided by the external **5V DC power supply**. The SX1301 and related clock crystal are powered by dual output LDO transformer outputs **1.8V** and **3.3V** in order to meet the normal working condition of SX1301. Other key components are powered by LDO transformer output 3.3V.

To be aware of the system design of LDO's power supply enable is provided by the output GPIO of SX1301 as default. The connection method of pin enable should be kept the same as the Semtech official code. At the same time, system design also needs to keep flexibility and all LDO enable should be connected to **pin DB24**. In this case, users can run the official reference code on this board, and also can change all external enable clock as they need to achieve the flexibility debugging.

**2.Power Amplifier**

The Power amplifier chooses **RFMD LF Power Amplifier** and built-in two steps gain with a maximum power output of **0.5W**.The frequency range can cover from **380MHZ~960MHz**. The two steps gain control table as:

| **Parameter** | **Minimum** | **Typical** | **Maximum** | **Unit** | **Condition** | 
| ---- | ---- | ---- | ---- | ---- | ---- | 
| Overall |  |  |  |  | T=25°C, VCC=3.6V, VPD=Vbias=3.0V, Pin=0dBm, f=915 MHz | 
| CW Output Power |  | 27.5 |  | dBm | VCC=3.6V | 
| CW Output Power |  | 30 |  | dBm | VCC=5V | 
| Small Signal Gain |  | 32 |  | dB | Pin=10dBm | 
| Second Harmonic |  | 23 |  | dBc | Without external second harmonic trap | 
| Third Harmonic |  | 45 |  | dBc |  | 
| CW Efficiency | 55 | 63 |  | % | G16="high", G8="high", Pin=0dBm | 
| Power Down "ON" |  | 3.0 |  | V | Voltage supplied to the input. | 
| Power Down "Off" | 0 | 0.5 | 0.8 | V | Voltage supplied to the input. | 
| VPD Input Current |  | 6 |  | mA | Only in "ON" state. | 
| G16, G8 "ON" | 1.7 |  | 3.0 | V | Voltage supplied to the input. | 
| G16, G8 "OFF" | 0 |  | 0.7 | V | Voltage suppled to the input. | 
| G16, G8 Input Current |  | 1.0 |  | mA | Only in "ON" state. | 
| Output Power | 26.5 | 27.5 | 29 | dBm | G16="high", G8="high", Pin=0dBm | 
|  | 21 | 23 | 25 | dBm | G16="high", G8="low", Pin=0dBm | 
|  | 14 | 16 | 28 | dBm | G16="low", G8="high", Pin=0dBm | 
|  | 3 | 5 | 8 | dBm | G16="low", G8="low", Pin=0dBm | 
| Turn On/Off Time |  | 200 |  | ns |  | 


**3.RF Switch**

The RF switch chooses the **RFSW1012** that has high isolation and low insertion loss. This chip handles the switch between Tx and Rx. The Control logic as shown in figure 1 below shows that the pin of CTRL was controlled by SX1301’s GPIO through the output signal of **LNA___EN_A**, the Pin of EN was controlled by SX1301’s GPIO through output signal of **RADIO_EN_A**. Simultaneously, it also can be controlled by the external input signal through **DB24**.

| **State** | **VDD** | **CTRL** | **EN** | **RF Path** | 
| ---- | ---- | ---- | ---- | ---- | 
| 1 | 2.7V to 4.6V | High Voltage | High Voltage | ANT-RF2 | 
| 2 | 2.7V to 4.6V | Low Voltage | High Voltage | ANT-RF1 | 
| Shutdown | 2.7V to 4.6V | Don't Care | Low Voltage | Shutdown | 


$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1593597970\/31338\/ovnhzwst8hd9fuhkqssa.jpg",
        "mode": "responsive",
        "width": 776,
        "height": 529,
        "caption": "**Figure 1:** RAK831 Control Logic"
    }
}]$

