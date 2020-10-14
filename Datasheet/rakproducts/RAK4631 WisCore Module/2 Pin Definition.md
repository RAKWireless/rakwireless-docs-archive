---
type: page
title: Pin Definition
listed: true
slug: pin-definition-rak4631
---published

### WisConnector Pin Definition

The breakout module allows the RAK4630 stamp module’s pinout to be transferred to board-to-board connector, the Figure 1 shows the definition of this connector.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1594958923\/32151\/euirf6sitcwrkxgqjfsm.jpg",
        "mode": "responsive",
        "width": 420,
        "height": 564,
        "caption": "**Figure 1**: WisConnector pin defintion"
    }
}]$

| **Pin No.** | **Name** | 
| ---- | ---- | 
| 1 | VBAT_1 | 
| 2 | VBAT | 
| 3 | GND1 | 
| 4 | GND2 | 
| 5 | 3V3_1 | 
| 6 | 3V3_2 | 
| 7 | USB+ | 
| 8 | USB- | 
| 9 | VBUS | 
| 10 | SW1 | 
| 11 | TXD0 | 
| 12 | RXD0 | 
| 13 | RESET | 
| 14 | LED1 | 
| 15 | LED2 | 
| 16 | LED3 | 
| 17 | VDD_1 | 
| 18 | VDD_2 | 
| 19 | I2C1_SDA | 
| 20 | I2C1_SCL | 
| 21 | AIN0 | 
| 22 | AIN1 | 
| 23 | BOOT0 | 
| 24 | NC | 
| 25 | SPI_CS | 
| 26 | SPI_CLK | 
| 27 | SPI_MISO | 
| 28 | SPI_MOSI | 
| 29 | IO1 | 
| 30 | IO2 | 
| 31 | IO3 | 
| 32 | IO4 | 
| 33 | TXD1 | 
| 34 | RXD1 | 
| 35 | I2C2_SDA | 
| 36 | I2C2_SCL | 
| 37 | IO5 | 
| 38 | IO6 | 
| 39 | GND3 | 
| 40 | GND4 | 
| F1 | GND5 | 
| F2 | GND6 | 
| F3 | GND7 | 
| F4 | GND8 | 


### WisConnector Pin Order

The Figure 2 shows the pin order of the WisConnector , which is located in the bottom layer of the module.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1594963724\/32151\/adjndnzaglgvzt2tpvfk.jpg",
        "mode": "300",
        "width": 467,
        "height": 687,
        "caption": "**Figure 2**: WisConnector pin order"
    }
}]$

### Core Module

The breakout module itself has a RAK4630 at its core, the Figure 3 shows the core module pin and connection information, by default, the NFC function is disabled for conserve the low power characteristic.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1594964025\/32151\/vjpevuvfqnztj0us1y2a.jpg",
        "mode": "responsive",
        "width": 783,
        "height": 700,
        "caption": "**Figure 3**: Core module pin definition"
    }
}]$

| **Pin No.** | **Name** | 
| ---- | ---- | 
| 1 | VBUS | 
| 2 | USB- | 
| 3 | USB+ | 
| 4 | P0.13/I2C_SDA | 
| 5 | P0.14/I2C_SCL | 
| 6 | P0.15/UART2_RX | 
| 7 | P0.16/UART2_TX | 
| 8 | P0.17/UART2_DE | 
| 9 | P0.19/UART1_RX | 
| 10 | P0.20/UART1_TX | 
| 11 | P0.21/UART1_DE | 
| 12 | P0.10/NFC2 | 
| 13 | P0.09/NFC1 | 
| 14 | GND | 
| 15 | RF_BT | 
| 16 | GND | 
| 17 | NRF_RESET | 
| 18 | SWDCLK | 
| 19 | SWDIO | 
| 20 | VBAT_SX | 
| 21 | VBAT_IO_SX | 
| 22 | GND | 
| 23 | P0.24/I2C_SDA_2 | 
| 24 | P0.25/I2C_SCL_2 | 
| 25 | P1.01/SW1 | 
| 26 | P1.02/SW2 | 
| 27 | P1.03/LED1 | 
| 28 | P1.04/LED2 | 
| 29 | P0.03/QSPI_CLK | 
| 30 | P0.02/QSPI_DIO3 | 
| 31 | P0.28/QSPI_DIO2 | 
| 32 | P0.29/QSPI_DIO1 | 
| 33 | P0.30/QSPI_DIO0 | 
| 34 | P0.26/QSPI_CS | 
| 35 | GND | 
| 36 | GND | 
| 37 | RF_LoRa | 
| 38 | GND | 
| 39 | P0.31/AIN7 | 
| 40 | P0.05/AIN3 | 
| 41 | P0.04/AIN2 | 
| 42 | GND | 
| 43 | VDD_NRF | 
| 44 | VBAT_NRF | 


### SWD Interface

The breakout module expose an SWD debug interface, the Figure 4 shows the connection information. Additionally, the RST pin is used for resetting the core module RAK4630.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1595069471\/32151\/fdy0wvn1hfdwyupe7vlb.jpg",
        "mode": "responsive",
        "width": 309,
        "height": 238,
        "caption": "**Figure 4**: SWD interface"
    }
}]$

### Power up automatic reset

The breakout module has a power up automatic reset circuit, the Figure 5 shows the automatic reset mechanism, this module also can be reset though RAK5005 reset pin.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1595069607\/32151\/o7fhgiypgjrtl9gnvszw.jpg",
        "mode": "responsive",
        "width": 174,
        "height": 386,
        "caption": "**Figure 5**: Power up automatic reset"
    }
}]$

### Flash

The RAK4630 module comprises a flash memory controlled by the SPI interface. The memory size is 8 Mb.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1595069891\/32151\/njnwyqi57cteospvatte.jpg",
        "mode": "600",
        "width": 726,
        "height": 189,
        "caption": "**Figure 6**: Flash"
    }
}]$

