---
type: page
title: Schematic Diagram
listed: true
slug: schematic-diagram-rak1920
---published

## Power Supply

The RAK1920 module supports 3.3V and 5V options, by default, the 3.3V is used as the power source of sensors. The module integrates a  boost converter from the VBAT to 5V. The VBAT is the battery output voltage, usually between 3.7V and 4.2V. The EN pin enables this boost converter and is controlled by the WisCore module of the overall solution. 

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1595564349\/32532\/qlu7ayicbgtvchcneoxt.jpg",
        "mode": "600",
        "width": 945,
        "height": 518,
        "caption": "**Figure 1**: Power supply"
    }
}]$

## WisIO Connector

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1595567650\/32532\/oxp6gpkxwyxoofmlyhh4.jpg",
        "mode": "600",
        "width": 580,
        "height": 570,
        "caption": "**Figure 2**: WisIO Connector"
    }
}]$

The RAK1920 module uses only a subset of all the pins available in the WisIO connector. These are shown in the table below:

| **Name** | **Description** | **Comment** | 
| ---- | ---- | ---- | 
| VBAT | battery output voltage | Maximum: 4.2 Volts | 
| 3V3 | 3.3 V | Default, sensor power supply | 
| TXD1/RXD1 | UART interface | Connected only to the Click Boards connector. | 
| CS/SCK/MOSI/MISO | SPI interface | Connected only to the Click Boards | 
| SDA/SCL | I2C interface | All I2C sensors | 
| AIN0/AIN1 | ADC input interfaces | Grove or click Boards | 
| INT | Hardware Interrupt | Connected only to the Click Boards connector. | 
| RST | Reset | Connected only to the Click Boards connector | 
| PWM | PWM input | Connected only to the Click Boards connector. | 
| EN | Boost Converter Enable | IO5 | 
| IO1/IO3 | General purpose I/O | Connected to Grove digital I/O sensors’<br>connectors. | 


### WisIO Connector Pin Order

The Figure 3 shows the WisIO connector’s pin order. The connector is located in the bottom layer of the RAK1920 module.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1595567938\/32532\/dxzsrzq95mintbtrcbnp.jpg",
        "mode": "300",
        "width": 662,
        "height": 555,
        "caption": "**Figure 3**: WisIO connector\u2019s pin order"
    }
}]$

