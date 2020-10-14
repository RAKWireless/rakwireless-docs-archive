---
type: page
title: Interfaces
listed: true
slug: interfaces-rak5010-wistrio-nb-iot
---published

The node is built around the BG96 module and the nRF52840 BLE chip. It provides the following interfaces, headers, jumpers, buttons and connectors:

- Micro USB
- 2 sets of 4-pin 2.54mm Headers (UART, GPIOS, I2C, power)
- 4-pin Jlink header
- 2-pin Battery female
interface
- 2-pin Solar Panel
female interface
- LEDs
- Reset Button
- PWR Button for the
BG96

There are two Antenna connectors:

- LTE Antenna with iPEX
connector
- GPS Antenna with iPEX
connector

### Micro-B USB Interface

A Standard Micro-B
USB compliant with USB 2.0 standard specification. This USB interface is
connected to the USB port of NRF52840 for default. It also can connect to BG96
by reworking some resistor on the board. If this USB port is connected to the
BG96, BG96’s AT command port GNSS port and debug port can be accessed through
this USB. It is also used as charge input port for battery. The Micro-B USB pin
definition is shown below:

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1567034111\/18930\/bjkgtz3guvyyqem8amsm.png",
        "mode": "responsive",
        "width": 181,
        "height": 75,
        "caption": "**Figure 2**: USB Connector Pinout"
    }
}]$

| **Pin** | **Description** | 
| ---- | ---- | 
| 1 | USB_VBUS (+5V) | 
| 2 | USB_DM | 
| 3 | USB_DP | 
| 4 | NC | 
| 5 | GND | 


This USB port is also
used as port for charging the battery.

### LEDs

Three LEDs are used
to indicate operating status, here are their functions:

| **Color** | **Connection** | **Function** | 
| ---- | ---- | ---- | 
| Green LED | connected to the nRF52840 | Defined by the user | 
| Blue LED | connect to the BG96 | Indicates the status<br>of the BG96. | 
| Red LED | connect to the BG96 | Indicates the network<br>status of the BG96 | 


### RESET Push Button

Reset Push Button is
used to reset the nRF52840. You can control the BG96 reset with by the firmware
of the nRF52840.

### PWRKEY Push Button

When the BG96 is in
power off mode, it can be turned back on to normal mode by holding the PWRKEY
button for at least 100ms. Holding the PWRKEY button for at least 650 ms, the
module will execute the power-down procedure, after the PWRKEY is released.

### BG96 - nRF52840 IO Connections 

The nRF52840
communicates with the BG96 primarily though the UART interface. There is
however additional signaling between the two modules. This is for the purpose
of auto monitoring of status indicators and control. The pin mapping is shown
below:

| **Function of BG96** | **PIN definition on<br>nRF52840** | 
| ---- | ---- | 
| TX of UART | P0.08 (RX for the<br>nRF52840) | 
| RX of UART | P0.06 (TX for the<br>nRF52840) | 
| BG96_CTS | P0.11 | 
| BG96_RTS | P0.07 | 
| BG96_RI | P0.27 | 
| BG96_STATUS | P0.31 | 
| BG96_RESET | P0.28 | 
| BG96_PWRKEY | P0.02 | 
| BG96_WDISABLE | P0.29 | 
| BG96_DTR | P0.26 | 
| BG96_AP READY | P0.30 | 
| BG96_PSM | P0.03 | 


If BG96_RESET, BG96_PWRKEY, and BG96_WDISABLE are not set correctly, the BG96 module will not boot up normally. When powering up, the BG96 RESET should be retained at a
low-level voltage, the BG96_WDISABLE should be retained at low level voltage,
and the BG96_PWRKEY should be given a pulse with a high level and at least
100ms width in order to turn the BG96 normally.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1567035131\/18930\/ggm40nnrzjsshxdfdugz.jpg",
        "mode": "responsive",
        "width": 624,
        "height": 266,
        "caption": "**Figure 3**: Turning on the BG96 via the PWRKEY"
    }
}]$

### Antenna RF Interface

The connectors for
both the GPS and LTE antennas are iPEX.

Make sure that the
LTE antenna is tuned to work at the operational frequency of your LTE provider,
corresponding to your region.

