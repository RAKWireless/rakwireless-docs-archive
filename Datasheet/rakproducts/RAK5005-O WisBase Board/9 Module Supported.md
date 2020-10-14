---
type: page
title: Module Supported
listed: false
slug: module-supported-rak5005-o
---draft

In this section, there is a brief introduction about WisBlock module. It can help you to understand and choose the module you want. About the detail of each module, please refer the reference manual of the respective module.

### WisBlock Module in Production

RAK5005-O supports different kind of modules, according to the function and its the position on the RAK5005-O. These modules are classified into three categories:

1. **WisDuo**: containis MCU and wireless link transceiver. 
2. **WisSensor**: integrates mems sensor 
3. **WisIO**: extends IO, power supply, and sensors.

The table below shows the WisDuo modules:

| **P/N** | **RAK module on it** | **Function** | **Chipset** | 
| ---- | ---- | ---- | ---- | 
| RAK4261 | RAK4260 | MCU+LoRa | MicroChip ATSAMR34J18B | 
| RAK4631 | RAK4630 | BLE+LoRa | Nordic nRF52840+SX1262 | 
| RAK4281 | RAK4280 | MCU+LoRa | ST STM32L476+SX1262 | 
| RAK3401 | RAK3400 | BLE | Nordic nRF52840 | 


The table below shows the WisSensor modules:

| **P/N** | **Function** | **Chipset** | 
| ---- | ---- | ---- | 
| RAK1901 | Temperature & Humidity Sensor | Sensirion SHTC3 | 
| RAK1902 | Pressure Sensor | ST LPS22HB | 
| RAK1903 | Ambient Light Sensor | TI OPT3001DNPR | 
| RAK1904 | 3-axis Sensor | ST LIS3DH | 
| RAK1905 | 9-axis Sensor | TDK ICM20948 | 
| RAK1906 | Environmental Sensor | BOSCH BME680 | 
| RAK1910 | GPS Sensor | U-BLOX MAX-7Q | 


The table shows the WisIO modules:

| P/N | Function | Chipset | 
| ---- | ---- | ---- | 
| RAK5801 | 4–20mA sensor interface |  | 
| RAK5802 | RS485 interface |  | 
| RAK5803 | 0–5V sensor interface |  | 
| RAK5804 | IO extension board |  | 
| RAK2305 | WiFi extension board | ESP32 | 
| RAK2705 | NFC reader board | ST CR95HF | 
| RAK5860 | NB-IoT | BG77 | 
| RAK5804 | IO extension board |  | 


### WisBlock: Function and Data Bus Supported

### WisDuo Function and Data Bus

