---
type: page
title: Configure RAK7431 Working Modes
listed: true
slug: configure-rak7431-working-modes
---published

### Data Transparent Mode

When the RS485 data interface works in Modbus mode, the data encapsulation format can be divided into two types: **transparent mode** and **non-transparent mode.**

- In **transparent mode**, the Modbus execution instruction response data (data, received by the node) will be directly forwarded through the LoRaWAN network.
- In the **non-transparent mode**, the Modbus execution instruction response data (data, received by the node) will be encapsulated in the message header according to the Modbus protocol, and then transmitted to the server through LoRaWAN.

$plugin[{
    "type": "callout",
    "data": {
        "text": "The non-transparent mode is the default one.",
        "type": "info",
        "title": "Note:"
    }
}]$

Enter the following AT command in the RAK Serial Tool to change the mode:

$plugin[{
    "type": "code-block",
    "data": {
        "languageBlocks": [
            {
                "code": "AT+TRANSPARENT=n",
                "language": "none"
            }
        ]
    }
}]$

| **n** | **Condition** | 
| ---- | ---- | 
| 0 | transparent mode is turned off | 
| 1 | it is turned on | 


$plugin[{
    "type": "callout",
    "data": {
        "text": "The change takes effect immediately after modification.",
        "type": "info",
        "title": "Note:"
    }
}]$

### Scheduled Polling Function

When the device works in MODBUS mode, it supports the scheduled polling function.

This means that the device will perform a polling operation every given period (polling cycle). During polling, the device will send the pre-added MODBUS instructions in turn and forward the corresponding response data through the LoRaWAN network. 

The device turns on the scheduled polling by default. The AT command for this is:

$plugin[{
    "type": "code-block",
    "data": {
        "languageBlocks": [
            {
                "code": "AT+ENABLEPOLL=n",
                "language": "none"
            }
        ]
    }
}]$

| **n** | **Condition** | 
| ---- | ---- | 
| 0 | turns scheduled polling off | 
| 1 | turns it on | 


$plugin[{
    "type": "callout",
    "data": {
        "text": "The modification takes effect after restart.",
        "type": "info",
        "title": "Note:"
    }
}]$

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1597147438\/41815\/i6ovapldosrez1frvkw5.png",
        "mode": "responsive",
        "width": 1141,
        "height": 446,
        "caption": "**Figure 1**: Scheduled polling example"
    }
}]$

### Scheduled Polling Cycle

This command sets/reads the scheduled polling cycle. This command only works if scheduled polling is enabled. The modification takes effect after the next polling cycle or a restart.

**Example**: To set the polling cycle to 60 seconds, use this command:

$plugin[{
    "type": "code-block",
    "data": {
        "languageBlocks": [
            {
                "code": "AT+POLLPERIOD=60",
                "language": "none"
            }
        ]
    }
}]$

RAK7431 supports polling mode, which stores up to 32 query instructions at a maximum length of 128 bytes per instruction. Polling intervals and wait times can be adjusted as needed. RAK7431 converts the data returned by the RS485 node into a LoRaWAN message, which can be sent to the LoRaWAN gateway as is or encapsulated. In transparent mode, the data for the RS485 is sent in the payload of the LoRa message as is, and in non-transparent mode, the data of RS485 is encapsulated in the LoRa message with a header and validation.

### Add Polling Instructions

To add polling instruction, execute the AT command:

$plugin[{
    "type": "code-block",
    "data": {
        "languageBlocks": [
            {
                "code": "AT+ADDPOLL=<n>:<xxxx>",
                "language": "none"
            }
        ]
    }
}]$

| **Parameter** | **Description** | **Value Range** | 
| ---- | ---- | ---- | 
| n | polling instruction ID | 1 to 127 | 
| xxxx | polling instruction content; hexadecimal string | 128 bytes max | 


According to the temperature and humidity register address of the temperature and humidity sensor in the example and the RS485 address, the polling instruction should be:

$plugin[{
    "type": "code-block",
    "data": {
        "languageBlocks": [
            {
                "code": "AT+ADDPOLL=1:010300000002C40B",
                "language": "none"
            }
        ]
    }
}]$

**Example**: If you have added multiple RS485 temperature and humidity sensors, continue to increase the polling instructions based on the RS485 address and register address, for example:

- RS485 Temperature and humidity sensor addr: 01, Polling 1: 010300000002C40B
- RS485 Temperature and humidity sensor addr: 04, Polling 2: 040300000002C45E
- RS485 Temperature and humidity sensor addr: 08, Polling 3: 080300000002C492
- RS485 Temperature and humidity sensor addr: 0F, Polling 4: 0F0300000002C525

You will need to increase the polling instruction by the following AT commands:

$plugin[{
    "type": "code-block",
    "data": {
        "languageBlocks": [
            {
                "code": "AT+ADDPOLL=1:010300000002C40B",
                "language": "none"
            }
        ]
    }
}]$

$plugin[{
    "type": "code-block",
    "data": {
        "languageBlocks": [
            {
                "code": "AT+ADDPOLL=2:040300000002C45E",
                "language": "none"
            }
        ]
    }
}]$

$plugin[{
    "type": "code-block",
    "data": {
        "languageBlocks": [
            {
                "code": "AT+ADDPOLL=3:080300000002C492",
                "language": "none"
            }
        ]
    }
}]$

$plugin[{
    "type": "code-block",
    "data": {
        "languageBlocks": [
            {
                "code": "AT+ADDPOLL=4:0F0300000002C525",
                "language": "none"
            }
        ]
    }
}]$

The RAK7431 sends an instruction to the sensor every 1 minute to obtain temperature and humidity data, and the following is the result of 3 consecutive scheduled polls:

- **DTU Tx**: The polling instruction sent to the Sensors over RS485 Data Interface
- **DTU Rx**: The sensor data received.
- **LoRa Tx**：Send the received data through a LoRaWAN network.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1597151746\/41815\/ewu31bh8cx4j0rnwohyl.jpg",
        "mode": "600",
        "width": 664,
        "height": 850,
        "caption": "**Figure 2**: Data in transparent mode"
    }
}]$

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1597151780\/41815\/kvtlpuirk8qmmrpjzzma.jpg",
        "mode": "600",
        "width": 664,
        "height": 850,
        "caption": "**Figure 3**: Data in non-transparent mode"
    }
}]$

- **Humidity calculation**: hex is 0210, the decimal is 528, converted humidity is 52.8% RH. 
- **Temperature calculation**: hex is 012F, the decimal is 303, converted temperature is 30.3 ℃.

