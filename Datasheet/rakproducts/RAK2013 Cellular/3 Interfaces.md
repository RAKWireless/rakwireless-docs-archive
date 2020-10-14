---
type: page
title: Interfaces
listed: true
slug: interfaces---rak2013-cellular
---published

It is built with **Quectel BG96/EG91/EG95 module** and compatible with **Raspberry Pi HAT**. It provides the following interfaces, headers, jumpers, button and connectors:

- 40-pins Raspberry connector
- Micro USB
- MikroBus connector
- Earphone Jack
- MIC Jack
- Speaker Jack
- Reset Button
- PWRKEY Button
- Nano Sim Card slot
- LEDs
- Reset Button
- USB boot jumper

**IPEX Antenna Connectors:**

- LTE antenna
- GPS/LTE DIV antenna

### Micro-B USB Interface

A Standard Micro-B USB compliant with USB 2.0 standard specification is used to
provide an interface to connect our device to Raspberry Pi or a PC for control of the board and
firmware upgrade. The Micro-B USB pin connection and definition is shown below:

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1563420201\/17667\/l1ti6nit3eivy0tsrz6m.jpg",
        "mode": "responsive",
        "width": 181,
        "height": 75,
        "caption": "**Figure 3:** Micro-B USB Connection"
    }
}]$

| **Pin** | **Description** | 
| ---- | ---- | 
| 1 | USB_VBUS (+5V) | 
| 2 | USB_DM | 
| 3 | USB_DP | 
| 4 | NC | 
| 5 | GND | 


This USB port is connected to the BG96/EG91/EG95 USB interface. The USB
interface is used for AT command communication, data transmission, software
debugging and firmware upgrade.

### LEDs

Three (3) LEDs are used to indicate operating status, here are their functions:

| **LED Color** | **Function** | **LED Status** | **Description** | 
| ---- | ---- | ---- | ---- | 
| **Green** | Power LED | ON | Indicates that the power is good. | 
| **Blue** | Status | ON<br><br>OFF | The module is powered on.<br><br>The module is powered off. | 
| **Red** | NETLIGHT | ON<br><br>OFF | Indicates the module's network activity status.<br><br>Not registered to the network. | 


### RESET Push Button

Reset Push Button is used to reset the BG96/EG91/EG95 module. To reset the module, push the Reset Button for 1 second.

### PWRKEY Push Button

When either of Quectel BG96 / EG91 / EG95 module is in power off mode, it can be turned on to normal mode
by driving the PWRKEY pin to a low level for at least 100 ms. Note that the module is still in power off mode even when plugging in the power socket, thus, press the PWRKEY to power up the module. When the module is in normal mode, it can be turn to power off mode by pressing the PWRKEY button.

### Antenna RF interface

The modules have two RF interfaces for LTE antenna and GPS/LTE DIV antenna over
standard UFL connectors (Hirose U. FL-R-SMT) with a characteristic impedance of
50Ω. The RF ports support both the transmitter and receiver, providing the antenna interface.