| RAK4202 Pin Definition | RAK4601 Pin Definition | RAK4261 Pin Definition | RAK4231 Pin Definition | RAK4201 Pin Definition | Function Name of WisBase | Pin Number | Pin Number | Function Name of WisBase | RAK4201 Pin Definition | RAK4231 Pin Definition | RAK4261 Pin Definition | RAK46011 Pin Definition | RAK4202 Pin Definition | 
| ---- | ---- | ---- | ---- | ---- | ---- | ---- | ---- | ---- | ---- | ---- | ---- | ---- | ---- | 
| NC | NC | NC | NC | NC | VBAT | 1 | 2 | VBAT | NC | NC | NC | NC | NC | 
| GND | GND | GND | GND | GND | GND | 3 | 4 | GND | GND | GND | GND | GND | GND | 
| 3V3 | 3V3 | 3V3 | 3V3 | 3V3 | 3V3 | 5 | 6 | 3V3 | 3V3 | 3V3 | 3V3 | 3V3 | 3V3 | 
| NC | NC | PA25_USB_P | NC | NC | USB+ | 7 | 8 | USB– | NC | NC | PA24_USB_N | NC | NC | 
| NC | NC | NC | NC | NC | VBUS | 9 | 10 | SW1 | NC | NC | NC | NC | NC | 
| UART1_TX1 | UART1_TX1 | UART1_TX1 | UART1_TX1 | UART1_TX1 | TXD0 | 11 | 12 | RXD0 | UART1_RX1 | UART1_RX1 | UART1_RX1 | UART1_RX1 | UART1_RX1 | 
| MCU_RST | MCU_RST | MCU_RST | MCU_RST | MCU_RST | RESET | 13 | 14 | LED1 | NC | NC | LED3/PA07 | NC | LED1/PA12 | 
| LED2/PB04 | NC | LED2/PA27 | NC | NC | LED2 | 15 | 16 | LED3 | NC | NC | AIN1/PA09 | NC | LED3/PA15 | 
| 3V3 | 3V3 | 3V3 | 3V3 | 3V3 | VDD | 17 | 18 | VDD | 3V3 | 3V3 | 3V3 | 3V3 | 3V3 | 
| I2C1_SDA/PB9 | I2C1_SDA | I2C1_SDA | I2C1_SDA | I2C1_SDA | I2C1_SDA | 19 | 20 | I2C1_SCL | I2C1_SCL | I2C1_SCL | I2C1_SCL | I2C1_SCL | I2C1_SCL/PB8 | 
| AIN0/PAO | NC | AIN0/UART1_DE | AIN0/UART1_DE | AIN0/UART1_DE | AIN0 | 21 | 22 | AIN1 | NC | NC | AIN1/PA09 | NC | AIN1/PA2 | 
| BOOT0 | NC | NC | NC | NC | BOOT0 | 23 | 24 | NC | NC | NC | NC | NC | NC | 
| NC | NC | PA | NC | NC | SPI_CS | 25 | 26 | SPI_CLK | SPI_CLK_1 | SPI_CLK_1 | PB23_SCK | NC | NC | 
| NC | NC | SPI_MISO_1 | SPI_MISO_1 | SPI_MISO_1 | SPI_MISO_1 | 27 | 28 | SPI_MOSI | SPI_MOSI_1 | SPI_MOSI_1 | PA23_MOSI | NC | NC | 
| 1PPS | IO1/RESERVED | IO1/PB22 | NC | IO1/UART0_DE | IO1 | 29 | 30 | IO2 | NC | NC | PA15 | IO2/RESERVED | STANDBY/PB2 | 
| IO3/PB3 | IO3/NFC1 | IO3/PA14 | NC | NC | IO3 | 31 | 32 | IO4 | NC | NC | NC | IO4/NFC2 | IO4/PB5 | 
| UART2_TX1/PB10 | USART2_TX1 | UART3_TX1 | UART0_TX1 | UART0_TX1 | TXD1 | 33 | 34 | RXD1 | UART0_RX _1 | UART0_RX_1 | UART_RX | UART2_RX | UART2_RX/PB11 | 
| NC | NC | NC | NC | NC | I2C2_SDA | 35 | 36 | I2C2_SCL | NC | NC | NC | NC | NC | 
| IO5/PB15 | NC | NC | NC | NC | IO5 | 37 | 38 | IO6 | NC | NC | NC | NC | IO6/PA8 | 
| GND | GND | GND | GND | GND | GND | 39 | 40 | GND | GND | GND | GND | GND | GND | 


### WisSensor Funtion and Data Bus

| Type 4 | Type 3 | Type 2 | Type 1 | D | C | B | A | Pin Number | Pin Number | A | B | C | D | Type 1 | Type 2 | Type 3 | Type 4 | 
| ---- | ---- | ---- | ---- | ---- | ---- | ---- | ---- | ---- | ---- | ---- | ---- | ---- | ---- | ---- | ---- | ---- | ---- | 
| RXD | NC | NC | NC | NC | NC | NC | TXS1 | 1 | 2 | GND | GND | GND | GND | GND | GND | GND | GND | 
| NC | NC | NC | NC | SPI_CS | SPI_CS | SPI_CS | SPI_CS | 3 | 4 | SPI_CLK | SPI_CLK | SPI_CLK | SPI_CLK | NC | NC | NC | NC | 
| NC | NC | NC | NC | SPI_MISO | SPI_MISO | SPI_MISO | SPI_MISO | 5 | 6 | SPI_MOSI | SPI_MOSI | SPI_MOSI | SPI_MOSI | NC | NC | NC | NC | 
| NC | I2C1_SCL | I2C1_SCL | I2C1_SCL | I2C1_SCL | I2C1_SCL | I2C1_SCL | I2C1_SCL | 7 | 8 | I2C1_SDA | I2C1_SDA | I2C1_SDA | I2C1_SDA | I2C1_SDA | I2C1_SDA | I2C1_SDA | NC | 
| NC | VDD | VDD | VDD | VDD | VDD | VDD | VDD | 9 | 10 | IO2 | IO1 | IO4 | IO6 | NC | NC | INT2 | RESET | 
| 3V3_S | NC | NCN | NC | 3V3_S | 3V3_S | 3V3_S | 3V3_S | 11 | 12 | IO1 | IO2 | IO3 | IO5 | NC | INT | INT1 | 1PPS | 
| 1PPS | INT1 | INT | NC | NC | NC | NC | NC | 13 | 14 | 3V3_S | 3V3_S | 3V3_S | 3V3_S | NC | NC | NC | 3V3_S | 
| RESET | INT2 | NC | NC | NC | NC | NC | NC | 15 | 16 | VDD | VDD | VDD | VDD | VDD | VDD | VDD | NC | 
| NC | I2C1_SDA | I2C1_SDA | I2C1_SDA | NC | NC | NC | NC | 17 | 18 | NC | NC | NC | NC | I2C1_SCL | I2C1_SCL | I2C1_SCL | NC | 
| NC | NC | NC | NC | NC | NC | NC | NC | 19 | 20 | NC | NC | NC | NC | NC | NC | NC | NC | 
| NC | NC | NC | NC | NC | NC | NC | NC | 21 | 22 | NC | NC | NC | NC | NC | NC | NC | NC | 
| GND | GND | GND | GND | GND | GND | GND | GND | 23 | 24 | RXD1 | NC | NC | NC | NC | NC | NC | TXD | 


