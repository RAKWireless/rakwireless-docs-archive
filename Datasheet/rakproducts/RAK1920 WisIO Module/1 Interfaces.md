---
type: page
title: Interfaces
listed: true
slug: interfaces-rak1920
---published

### Mikroe Click Boards Interfaces

The RAK1920 supports all the Click boards modules manufactured by Mikroe through the mikroBUS™ interface, the Figure 1 shows the pin number of the mikroBUS.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1595568378\/32533\/p0lybphwy6jqxf95rdug.jpg",
        "mode": "300",
        "width": 574,
        "height": 485,
        "caption": "**Figure 1**: Mikroe\u2019s mikroBUS\u00ae interface"
    }
}]$

The Figure 2 shows the definition of the mikroBUS interface:

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1595568431\/32533\/bqfrtnattszwfq7gzjzy.jpg",
        "mode": "600",
        "width": 801,
        "height": 366,
        "caption": "**Figure 2**: mikroBUS interface pin definition"
    }
}]$

### Grove Sensor Interfaces

The RAK1920 module supports the Grove I2C and digital I/O sensors. The Figure 3 shows the pin number and definition of the Grove sensor. By default, VCC is connected to 3.3V line of the WisIO connector. 

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1595568616\/32533\/msxvows6e7lzkmos1swh.jpg",
        "mode": "300",
        "width": 666,
        "height": 556,
        "caption": "**Figure 3**: Grove Sensor interfaces"
    }
}]$

By default, the I2C is enabled in the RAK1920 module, but if it is required, the RAK1920 module can also supports sensors with Grove UART interface and ADC sensors. To enable the UART interface,  a resistance connection needs to be added by the customer. When use Grove UART interface sensor module, replace R9 to R10, R11 to R12, when use Grove ADC interface (not ADC to I2C module) sensor module, replace R13 to R14, change R15 to R16. The Figure 4 shows replace connection resistance location.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1595568681\/32533\/abcnzp0qpe0g1xuzowid.jpg",
        "mode": "300",
        "width": 787,
        "height": 667,
        "caption": "**Figure 4**: Replace connection resistance location"
    }
}]$

The Figure 5 shows Grove sensor cables:

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1595568758\/32533\/opuzhfewyef4xyvno3ik.jpg",
        "mode": "300",
        "width": 579,
        "height": 392,
        "caption": "**Figure 5**: Grove Sensor cables"
    }
}]$

The table below is the  Grove cable color and function definition.

| **Pin** | **Color** | **Function** | 
| ---- | ---- | ---- | 
| 1 | Yellow | Digital IO1 /ADC CH1 /UART RX /I2C Cock | 
| 2 | White | Digital IO2 /ADC CH2 /UART TX /I2C Data | 
| 3 | Red | VCC | 
| 4 | Black | GND | 


### Qwiic Sensor Interface

The RAK1920 module supports sensors manufactured by SparkFun through the Qwiic Connet interface. The Figure 6 shows the Qwiic Connect interface.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1595568927\/32533\/siucuj1qzgj7wkqvtiuf.jpg",
        "mode": "300",
        "width": 524,
        "height": 403,
        "caption": "**Figure 6**: Qwiic Connect\u00ae interface"
    }
}]$

The Figure 7 shows a Qwiic Connect cable:

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1595569188\/32533\/zem5rncj3jo1jzpd0d78.jpg",
        "mode": "300",
        "width": 488,
        "height": 381,
        "caption": "**Figure 7**: Qwiic Cable"
    }
}]$

The table below shows the Qwiic Connect cable color and function definition:

| **Pin** | **Color** | **Function** | 
| ---- | ---- | ---- | 
| 1 | Yellow | I2C Cock | 
| 2 | Blue | I2C Data | 
| 3 | Red | 3.3V | 
| 4 | Black | GND | 


### Reserved I2C Interface

The RAK1920 module has a reserved I2C interface, it can be used for generic I2C interface sensors. Note, this I2C interface only supports 3.3V type of sensors. The Figure 8 shows the reversed I2C interface.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1595569768\/32533\/pwncz4kbheesydu4akue.jpg",
        "mode": "300",
        "width": 506,
        "height": 454,
        "caption": "**Figure 8**: Reserved I2C Interface"
    }
}]$

