---
type: page
title: Hardware FAQs
listed: true
slug: hardware
---published

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1572527033\/21831\/jivk45ocedlms0ylv5nv.png",
        "mode": "600",
        "width": 1626,
        "height": 880,
        "caption": null
    }
}]$

### 1. Can we develop our own Applications in RAK’s LoRawan modules?

**Answer:** Yes, With the newly released RAK RUI API, it is now possible to connect specific sensors in your device. You will be able to customize your own firmware for your specific needs whether be a project or even as a hobby. For more information about RAK RUI API, check out this [Guide](https://doc.rakwireless.com/developer-tools/developer-tools/getting-started) . You can also check out this sample **[Firmware Customizing](https://doc.rakwireless.com/rak7204-lora-environmental-sensor/firmware-customizing)** guide on how to upload your firmware to your device.

### 2. What are the external interfaces in RAK5205 Wistrio LoRa Tracker? What are the frequency bands that it supports?and how many GPIOs are there?

**Answer:** The RAK5205 LoRa tracker board is built on the Semtech SX1276 chip, with the STM32L1 MCU at its core. It  supports **I2C, GPIOs, UART and ADC interfaces. The board supports all LoRaWAN frequency channels** (EU433, EU868, CN470 , US915, AS920, AS923, AU915, KR920, IN865)  which is easy to configure while building the firmware from the source code The RAK5205 has 7 GPIOs labeled as PA8, PB3, PB5, SWD_TMS, SWD_ CLK, LED1_PA12 and LED2_PB4. For a full overview of the pinout diagram of the device you can check the datasheet [here](https://doc.rakwireless.com/datasheet/rakproducts/pin-definition---rak5205)

### 3. What are the frequencies supported by RAK Gateways?

**Answer:** RAK Gateways support all LoRaWAN frequency channels as shown in the list provided below: 

- EU433
- CN470
- IN865
- EU868
- AU915
- US915
- AS920
- KR920
- AS923

### 4. Will the RAK2245 Pi Hat work with the newly released Raspberry Pi 4?

**Answer:** Yes. We have provided a pre-compiled firmware image that you can just easily use and flash it into your Raspberry Pi 4. You can check out the [**RAK2245 - Pi Hat Device Firmware Setup**](https://doc.rakwireless.com/rak2245-pi-hat/device-firmware-setup) guide on how to burn the firmware image into your raspberry pi device.

$plugin[{
    "type": "callout",
    "data": {
        "text": "Please use the official **USB-C Power supply** in order for you not to encounter some power issues.",
        "type": "warning",
        "title": "Note"
    }
}]$

### 5. What is the range that I can achieve with LoRa?

**Answer:** Technically one can achieve with a range of 10-15km but there are a lot of factors that one should consider like placement of gateway, type of antenna used, message payload, physical obstructions and many more. In Rakwireless, we have obtained with a range of **20km** through the use of the **RAK7249 Macro Outdoor Gateway.** To learn more about the actual testing, click [here](https://downloads.rakwireless.com/en/LoRa/DIY-Gateway-RAK7249/Application-Notes/RAKwireless_LoRAWAN_Coverage_Drive_Test_Report.pdf).

### 6. What is the meaning of the LED of the RAK612 LoRa Button?

**Answer**: Whenever the keys 1 - 4 is pressed, the corresponding basket light under each key lights up for 300ms.

$plugin[{
    "type": "callout",
    "data": {
        "text": "To enter Configuration Mode, long press Key 1 for at least 500ms. Press Key 1 again for at least 500ms to exit Configuration Mode.",
        "type": "info",
        "title": "Note:"
    }
}]$

| **Mode** | **Red LED** | **Green LED** | **Blue LED** | 
| ---- | ---- | ---- | ---- | 
| Configuration Mode | Steady ON | OFF | OFF | 
| Transmission Successful | ON | OFF | Flash Twice after Red LED | 
| Transmission Fail | Flash Twice | OFF | OFF | 
| USB Cable Plugged | OFF | ON | OFF | 


### 7. What is the average power consumption of the RAK7249 Macro Outdoor Gateway with LTE working for both 8-channel and 16-channel LoRa?

$plugin[{
    "type": "callout",
    "data": {
        "text": "To attain such test condition, settings must be followed below:\n\n- **GPS and Wi-Fi**: Disabled\n- **4G and LoRa**: Enabled",
        "type": "info",
        "title": "Note:"
    }
}]$

**At 8-Channels Working**

- 12V DC Power Supply-Average Power: 12 Volts x 0.32 Amperes = 8.84 Watts
- PoE 48V Power Supply-Average Power: 48 Volts x 0.1 Amperes = 4.8 Watts

**At 16-Channels Working**

- 12V DC Power Supply-Average Power: 12 Volts x 0.46 Amperes = 5.52 Watts
- PoE 48V Power Supply-Average Power: 48 Volts x 0.13 Amperes = 6.24 Watts

### 8. How many LoRa®  modules does RAK currently have? What are the features of each module?

> **Answer**: The following are the available modules: RAK4200, RAK4270, RAK4600, RAK4260, RAK811, RAK2200 several modules with RAK4200 and RAK811 are of high and low frequency.

The features of each module are shown in the following table:

| **Module Name** | **RAK4200** | **RAK4270** | **RAK4600** | **RAK4260** | **RAK811** | **RAK2200** | 
| ---- | ---- | ---- | ---- | ---- | ---- | ---- | 
| MCU | STM32L071KB | STM32L071KB | nRF52832 | ATSAMR34J18B | STM32L151CBU6 | N/A | 
| LoRa Chip | SX1276 | SX1262 | SX1276 | Integrated in the ATSAMR34J18B chip | SX1276 | SX1276 | 
| 32M TCXO | Not supported | Not supported | Not supported | Supported | Supported | Supported | 
| Support Mode | - PA_BOOST mode<br>- Receive mode | - PA_BOOST mode<br>- Receive mode | - PA_BOOST mode<br>- Receive mode | - PA_BOOST mode<br>- RFO_HF mode<br>- Receive mode | - PA_BOOST mode<br>- RFO_HF mode<br>- Receive mode | - PA_BOOST mode<br>- RFO_HF mode<br>- Receive mode | 
| TX Power | 19dB max @PA_BOOST | 22dB max@PA_BOOST | 20dB max @PA_BOOST<br><br>-20~4dB@BT | 20dB max @PA_BOOST<br><br>14dB max @RFO_HF mode | 20dB max @PA_BOOST<br><br>14dB max @RFO_HF mode | 20dB max @PA_BOOST<br><br>14dB max @RFO_HF mode | 
| LoRa® Frequency Range | RAK4200H:<br>863MHz to 923MHz<br><br>RAK4200L:<br>433MHz to 510MHz | RAK4270H:<br>863MHz to 923MHz | RAK4600H:<br>863MHz to 923MHz | RAK4260H:<br>863MHz to 923MHz | RAK811H:<br>863MHz to 923MHz<br><br>RAK811L:<br>433MHz to 510MHz | RAK2200H:<br>863MHz to 923MHz | 
| Form Factor | 15x15.5x2.5mm | 15x15.5x2.5mm | 15x23x2.5mm | 15x15x1.8mm | 22x14x1.7mm | 15x15 x 2.0 mm | 
| I/O ports | - 2x UART interfaces<br>- 1x I2C interface<br>- 1x SWD interface<br>- 2x GPIOs | - 2x UART interfaces<br>- 1x I2C interface<br>- 1x SWD interface<br>- 4x GPIOs | - 2x UART interfaces<br>- 1x I2C interface<br>- 1x SWD interface<br>- 1x NFC interface<br>- 2x GPIOs | - 2x UART interfaces<br>- 1x I2C interface<br>- 1x SWD interface<br>- 1x SPI interface<br>- 1x USB interface<br>- 3x ADCs<br>- 3x GPIOs<br>- 2x PTCs | - 2x UART interfaces<br>- 1x I2C interface<br>- 6x ADCs<br>- 8x GPIOs | N/A | 
| Receive Current | 15mA @ lora receive | 15mA @ lora receive | 17mA@lora receive mode<br><br>11.5mA@BT receice | 13.6mA@ lora receive | 16mA @ lora receive | 11.5mA@ lora receive | 
| Tx current | 124mA@Lora PA_BOOST | 124mA@Lora PA_BOOST | 125mA@Lora PA_BOOST&BT sleep<br><br>9mA@BT tx&lora sleep | 126mA@PA_BOOST@20dB<br><br>33mA@RFO@14dB | 126mA@PA_BOOST@20dB<br><br>33mA@RFO@14dB | 120mA@PA_BOOST@20dB<br><br>29mA@RFO@13dB | 
| Sleep Current | 1.5uA | 1.5uA | 2.0uA | 860nA | 10uA | 1uA | 
| Supply Voltage | 2.0 - 3.6V | 2.0 - 3.6V | 2.0 - 3.6V | 1.8V - 3.6V | 3V - 3.45V | 2.0 - 3.6V | 
| RF port | with Ipex | without Ipex | lora with Ipex<br><br>BT with ipex | Stamp pinout without Ipex | Stamp pinout without Ipex | Stamp pinout without Ipex | 
| Pin Count | 20 | 20 | 42 | 36 | 34 | 24 | 
| Program Tool | J-link | J-link | J-link | J-link | UART | N/A | 


### 9. What is the difference between all Raspberry Pi based LoRaWAN**™** Gateways that RAK currently offers?

**Answer:** Currently, RAKwireless offers 4 Raspberry Pi Based LoRaWAN Gateways namely RAK7246G, RAK7246, RAK7243 and RAK7244.

|  | **RAK7246** | **RAK7246G** | **RAK7243** | **RAK7244** | 
| ---- | ---- | ---- | ---- | ---- | 
| **Platform** | Raspberry Pi Zero W | Raspberry Pi Zero W | Raspberry Pi 3B+ | Raspberry Pi 4 | 
| **LoRa Concentrator Chip** | SX1308 | SX1308 | SX1301 | SX1301 | 
| **Tx Power** | 20dbm | 20dbm | 27dBm | 27dBm | 
| **Rx Sensitivity** | -139dbm @ SF12 at 125kHz | -139dbm @ SF12 at 125kHz | -139dbm @ SF12 at 125kHz | -139dbm @ SF12 at 125kHz | 
| **GPS** | N/A | Ublox MAX-7Q | Ublox MAX-7Q | Ublox MAX-7Q | 
| **Enclosure** | Acrylic | Acrylic | Metal | Metal | 
| **Cost** | $99 | $114 | $199 | $212 | 
| **Target Use Case** | Development Platform in Lab | Development Platform in Lab | Development and Real Deployment | Development and Real Deployment | 


