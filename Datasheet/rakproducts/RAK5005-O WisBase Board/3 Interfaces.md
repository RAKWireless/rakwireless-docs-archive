---
type: page
title: Interfaces
listed: false
slug: interfaces-rak5005-o
---draft

RAK5005-O provides the following interfaces, headers, jumpers, buttons and connectors:

- 1 connector for WisDuo 
- 1 connector for WisIO 
- 4 connectors for WisSensor 
- Micro USB connector 
- 3 sets of 4-pin 2.54mm headers (UART, GPIOS, I2C, power etc.) 
- 2-pin battery interface 
- 2-pin solar panel interface 
- LEDs 
- Reset button

### Micro-B USB port

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1594996975\/32154\/irahairz666wq95a0sjl.png",
        "mode": "responsive",
        "width": 195,
        "height": 89,
        "caption": "**Figure 1:** Micro-B USB connector's pinout"
    }
}]$

The Micro-B USB connector is compliant with the USB2.0 specification. This USB interface is connected to the BG96. BG96's AT command port, GNSS port, and Debug port. It is also used as a charging input port for the battery. The Micro-B USB pin definition is shown below:

| **Pin** | **Description** | 
| ---- | ---- | 
| 1 | USB_VBUS (+5V) | 
| 2 | USB_DM | 
| 3 | USB_DP | 
| 4 | NC | 
| 5 | GND | 


### J10, J11, J12 headers

On the WisBlock, there are 3 pieces of 2.54mm pitch header for IO extension. Some data bus and signal from the MCU module are also connected to these headers, such as I2C, UART, ADC, etc.

**J10 pin definition**

| **Pin** | **Description** | 
| ---- | ---- | 
| 1 | - BOOT0 from ST MCU. <br>- The ST MCU will enter boot mode when connector BOOT0 to VDD during reset. | 
| 2 | GND | 
| 3 | UART1 TX | 
| 4 | UART1 RX | 


**J11 pin definition**

| **Pin** | **Description** | 
| ---- | ---- | 
| 1 | AIN, ADC input signal | 
| 2 | - IO1<br>- General purpose IO | 
| 3 | - IO2<br>- Used for 3V3_S enable | 
| 4 | VBAT | 


**J12 pin definition**

| **Pin** | **Description** | 
| ---- | ---- | 
| 1 | VDD | 
| 2 | GND | 
| 3 | I2C clock | 
| 4 | I2C data | 


### Battery Connector

The pin definition of a Li-ion battery connector is shown in the table below.

| **Pin** | **Pin Name** | **Description** | 
| ---- | ---- | ---- | 
| 1 | GND | GND | 
| 2 | VBAT | Positive of the battery | 


$plugin[{
    "type": "callout",
    "data": {
        "text": "The voltage of the battery **must not exceed 4.3V**.",
        "type": "info",
        "title": "Info"
    }
}]$

### Solar Panel Connector

The pin definition of the solar panel connector is shown in the table below.

| **Pin** | **Pin Name** | **Description** | 
| ---- | ---- | ---- | 
| 1 | C0NN_5V | Positive of solar panel | 
| 2 | GND | GND | 


$plugin[{
    "type": "callout",
    "data": {
        "text": "The output of the solar panel **must not exceed 5.5V**, otherwise, it may cause permanent damage to the board.",
        "type": "info",
        "title": "Info"
    }
}]$

### LEDs

Three LEDs are used to indicate the operating status. Below are the functions of the LEDs:

- **Red LED** - connected to the charger chip to indicate the charger status. When the battery is charging, this red LED is on. When the battery is full, this LED is weak light or off.
- **Green LED** - connected to the MCU module, controlled by MCU defined by the user.
- **Blue LED** - connected to the MCU module, controlled by MCU defined by the user.

### RESET Push Button

The Reset Push Button is connected to the MCU module. When pushed, it resets the MCU.