The WisSensor data bus is divided into four type. The relationship is shown in the table below:

| **Sensor Type** | **WisSensor** | **Description** | 
| ---- | ---- | ---- | 
| Type 1 | RAK1901 | Temperature & Humidity Sensor | 
|  | RAL1906 | Environmental Sensor | 
| Type 2 | RAK1902 | Pressure Sensor | 
|  | RAK1903 | Ambient Light Sensor | 
|  | RAK1905 | 9-axis Sensor | 
| Type 3 | RAK1904 | 3-axis Sensor | 
| Type 4 | RAK1910 | GPS Sensor | 


### WisIO Function and Data Bus

| RAK2305 | RAK2705 | RAK5802 | RAK5801 | Function Name of WisBase | Pin Number | Pin Number | Function Name of WisBase | RAK5801 | RAK5802 | RAK2705 | RAK2305 | 
| ---- | ---- | ---- | ---- | ---- | ---- | ---- | ---- | ---- | ---- | ---- | ---- | 
| ESP32 | NFC | RS485 | 4-20mA |  |  |  |  | 4-20mA | RS485 | NFC | ESP32 | 
| VBAT | VBAT | VBAT | VBAT | VBAT | 1 | 2 | VBAT | VBAT | VBAT | VBAT | VBAT | 
| GND | GND | GND | GND | GND | 3 | 4 | GND | GND | GND | GND | GND | 
| NC | NC | NC | NC | 3V3 | 5 | 6 | 3V3_S | 3V3 | 3V3 | NC | NC | 
| NC | NC | NC | NC | USB+ | 7 | 8 | USB– | NC | NC | NC | NC | 
| NC | NC | NC | NC | VBUS | 9 | 10 | SW1 | NC | NC | NC | NC | 
| TXD0 | NC | NC | NC | TXD0 | 11 | 12 | RXD0 | NC | NC | NC | RXD0 | 
| NC | NC | NC | NC | RESET | 13 | 14 | LED1 | NC | NC | NC | LED1 | 
| LED2 | NC | NC | NC | LED2 | 15 | 16 | LED3 | NC | NC | NC | NC | 
| NC | NC | NC | NC | VDD | 17 | 18 | VDD | NC | NC | NC | NC | 
| I2C1_SDA | NC | I2C1_SDA | I2C1_SDA | I2C1_SDA | 19 | 20 | I2C1_SCL | I2C1_SCL | I2C1_SCL | NC | I2C1_SCL | 
| NC | NC | AIN0 | AIN0 | AIN0 | 21 | 22 | AIN1 | AIN1 | NC | NC | NC | 
| NC | NC | NC | NC | NC | 23 | 24 | NC | NC | NC | NC | NC | 
| SPI_CS | SPI_CS* | NC | NC | SPI_CS | 25 | 26 | SPI_CLK | NC | NC | SPI_CLK* | SPI_CLK | 
| SPI_MISO | SPI_MISO* | NC | NC | SPI_MISO | 27 | 28 | SPI_MOSI | NC | NC | SPI_MOSI* | SPI_MOSI | 
| NC | NC | NC | NC | IO1 | 29 | 30 | IO2 | NC | NC | NC | IO2 | 
| NC | SPI_CS | NC | NC | IO3 | 31 | 32 | IO4 | NC | NC | SPI_CLK | NC | 
| RXD1 | RXD1 | RXD1 | NC | TXD1 | 33 | 34 | RXD1 | NC | TXD1 | TXD1 | TXD1 | 
| NC | NC | NC | NC | I2C2_SDA | 35 | 36 | I2C2_SCL | NC | NC | NC | NC | 
| NC | SPI_MISO | NC | NC | IO5 | 37 | 38 | IO6 | NC | NC | SPI_MOSI | NC | 
| GND | GND | GND | GND | GND | 39 | 40 | GND | GND | GND | GND | GND | 


$plugin[{
    "type": "callout",
    "data": {
        "text": "- Can be supported by rework hardware.",
        "type": "info",
        "title": "Info"
    }
}]$

