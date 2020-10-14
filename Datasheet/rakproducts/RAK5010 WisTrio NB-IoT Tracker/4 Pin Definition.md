---
type: page
title: Pin Definition
listed: true
slug: pin-definition---rak5010-wistrio-nb-iot-tracker
---published

There are two connectors on the board.

### P1

Solar panel interface

| **Pin** | **Pin Name** | **Description** | 
| ---- | ---- | ---- | 
| 1 | C0NN_5V | Positive of Solar Panel | 
| 2 | GND | GND | 


$plugin[{
    "type": "callout",
    "data": {
        "text": "The output of the solar panel cannot exceed 5.5V, otherwise it may cause permanent damage to the board.",
        "type": "info",
        "title": "Note"
    }
}]$

### P2

Li-ion battery connector.

| **Pin** | **Pin Name** | **Description** | 
| ---- | ---- | ---- | 
| 1 | GND | GND | 
| 2 | VBAT | Positive of the Battery | 


### J9

J9 is J-LINK connector, with J-LINK debugger, you can program and debug nRF52840.

| **Pin** | **Pin Name** | **Description** | 
| ---- | ---- | ---- | 
| 1 | VDD | 1.8V default. Reference voltage for J-LINK, note 1 | 
| 2 | SWDIO | SWD data signal(3.3V<br>tolerant) | 
| 3 | SWDCLK | SWD clock signal(3.3V tolerant) | 
| 4 | GND | GND | 


$plugin[{
    "type": "callout",
    "data": {
        "text": "VDD of J9 should\nconnect to the PIN1 of SEGGER J-LINK (See Figure Below) debugger for SWDIO\/SWDCLK\u2019s\nreference voltage. If this pin is not connect correctly, the J-LINK\u2019 logic\nlevel may not set to VDD of nrf52840, it may damage the nrf52840.",
        "type": "info",
        "title": "Note"
    }
}]$

Below is the definition of 20PIN segger J-LINK connector:

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1578895018\/18933\/jniplclj61xxyjkdu9my.png",
        "mode": "responsive",
        "width": 6806,
        "height": 4468,
        "caption": "**Figure 1**: J-LINK Pinout"
    }
}]$

| Pin | Signal | Type | Description | 
| ---- | ---- | ---- | ---- | 
| 1 | VTref | Input | This is the target<br>reference voltage. It is used to check if the target has power, to create the<br>logic-level reference for the input comparators and to control the output logic<br>levels to the target. It is normally fed from VDD of the target board and must<br>not have a series resistor | 


### J10 and J12

J10 and J12 are IO extension headers. Those are bridged from the nRF52840 IOs, through logical level shift circuits. Thus, the IOs level is set by the VREF pin. The function of these IOs is configurable. They can work as UART, I2C ，general GPIO or AD.

- Definition of J10:

| Pin | Pin Name | Description | 
| ---- | ---- | ---- | 
| 1 | GND | GND | 
| 2 | VBAT | Connected to the Battery | 
| 3 | AIN | Configurable IO,<br>connected to AIN3 (P0.05) on nRF52840. If used as AD, the input range is<br>configurable, please refer to the manual of nrf52840, if used as general IO,<br>the logic level is 1.8V and there no level shift on it. | 
| 4 | NRF_IO1 | Configurable IO,<br>connected to P0.19 on the nRF52840. There is a level shift circuit between this<br>pin and the nRF52840 | 


- Definition of J12:

| **Pin** | **Pin Name** | **Description** | 
| ---- | ---- | ---- | 
| 1 | EXT_VREF | Reference level for<br>the IO extensions | 
| 2 | NRF_IO2 | Configurable IO, connect<br>to P0.20 on the nRF52840. There is a level shift circuit between this pin and<br>the nRF52840 | 
| 3 | NRF_IO3 | Configurable IO,<br>connect to P1.02 on the nRF52840. There is a level shift circuit between this<br>pin and the nRF52840 | 
| 4 | NRF_IO4 | Configurable IO, connect<br>to P1.01 on the nRF52840. There is a level shift circuit between this pin and<br>the nRF52840 | 


The logic level shift
circuit on the RAK5010 board connects EXT_VREF to your extension board’s power
and equalizes it to the logical level of the IO on your extension board.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1567039444\/-1\/nenylqh3frd5qoat9uhb.jpg",
        "mode": "responsive",
        "width": 672,
        "height": 329,
        "caption": "**Figure 2**:  Typical Converter Circuitry"
    }
}]$

