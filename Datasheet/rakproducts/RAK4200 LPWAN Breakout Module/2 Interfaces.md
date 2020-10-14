---
type: page
title: Interfaces
listed: true
slug: interfaces-rak4200-breakout
---published

## SWD Programming Interface

When programming via a JLINK tool, it is required to have all of the following 5 pins connected to the JLINK tool: 

1. **3V3**
2. **SWDIO**
3. **SWCLK**
4. **GND**
5. **MCU_NRST**

$plugin[{
    "type": "callout",
    "data": {
        "text": "For the aforementioned reason, it is best you leave these exposed for programming purposes and not to remap them as GPIOs.",
        "type": "info",
        "title": "Note:"
    }
}]$

## UARTinterface

There are two UART interfaces on RAK4200 module: 

- **UART1** – recommended for debugging/firmware update
- **UART2** – recommended for external MCU connection.

## I2C Interface

The following pins are intended for I2C (_require 10k resistance pull-up_):

- **I2C_SCL**
- **I2C_SDA**

## RF interface

J3 is soldered to the antenna connector. Depending on your choice, it can come with either SMA or IPEX style connector. Make sure to select the one you need when ordering. 

## SPI interface

The SPI interface (**_SPI MOSI, SPI MISO, SPI_CLK_**) is connected to **SX1276** internally. 

$plugin[{
    "type": "callout",
    "data": {
        "text": "For the aforementioned reason, it is best you do not use it for external connections.",
        "type": "info",
        "title": "Note:"
    }
}]$

