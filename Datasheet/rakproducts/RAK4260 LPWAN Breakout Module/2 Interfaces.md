---
type: page
title: Interfaces
listed: true
slug: interfaces-rak4260-breakout
---published

### SWD Programming Interface

When programming via a JLINK tool, it is required to have all of the following 5 pins connected to your JLINK tool:

1. **3V3**
2. **SWDIO**
3. **SWCLK**
4. **GND**
5. **RST**

$plugin[{
    "type": "callout",
    "data": {
        "text": "For the aforementioned reason, it is best you leave these exposed for programming purposes and not to remap them as GPIOs.",
        "type": "info",
        "title": "Note:"
    }
}]$

### UART Interface

There are two UART interfaces on RAK4200 module:

- **UART1** – default interface
- **UART3** – reserved, can also act as GPIOs.

### I2C Interface

I2C_SCL and I2C_SDA are connected to the ATECC608A crypto chip for the purpose of developing cryptographic applications: network end-point key management and exchange small message and PII data encryption, secure boot and protected download, ecosystem control and anti-cloning.

### RF Interface

J4 is soldered to the antenna connector. Depending on your choice it can come with either SMA or IPEX style connector. Make sure to select the one you need when ordering.

