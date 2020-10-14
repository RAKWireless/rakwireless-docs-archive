---
type: page
title: Pin Definition
listed: false
slug: pin-definition-rak5801
---draft

In this section, it covers the pin number of the sensor connector, the definition, and the functionalities of each pin shown in a tabular representation. 

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1595494816\/32359\/x7oukfypxf1nnsjh6es0.png",
        "mode": "responsive",
        "width": 399,
        "height": 478,
        "caption": "**Figure 1**: RAK5801 sensor connector"
    }
}]$

| **Pin Number** | **Function Description** | 
| ---- | ---- | 
| 1 | SCL of the I2C interface | 
| 2 | SDA of the I2C interface | 
| 3 | 3V3 output | 
| 4 | VBAT, Battery output | 
| 5 | 12V output for external sensors | 
| 6 | GND | 
| 7 | Analog input 0 | 
| 8 | Analog input 1 | 


With the  WisIO connector, the RAK5801 module is attached to the WisBoard baseboard. Refer to Figure 2 for the pin order of the WisIO connector of the module. 

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1595498782\/32359\/vwvgm3vtjnwsuydl1li5.png",
        "mode": "responsive",
        "width": 763,
        "height": 457,
        "caption": "**Figure 2**: RAK5801 Internal WisIO Connector"
    }
}]$

The functionalities of each pins of the WisIO connector are tabulated below.

| **Pin Number** | **Description** | **Pin Number** | **Description** | 
| ---- | ---- | ---- | ---- | 
| 1 | Battery Power | 2 | Battery Power | 
| 3 | GND | 4 | GND | 
| 5 | NC, reserved for 3V3 | 6 | 3.3V Power | 
| 7 | NC | 8 | NC | 
| 9 | NC | 10 | NC | 
| 11 | NC | 12 | NC | 
| 13 | NC | 14 | NC | 
| 15 | NC | 16 | NC | 
| 17 | NC | 18 | NC | 
| 19 | SDA for I2C1 | 20 | SCL for I2C1 | 
| 21 | NC | 22 | Analog to MCU | 
| 23 | NC | 24 | NC | 
| 25 | NC | 26 | NC | 
| 27 | NC | 28 | NC | 
| 29 | Enable note1 | 30 | NC | 
| 31 | NC | 32 | Analog0 to MCU | 
| 33 | NC | 34 | NC | 
| 35 | NC | 36 | NC | 
| 37 | NC | 38 | NC | 
| 39 | GND | 40 | GND | 


$plugin[{
    "type": "callout",
    "data": {
        "text": "This signal controls the dc-dc power supply on RAK5801, before capture analog signal, please set this pin to high to enable power for RAK5801.",
        "type": "info",
        "title": "Info"
    }
}]$

