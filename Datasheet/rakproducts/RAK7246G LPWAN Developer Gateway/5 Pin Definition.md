---
type: page
title: Pin Definition
listed: true
slug: pin-definition-rak7246g
---published

The table below shows the pin number of RAK2246 Pi HAT and its corresponding name and description. Refer to figure 1 for the pinout diagram. 

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1590742973\/26040\/cazocgarxqpwr2iowjzz.jpg",
        "mode": "600",
        "width": 1799,
        "height": 1760,
        "caption": "**Figure 1:** RAK7246G Pinout Diagram"
    }
}]$

| **Pin** | **Name** | **Description** | 
| ---- | ---- | ---- | 
| 1 | NC | Not Connected | 
| 2 | +5V | +5V Supply Voltage | 
| 3 | SDA | I2C_SDA (Connected to GPS Module I2C_SDA) | 
| 4 | +5V | +5V Supply Voltage | 
| 5 | SCL | I2C_SCL (Connected to GPS Module I2C_SCL) | 
| 6 | GND | Ground | 
| 7 | NC | Not Connected | 
| 8 | UART_TX | It should be connected to the RPi’s UART_TXD. It has been connected to<br>the GPS Module’s UART_RXD internally. | 
| 9 | GND | Ground | 
| 10 | UART_RX | It should be connected to the RPi’s UART_RXD. It has been connected to<br>the GPS Module’s UART_TXD internally. | 
| 11 | RESET | SX1308 RESET (GPIO17 of RPi) | 
| 12 | NC | Not Connected | 
| 13 | NC | Not Connected | 
| 14 | GND | Ground | 
| 15 | NC | Not Connected | 
| 16 | NC | Not Connected | 
| 17 | NC | Not Connected | 
| 18 | NC | Not Connected | 
| 19 | SPI_MOSI | It should be connected to the RPi’s SPI_MOSI. It has been connected to the SX1308’s SPI_MOSI internally. | 
| 20 | GND | Ground | 
| 21 | SPI_MISO | It should be connected to the RPi’s SPI_MISO. It has been connected to the SX1308’s SPI_MISO internally | 
| 22 | NC | Not Connected | 
| 23 | SPI_SCLK | It should be connected to the RPi’s SPI_SCLK.<br>It has been connected to the SX1308’s SPI_CLK internally. | 
| 24 | SPI_CE0 | It should be connected to the RPi’s SPI_CE0. It has been<br>connected to the SX1308’s SPI_CS internally. | 
| 25 | GND | Ground | 
| 26 | NC | Not Connected | 
| 27 | ID_SD | I2C_SDA for HAT ID EEPROM | 
| 28 | ID_SC | I2C_SCL for HAT ID EEPROM | 
| 29 | NC | Not Connected | 
| 30 | NC | Not Connected | 
| 31 | NC | Not Connected | 
| 32 | NC | Not Connected | 
| 33 | RESET_GPS | GPS Module reset PIN (GPIO13 of RPi) | 
| 34 | GND | Ground | 
| 35 | STANDBY_GPS | GPS Module standby PIN (GPIO19 of RPi) | 
| 36 | NC | Not Connected | 
| 37 | NC | Not Connected | 
| 38 | NC | Not Connected | 
| 39 | GND | Ground | 
| 40 | NC | Not Connected | 


