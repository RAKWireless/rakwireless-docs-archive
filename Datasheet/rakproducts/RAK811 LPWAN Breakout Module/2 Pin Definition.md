---
type: page
title: Pin Definition
listed: true
slug: pin-definition-rak811-lora-breakout-module
---published

The RAK811 supports two different frequency variation: High Radio Frequency and Low Radio frequency.

## High Radio Frequency

The high radio frequency hardware support the regions of EU868, US915, AU915, KR920, AS923, IN865.

### High RF Pin Outline

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1594019247\/21948\/n4ougn6crjbixrpsnzmq.jpg",
        "mode": "600",
        "width": 972,
        "height": 808,
        "caption": "**Figure 1**: Board Pinout for RAK811 Breakout High RF"
    }
}]$

### High RF Pin Definition

| **Pin No.** | **Name** | **Type** | **Description** | 
| ---- | ---- | ---- | ---- | 
| 1 | LoRa 3.3V | P | Main Power Voltage Source Input | 
| 2 | UART1_TXD | O | UART1 Interface | 
| 3 | UART1_RXD | I | UART1 Interface | 
| 4 | PB12 | I/O | ADC_IN18 | 
| 5 | RST | I | Reset Trigger Input, Low Active | 
| 6 | PB3 | I/O | B part for GPIO port | 
| 7 | PB5 | I/O | B part for GPIO port | 
| 8 | PA15 | I/O | A part for GPIO port | 
| 9 | BOOT0 |  | Boot mode GPIO enable pin,high active | 
| 10 | GND |  | Ground connections | 
| 11 | PA0 | O | ADC_IN0 | 
| 12 | PA1 | I | ADC_IN1 | 
| 13 | SWCLK |  | Serial Wire Debug Pin | 
| 14 | SWDIO |  | Serial Wire Debug Pin | 
| 15 | PB4 | I | B part for GPIO port | 
| 16 | PB15 | I/O | ADC_IN21 | 
| 17 | PA2 | I/O | ADC_IN2 | 
| 18 | PA8 | I/O | A part for GPIO port | 
| 19 | PA12 | O | A part for GPIO port | 
| 20 | PB14 | I/O | ADC_IN20 | 


## Low Radio Frequency

The Low radio frequency is applicable to bandwidth of regions EU433 and CN470.

### Low RF Pin Outline

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1594020067\/21948\/ezhliqimq3iksrm0nuhp.png",
        "mode": "600",
        "width": 1245,
        "height": 1277,
        "caption": "**Figure 2**: Board Pinout for RAK811 Breakout Low RF"
    }
}]$

### Low RF Pin Definition

| **Pin No.** | **Name** | **Type** | **Description** | 
| ---- | ---- | ---- | ---- | 
| 1 | LoRa 3.3V | P | Main Power Voltage Source Input | 
| 2 | UART1_TXD | O | UART1 Interface | 
| 3 | UART1_RXD | I | UART1 Interface | 
| 4 | PB12 | I/O | ADC_IN18 | 
| 5 | RST | I | Reset Trigger Input, Low Active | 
| 6 | PA3 | I/O | A part for GPIO port | 
| 7 | PB5 | I/O | B part for GPIO port | 
| 8 | PA12 | I/O | A part for GPIO port | 
| 9 | PB4 |  | Boot mode GPIO enable pin,high active | 
| 10 | GND |  | Ground connections | 
| 11 | PA0 | O | ADC_IN0 | 
| 12 | PA1 | I | ADC_IN1 | 
| 13 | SWCLK |  | Serial Wire Debug Pin | 
| 14 | SWDIO |  | Serial Wire Debug Pin | 
| 15 | PA11 | I | A part for GPIO port | 
| 16 | PB15 | I/O | ADC_IN21 | 
| 17 | PA2 | I/O | ADC_IN2 | 
| 18 | PB13 | I/O | A part for GPIO port | 
| 19 | PA12 | O | A part for GPIO port | 
| 20 | PB14 | I/O | ADC_IN20 | 


