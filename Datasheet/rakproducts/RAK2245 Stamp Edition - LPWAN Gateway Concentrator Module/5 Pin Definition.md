---
type: page
title: Pin Definition
listed: true
slug: pin-definition-rak2245-stamp-edition
---published

The pinout diagram for the RAK2245 Stamp Edition - LPWAN Gateway Concentrator Module is shown in figure 1 below.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1565448056\/17454\/fahimiuydovhvpxrmcl9.jpg",
        "mode": "responsive",
        "width": 900,
        "height": 1200,
        "caption": "**Figure 1:** Pinout Diagram of RAK2245 Stamp Edition - LPWAN Gateway Concentrator Module"
    }
}]$

The pin connector of RAK2245 Stamp Edition - LPWAN Gateway Concentrator Module is located at the bottom side. Refer to the table below for the description and numbering of each pins.

| **Pin** | **Name** | **Type** | **Description** | 
| ---- | ---- | ---- | ---- | 
| A1 | GND | GND | GND | 
| A2 | GND | GND | GND | 
| A3 | +5V | POWER | +5V Supply Voltage | 
| A4 | IOREF | POWER | Supply Voltage for Level Translator | 
| A5 | RESET_GPS | Input | GPS Module reset PIN | 
| A6 | STANDBY_GPS | Input | GPS Module standby PIN | 
| A7 | UART_TXD | UART | It should be connected to Main Board's UART_RXD. This pin is connected to GPS Module's UART_TXD internally. | 
| A8 | SPI_MOSI | SPI | It should be connected to Main Board's SPI_MOSI. And this pin has been connected to SX1301's SPI_MOSI internally. | 
| A9 | SPI_CS | SPI | It should be connected to Main Board's SPI_CS. And this pin has been connected to SX1301's SPI_CS internally. | 
| A10 | SPI_MISO | SPI | It should be connected to Main Board's SPI_MISO. And this pin has been connected to SX1301's SPI_MISO internally. | 
| A11 | SPI_CLK | SPI | It should be connected to Main Board's SPI_CLK. And this pin has been connected to SX1301's SPI_CLK internally. | 
| A12 | UART_RXD | UART | It should be connected to Main Board's UART_TXD. This pin is connected to GPS Module's UART_RXD internally. | 
| A13 | RST_BTN_N | RST | SX1301 RESET | 
| A14 | GND | GND | GND | 
| A15 | GND | GND | GND | 
| B1 | GND | GND | GND | 
| B2 | GND | GND | GND | 
| B3 | SDA_GPS | I2C | GPS Module I2C SDA | 
| B4 | SCL_GPS | I2C | GPS Module I2C SCL | 
| B5 | GND | GND | GND | 
| G1 | GND | GND | GND | 
| G2 | GND | GND | GND | 
| G3 | GND | GND | GND | 
| G4 | GND | GND | GND | 
| G5 | GND | GND | GND | 
| G6 | GND | GND | GND | 
| G7 | GND | GND | GND | 
| G8 | GND | GND | GND | 


