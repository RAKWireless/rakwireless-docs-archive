---
type: page
title: Pin Definition
listed: true
slug: pin-definition-rak2287
---published

### Pinout Diagram

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1590744586\/23910\/nemdunu4snqbtkybvvte.jpg",
        "mode": "responsive",
        "width": 1686,
        "height": 1640,
        "caption": null
    }
}]$

### Pinout Description

| **Type** | **Description** | 
| ---- | ---- | 
| IO | Bidirectional | 
| DI | Digital input | 
| DO | Digital output | 
| OC | Open collector | 
| OD | Open drain | 
| PI | Power input | 
| PO | Power output | 
| NC | No Connection | 


| **Pin No.** | **Mini PCIEx Pin<br>Rev. 2.0** | **RAK2287 Pin** | **Type** | **Description** | **Remarks** | 
| ---- | ---- | ---- | ---- | ---- | ---- | 
| **1** | WAKE# | SX1261_BUSY | DO | No Connection by default | Reserved for future applications | 
| **2** | 3.3Vaux | 3V3 | PI | 3.3V DC supply |  | 
| **3** | COEX1 | SX1261_DIO1 | IO | No Connection by default | Reserved for future applications | 
| **4** | GND | GND |  | Ground |  | 
| **5** | COEX2 | SX1261_DIO2 | IO | No Connection by default | Reserved for future applications | 
| **6** | 1.5V | GPIO(6) | IO |  | Connect to SX1302’s GPIO[6]. | 
| **7** | CLKREQ# | SX1261_NSS | DI | No Connection by default | Reserved for future applications | 
| **8** | UIM_PWR | NC |  | No Connection |  | 
| **9** | GND | GND |  | Ground |  | 
| **10** | UIM_DATA | NC |  | No Connection |  | 
| **11** | REFCLK- | SX1261_NRESET | DI | No Connection by default | Reserved for future applications | 
| **12** | UIM_CLK | NC |  | No Connection |  | 
| **13** | REFCLK+ | MCU_NRESET | DI | No Connection by defaul | Reserved for future applications | 
| **14** | UIM_RESET | NC |  | No Connection |  | 
| **15** | GND | GND |  | Ground |  | 
| **16** | UIM_VPP | NC |  | No Connection |  | 
| **17** | RESERVED | NC |  | No Connection |  | 
| **18** | GND | GND |  | Ground |  | 
| **19** | RESERVED | PPS | DO | Time pulse output | Leave open if not used. | 
| **20** | W_DISABLE# | NC |  | No Connection |  | 
| **21** | GND | GND |  | Ground |  | 
| **22** | PERST# | SX1302_RESET | DI | RAK2287 reset input | Active high, ≥100ns for <br><br>SX1302 reset. | 
| **23** | PERn0 | RESET_GPS | DI | GPS module ZOE-M8Q reset inputs | Active low, Leave open if not used. | 
| **24** | 3.3Vaux | 3V3 | PI | 3.3V DC supply |  | 
| **25** | PERp0 | STANDBY_GPS | DI | GPS module ZOE-M8Q external interrupt input | Active low, Leave open if not used. | 
| **26** | GND | GND |  | Ground |  | 
| **27** | GND | GND |  | Ground |  | 
| **28** | 1.5V | NC |  | No Connection |  | 
| **29** | GND | GND |  | Ground |  | 
| **30** | SMB_CLK | I2C_SCL | IO | HOST SCL | Connect to GPS module ZOE-M8Q’s SCL internally. Leave<br>open if not used. | 
| **31** | PETn0 | PI_UART_TX | DI | HOST UART_TX | Connect to GPS module ZOE-M8Q’s UART_RX internally.<br>Leave open if not used. | 
| **32** | SMB_DATA | I2C_SDA | IO | HOST SDA | Connect to GPS module ZOE-M8Q’s SDA internally. Leave<br>open if not used. | 
| **33** | PETp0 | PI_UART_RX | DO | HOST UART_RX | Connect to GPS module ZOE-M8Q’s UART_TX internally.<br>Leave open if not used. | 
| **34** | GND | GND |  | Ground |  | 
| **35** | GND | GND |  | Ground |  | 
| **36** | USB_D- | USB_DM | IO | USB differential data (-) | Require differential impedance of 90Ω. | 
| **37** | GND | GND |  | Ground |  | 
| **38** | USB_D+ | USB_DP | IO | USB differential data (+) | Require differential impedance of 90Ω. | 
| **39** | 3.3Vaux | 3V3 | PI | 3.3V DC supply |  | 
| **40** | GND | GND |  | Ground |  | 
| **41** | 3.3Vaux | 3V3 | PI | 3.3V DC supply |  | 
| **42** | LED_WWAN# | NC |  | No Connection |  | 
| **43** | GND | GND |  | Ground |  | 
| **44** | LED_WLAN# | NC |  | No Connection |  | 
| **45** | RESERVED | HOST_SCK | I/O | Host SPI CLK |  | 
| **46** | LED_WPAN# | NC |  | No Connection |  | 
| **47** | RESERVED | HOST _MISO | I/O | Host SPI MISO |  | 
| **48** | 1.5V | NC |  | No Connection |  | 
| **49** | RESERVED | HOST _MOSI | I/O | Host SPI MOSI |  | 
| **50** | GND | GND |  | Ground |  | 
| **51** | RESERVED | HOST _CSN | I/O | Host SPI CS |  | 
| **52** | 3.3Vaux | 3V3 | PI | 3.3V DC supply |  | 


