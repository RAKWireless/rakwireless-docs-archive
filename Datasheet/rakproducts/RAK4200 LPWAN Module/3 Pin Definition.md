---
type: page
title: Pin Definition
listed: true
slug: pin-definition---rak4200-lora-module
---published

Provided in this section is the Pinout of the RAK4200 LPWAN Module.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1590756577\/23171\/n92zecegauqcywvwh0to.jpg",
        "mode": "responsive",
        "width": 2519,
        "height": 1910,
        "caption": "**Figure 1**: Pinout of RAK4200"
    }
}]$

| **Pin** | **Name** | **I/O** | **Description** | 
| ---- | ---- | ---- | ---- | 
| 1 | UART2_RX | I | Main UART (STM32L071K8 PA3) | 
| 2 | UART2_TX | O | Main UART (STM32L071K8 PA2) | 
| 3 | UART2_DE | I/O | GPIO (STM32L071K8 PA1) | 
| 4 | UART1_TX | I/O | GPIO or UART(Reserved) (STM32L051K8 PA9) | 
| 5 | UART1_RX | I/O | GPIO or UART(Reserved)  (STM32L051K8 PA10) | 
| 6 | UART1_DE | I/O | GPIO or UART(Reserved) (STM32L051K8 PA12) | 
| 7 | SWDIO | I/O | Programming (STM32L051K8 PA13) | 
| 8 | SWCLK | I/O | Programming (STM32L051K8 PA14) | 
| 9 | I2C_SCL | I/O | I2C interface (STM32L051K8 PB6) | 
| 10 | I2C_SDA | I/O | I2C interface (STM32L051K8 PB7) | 
| 11 | GND |  | Ground | 
| 12 | RF | I/O | RF port (Reserved), default RF out by IPEX | 
| 13 | GND |  | Ground | 
| 14 | GND |  | Ground | 
| 15 | SPI_CLK | I/O | Reserved PA5 | 
| 16 | SPI_MISO | I/O | Reserved PA6 | 
| 17 | SPI_MOSI | I/O | Reserved PA7 | 
| 18 | MCU_NRST | I/O | MCU reset (STM32L051K8 NRST) | 
| 19 | GND |  | Ground | 
| 20 | VDD |  | DC3V3 | 


