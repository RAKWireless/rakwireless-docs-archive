---
type: page
title: Pin Definition
listed: true
slug: pin-definition---rak815-hybrid-location-tracker
---published

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1586327959\/17616\/po30wwudxuperjemcu3a.jpg",
        "mode": "responsive",
        "width": 10070,
        "height": 6001,
        "caption": "**Figure 1**: RAK815 Interface"
    }
}]$

$plugin[{
    "type": "callout",
    "data": {
        "text": "The pin numbers in the succeeding tables are sorted from top to bottom referred from the diagram above.",
        "type": "info",
        "title": "Note"
    }
}]$

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1565321783\/17616\/ayfv1uka45jedsak7obx.jpg",
        "mode": "300",
        "width": 3100,
        "height": 3133,
        "caption": "**Figure 2**: RAK815 SWD Debug Interface"
    }
}]$

### SWD Debug Interface

| **Pin** | **Name** | **Description** | 
| ---- | ---- | ---- | 
| 1 | VCC3.3 | 3.3V Power Supply | 
| 2 | SWDIO | SWD Interface data pin for NRF52832 | 
| 3 | SWDCLK | SWD Interface clock pin for NRF52832 | 
| 4 | P0.21_NRST | P0.21 for NRF52832, can be used as Reset pin (Button3) | 
| 5 | GND | Ground | 


$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1565321819\/17616\/muecmpudsdqesy4rdbvq.jpg",
        "mode": "600",
        "width": 6014,
        "height": 3029,
        "caption": "**Figure 3:** RAK815 UART Switch Interface"
    }
}]$

### UART Switch Interface

| **Pin** | **Name** | **Description** | 
| ---- | ---- | ---- | 
| 1 | GPS_TXD | UART TXD pin for GPS module | 
| 2 | GPS_RXD | UART RXD pin for GPS module | 
| 3 | P0.28 | P0.28 for NRF52832, Used as UART RXD | 
| 4 | P0.29 | P0.29 for NRF52832, Used as UART TXD | 
| 5 | TXD | The CP2102 converts the USB to the TXD pin of the UART | 
| 6 | RXD | The CP2102 converts the USB to the RXD pin of the UART | 


$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1565354996\/17616\/nsi68wvieymuh7rxrole.jpg",
        "mode": "300",
        "width": 800,
        "height": 800,
        "caption": "**Figure 4**: RAK815 GPS Module Expansion"
    }
}]$

### GPS Module Expansion

| **Pin** | **Name** | **Description** | 
| ---- | ---- | ---- | 
| 1 | VCC3.3 | 3.3V Power Supply | 
| 2 | GND | Ground | 
| 3 | GPS_TXD | UART TXD Pin for GPS Module | 
| 4 | GPS_RXD | UART RXD Pin for GPS Module | 
| 5 | P0.30 | P0.30 for NRF52832, used to control GPS module PPS | 


$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1565355121\/17616\/w32ph1qi0u8cxproa7ql.jpg",
        "mode": "600",
        "width": 900,
        "height": 600,
        "caption": "**Figure 5**: RAK815 Reserved I2C Interface"
    }
}]$

### Reserved I2C Interface of the LCD

| **Pin** | **Name** | **Description** | 
| ---- | ---- | ---- | 
| 1 | GND | Ground | 
| 2 | VCC3.3 | 3.3V Power Supply | 
| 3 | SCL | I2C SCL Clock Line | 
| 4 | SDA | I2C SDA Data Line | 


$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1565360053\/17616\/gflxrc5pbkxk2qpzptzb.jpg",
        "mode": "responsive",
        "width": 7788,
        "height": 7260,
        "caption": "**Figure 6**: RAK815 P1 and P3 Pinout"
    }
}]$

**Refer to this [[link](https://trello-attachments.s3.amazonaws.com/5d0661984b710a15f2d77e5a/5d404c95e4fe39657598137d/309aff8a522aaef94b2f03cf8a70e301/RAK815_-_P1_and_P3_Interface_Pinoout.jpg)]**for high quality image.

### Extension Interface P1

| **Pin** | **Name** | **Description** | 
| ---- | ---- | ---- | 
| 1 | GND | Ground | 
| 2 | P0.24 | P0.24 for NRF52832, used to control the expansion Button2 | 
| 3 | P0.25 | P0.25 for NRF52832, used to control the expansion LED6 | 
| 4 | P0.26 | P0.26 for NRF52832, used to control the expansion LED7 | 
| 5 | P0.27 | P0.27 for NRF52832, used to control the expansion Button1 | 
| 6 | P0.28 | P0.28 for NRF52832, used as UART RXD | 
| 7 | P0.29 | P0.29 for NRF52832, used as UART TXD | 
| 8 | P0.30 | P0.30 for NRF52832, used to control GPS module PPS | 
| 9 | P0.31 | P0.31 for NRF52832, used to control GPS module power | 
| 10 | GND | Ground | 
| 11 | GND | Ground | 
| 12 | GND | Ground | 
| 13 | VCC3.3 | 3.3V Power Supply | 
| 14 | VCC3.3 | 3.3V Power Supply | 


### Extension Interface P3

| **Pin** | **Name** | **Description** | 
| ---- | ---- | ---- | 
| 1 | GND | Ground | 
| 2 | SWDIO | SWD Interface data pin for NRF52832 | 
| 3 | SWDCLK | SWD Interface clock pin for NRF52832 | 
| 4 | P0.20 | P0.20 for NRF52832 | 
| 5 | P0.19 | P0.19 for NRF52832 | 
| 6 | P0.18 | P0.18 for NRF52832 | 
| 7 | P0.17 | P0.17 for NRF52832 | 
| 8 | P0.16 | P0.16 for NRF52832, used as I2C SCL | 
| 9 | P0.15 | P0.15 for NRF52832, used as I2C SDA | 
| 10 | GND | Ground | 
| 11 | P0.21_NRST | P0.21 for NRF52832, can be used as Reset pin (Button3) | 
| 12 | P0.04 | P0.04 for NRF52832, used to control LIS3DH module INT1 | 
| 13 | P0.03 | P0.03 for NRF52832, used to control LIS3DH module INT2 | 
| 14 | P0.02 | P0.02 for NRF52832, used as ADC to detect battery charge | 


