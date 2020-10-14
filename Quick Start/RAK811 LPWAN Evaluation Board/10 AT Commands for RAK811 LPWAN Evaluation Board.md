---
type: page
title: AT Commands for RAK811 LPWAN Evaluation Board
listed: true
slug: configuring-your-rak811-evaluation-board
---published

The purpose of this document is to demonstrate on how to configure the RAK811 LPWAN Evaluation Board thru the use of AT Commands via a **Serial Port Tool** running in your Windows PC. The list below shows the AT Commands available for use:

| **AT Command** | **Description** | 
| ---- | ---- | 
| at+help | This AT command can show all available AT<br>commands of this module/product for you | 
| at+version | Get the current firmware version number. | 
| at+get_config=device:status | Get all information about the device’s hardware components and their current status. | 
| at+set_config=device:restart | After set, the device will restart. | 
| at+set_config=device:boot | Lets the device work in boot mode | 
| at+run | Stop boot mode and run as normal. Only valid when the device works in boot mode. | 
| at+set_config=device:sleep:**X** | After setting, the device will go to sleep mode or wake up immediately.<br><br>• **0** - wake up<br><br>• **1** - sleep | 
| at+set_config=device:gpio:**X**:**Y** | Set a certain GPIO pin to high/low level. <br><br>• **X** - the pin number of a certain<br>GPIO on RAK811 module.<br><br>• **Y** - **0**: low level, **1**: high level. | 
| at+get_config=device:gpio:**X** | Get a certain GPIO’s level. <br><br>• **X** -the pin number of the GPIO on<br>RAK811 module. | 
| at+get_config=device:adc:**X** | Get the ADC value. <br><br>• **X** - the pin number of the ADC on<br>RAK811 module. | 
| at+set_config=device:iic:**X**:**YY**:**ZZ**:**A AA** | Read data from I2C or write a data to I2C. <br><br>• **X** - **0**: read, **1**: write. <br><br>• **YY** - device address, in HEX<br>format.<br><br>• **ZZ** - sensor’s register address, in<br>HEX format.<br><br>• **AAA** - if read, this parameter<br>means the length you want to read. If write,<br>this parameter means the data you want to<br>write. It must be in HEX format too. | 
| at+set_config=device:uart_mode:**X**:<br>**Y** | Set the UART work mode. <br><br>Parameters<br><br>• **X** - UART number on RAK811<br>module. <br><br>• **Y** -  **1**: Passthrough mode.<br><br>**Note:** If you want to go back to configuration mode, enter `+++`in the serial port. | 
| at+set_config=device:uart:**X**:**Y** | Set a certain UART’s Baud rate. <br><br>• **X -** the UART number<br><br>• **Y -** the Baud rate value. | 
| at+send=uart:**X**:**YYY** | Send data through UART. <br><br>• **X** - the UART number of RAK811<br>module <br><br>• **YYY** - the data you want to send<br>through UART | 
| at+join | Start LoRa® Network join procedure. | 
| at+send=lora:**X**:**YYY** | Send a customized data.<br><br>• **X** - LoRa® port<br><br>• **YYY** - the data which you want to send. The limited length is 50 Bytes, and the data must be in HEX format. | 
| at+set_config=lora:work_mode:**X** | Set the work mode for LoRa®. <br><br>• **X** - **0**: LoRaWAN®, **1**: LoRaP2P, **2**: Test Mode. | 
| at+set_config=lora:join_mode:**X** | Set the join mode for LoRaWAN®.<br><br>• **X** - **0**: OTAA, **1**: ABP | 
| at+set_config=lora:class:**X** | Set the class for LoRa®.<br><br>• **X** - **0**: Class A, **1**: Class B, **2**: Class C | 
| at+set_config=lora:region:**XXX** | Set the region for LoRa®.<br><br>• **XXX** - one of the following items: EU868 EU433, CN470, IN865, EU868, AU915, US915, KR920, AS923. | 
| at+set_config=lora:confirm:**X** | Set the type of messages which will be sent out through LoRa®.<br><br>• **X** - **0**: unconfirm, **1**: confirm | 
| at+set_config=lora:dev_eui:**XXXX** | Set the device EUI for OTAA.<br><br>• **XXXX** - the device EUI. | 
| at+set_config=lora:app_eui:**XXXX** | Set the application EUI for OTAA.<br><br>• **XXXX** - the application EUI. | 
| at+set_config=lora:app_key:**XXXX** | Set the application key for OTAA.<br><br>• **XXXX** - the application key. | 
| at+set_config=lora:dev_addr:**XXXX** | Set the device address for ABP.<br><br>• **XXXX** - the device address. | 
| at+set_config=lora:apps_key:**XXXX** | Set the application session key for ABP.<br><br>• **XXXX -** the application session key. | 
| at+set_config=lora:nwks_key:**XXXX** | Set the network session key for ABP.<br><br>• **XXXX** - the network session key. | 
| at+set_config=lora:ch_mask:**X:Y** | Set a certain channel on or off.<br><br>• **X -** the channel number, and you can check which channel can be set before you set it.<br><br>• **Y** - **0**: off, **1**: on | 
| at+set_config=lora:adr:**X** | Open or close the ADR function of LoRa® Node. <br><br>• **X - 0**: Close ADR; **1**: Open ADR. | 
| at+set_config=lora:dr:**X** | Set the DR of LoRa® Node.<br><br>• **X** - the number of DR. Generally, the value of X can be 0~5. More details, please check the LoRaWAN® 1.0.2 specification. | 
| at+set_config=lora:tx_power:**X** | Set the TX power level. <br><br>• **X** - The level of TX power. If you<br>want to know the relationship between TX<br>power level and dbm, please have a look at<br>LoRaWAN® 1.0.2 region specification on this [link](https://github.com/RAKWireless/Update-File/blob/master/LoRaWANRegionalParametersv1.0.2.pdf). | 
| at+get_config=lora:status | It will return all of the current information of LoRa®, except LoRa® channel. | 
| at+get_config=lora:channel | It will return the state of all LoRa® channels, then you can see which channel is closed and which channel is open very clearly. | 
| at+set_config=lorap2p:**XXX**:**Y**:**Z**:**A**:**B**:<br>**C** | Set the parameters for LoRa® P2P mode. This AT command is valid when the work<br>mode is ·LoRa® P2P.<br><br>• **XXX** - Frequency in Hz.<br><br>• **Y** - Spreading factor, [6, 7, 8, 9, 10, 11, 12].<br><br>• **Z** - Bandwidth, <br>                                                 **0**: 125 kHz,                                                                                     **1**: 250 kHz,                                                                                     **2**: 500kHz.<br><br>• **A** - Coding Rate, <br>                                                 **1**: 4/5, <br>                                                 **2**: 4/6, <br>                                                 **3**: 4/7, <br>                                                 **4**: 4/8. <br><br>• **B** - Preamble Length, 5-65535. <br><br>• **C** - Power in dbm, 5-20. | 
| at+send=lorap2p:**XXX** | Send data through LoRaP2P. This AT command is valid when it works in LoRaP2P mode.<br><br>• **XXX** - Data in HEX | 


