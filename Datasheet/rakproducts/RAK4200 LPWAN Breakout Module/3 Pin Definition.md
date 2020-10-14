---
type: page
title: Pin Definition
listed: true
slug: pin-definition-rak4200-breakout
---published

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1586922699\/27909\/blxaquvtuajwaylukmhs.png",
        "mode": "600",
        "width": 6704,
        "height": 7284,
        "caption": "**Figure 1**. RAK4200 Breakout Module Pinout"
    }
}]$

## J1 Pin Definitions

| **Pin** | **Name** | **I/O** | **Description** | **Alternate functions** | 
| ---- | ---- | ---- | ---- | ---- | 
| 1 | UART2_RX | I | Main<br>UART (STM32L071 PA3) | USART1_RX,<br>I2C1_ SDA | 
| 2 | UART2_TX | O | Main<br>UART (STM32L071 PA2) | MCO,<br>USART1_TX, I2C1_ SCL, I2C3_SMBA | 
| 3 | UART2_DE | I/O | GPIO<br>(STM32L071 PA1) | SPI1_MOSI,<br>EVENT OUT, USART1_ RTS_DE, COMP2_OUT | 
| 4 | UART1_DE | I/O | GPIO<br>or UART (Reserved)<br>GPIO<br>or UART (Reserved) | EVENT<br>OUT, TIM2_CH2<br><br>USART2_RTS_DE, TIM21_ETR,<br> USART4_RX, COMP1_INP, ADC_IN1 | 
| 5 | SWDIO | I/O | Programming<br>(STM32L071 PA13) | SWDIO,<br>LPUART1_RX | 
| 6 | SWCLK | I/O | Programming<br>(STM32L071 PA14) | SWCLK,<br>USART2_TX, LPUART1_ TX | 
| 7 | I2C_SCL | I/O | I2C<br>interface (STM32L071 PB6) | USART1_TX,<br>I2C1_ SCL, LPTIM1_ETR, COMP2_INP | 
| 8 | I2C_SDA | I/O | I2C<br>interface (STM32L071 PB6) | USART1_RX,<br>I2C1_ SDA, LPTIM1_IN2, USART4_CTS, COMP2_INP, VREF_PVD_IN | 


## J2 Pin Definitions

| **Pin** | **Name** | **I/O** | **Description** | **Alternate Functions** | 
| ---- | ---- | ---- | ---- | ---- | 
| 1 | VDD |  | DC3V3 | Supply<br>voltage 2.0~3.3V | 
| 2 | UART1_TX | I/O | GPIO<br>or UART (Reserved) (STM32L071 PA9) | TIM21_CH1, TIM2_CH3, USART2_TX, LPUART1_TX, COMP2_OUT, COMP2_INM,<br> ADC_IN2 | 
| 3 | UART1_RX | I/O | GPIO<br>or UART (Reserved) (STM32L071 PA10) | TIM21_CH2,<br>TIM2_ CH4, USART2_RX, LPUART1_RX, COMP2_INP, ADC_IN3 | 
| 4 | GND |  | Ground |  | 
| 5 | MCU_NRST | I/O | MCU<br>reset (STM32L071 NRST) |  | 
| 6 | SPI_CLK | I/O | Reserved<br>PA5 | Internal<br>connection to **SX1276 SPI_CLK** | 
| 7 | SPI_MISO | I/O | Reserved<br>PA6 | Internal<br>connection to **SX1276 SPI_MISO** | 
| 8 | SPI_MISO | I/O | Reserved<br>PA7 | Internal<br>connection to **SX1276 SPI_MOSI** | 


## J4 Pin Definitions

| **Pin** | **Name** | **I/O** | **Description** | **Alternate Functions** | 
| ---- | ---- | ---- | ---- | ---- | 
| 1 | VDD |  | DC3V3 | Supply<br>voltage 2.0~3.3V | 
| 2 | GND |  | Ground |  | 


