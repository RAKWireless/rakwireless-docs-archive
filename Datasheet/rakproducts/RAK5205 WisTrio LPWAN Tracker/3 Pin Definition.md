---
type: page
title: Pin Definition
listed: true
slug: pin-definition---rak5205
---published

Here are the six connectors for RAK5205 tracker board: P1, P2, J11, J12, J22 and J25

### P1

(Pin1 connected to VBATT, Pin2 connected to GND) Li-ion battery connector.

### P2

(Pin1 connected to VBUS, Pin2 connected to GND) Solar cell interface.

### J11

Pin1 is connected to VBUS. Pin2 is connected to VBIN. Without a battery
connection, the J11 needs to be short-circuited with a jumper. Instead, the J11
needs to be kept open.

### J12

Pin1 is connected to BOOT0. Pin2 is connected to VDD. Enter flash mode through jumper short circuit and open into normal mode.

### J22

30pins, follow the 96Board’s pin definition.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1590755768\/17641\/lb4pw2ktrm4n0qijmc8y.jpg",
        "mode": "responsive",
        "width": 2000,
        "height": 2000,
        "caption": "**Figure 1:** RAK5205 Pinout Diagram"
    }
}]$

| **Pin** | **Pin Name** | **Description** | 
| ---- | ---- | ---- | 
| 1 | NC | No Connection | 
| 2 | NC | No Connection | 
| 3 | UART1_TX | UART1_TX | 
| 4 | NC | No Connection | 
| 5 | UART1_RX1 | UART1_RX1 (need to connect RX pin and RX1 pin of J25 via jumper if user wants to use this UART interface). | 
| 6 | NC | No Connection | 
| 7 | NC | No Connection | 
| 8 | NC | No Connection | 
| 9 | GND | Ground | 
| 10 | GND | Ground | 
| 11 | VCCIN | 5V out | 
| 12 | VCC_3V3 | 3.3V out | 
| 13 | PA8 | GPIO Pin | 
| 14 | PB3 | GPIO Pin | 
| 15 | NC | No Connection | 
| 16 | PB5 | GPIO Pin | 
| 17 | SWD_TMS | GPIO Pin / R21, R22 pull-up 10K resistor can be used as JTAG interface | 
| 18 | SWD_CLK | GPIO Pin / R21, R22 pull-up 10K resistor can be used as JTAG interface | 
| 19 | LED1_PA12 | GPIO Pin | 
| 20 | LED2_PB4 | GPIO Pin | 
| 21 | NC | No Connection | 
| 22 | SCL | I²C | 
| 23 | NC | No Connection | 
| 24 | SDA | I²C | 
| 25 | NC | No Connection | 
| 26 | PB12 | ADC Interface | 
| 27 | NC | No Connection | 
| 28 | NC | No Connection | 
| 29 | RST | Reset Pin | 
| 30 | NC | No Connection | 


### J25

(RX1, RX, RXCP) J22 and USB UART share. If you use the UART of J22, you need to connect Rx and RX1 pins. If you use USB UART, you need to connect Rx and RXCP pins.

