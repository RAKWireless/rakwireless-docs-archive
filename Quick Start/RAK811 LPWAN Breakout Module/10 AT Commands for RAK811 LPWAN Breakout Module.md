---
type: page
title: AT Commands for RAK811 LPWAN Breakout Module
listed: true
slug: configuring-your-rak811-breakout-board
---published

The purpose of this section is to demonstrate on how to configure the RAK811 through the use of AT Commands via a Serial Port Tool running in your Windows PC. The list below shows the AT Commands available for use:

| **AT Command** | **Description** | 
| ---- | ---- | 
| at+version | Get the current firmware version number. | 
| at+get_config=device:status | Get all information about the device’s<br>hardware components and their current<br>status. | 
| at+set_config=device:restart | After set, the device will restart. | 
| at+set_config=device:boot | Let the device work in boot mode | 
| at+run | Stop boot mode and run as normal. It is<br>valid when the device works in boot mode. | 
| at+set_config=device:sleep:X | After setting, the device will go to sleep<br>mode or wake up immediately. <br><br>• **0** - sleep <br><br>• **1** - wake up | 
| at+join | Start to join LoRa® network | 
| at+send=lora:**X**:**YYY** | Send a customized data. <br><br>• **X -** LoRa® port <br><br>• **YYY -** the data which you want to send. The limited length is 50 Bytes, and the data must be in HEX format. | 
| at+set_config=lora:work_mode:**X** | Set the work mode for LoRa®. <br><br>• **X** - 0: LoRaWAN®, 1: LoRaP2P, 2: Test Mode. | 
| at+set_config=lora:join_mode:**X** | Set the join mode for LoRaWAN®. <br><br>• **X** - 0: OTAA, 1: ABP | 
| at+set_config=lora:class:**X** | Set the class for LoRa®. <br><br>• **X** - 0: Class A, 1: Class B, 2: Class C | 
| at+set_config=lora:region:**XXX** | Set the region for LoRa®. <br><br>• **XXX -** one of the following items: EU868 EU433, CN470, IN865, EU868, AU915, US915, KR920, AS923. | 
| at+set_config=lora:confirm:**X** | Set the type of messages which will be sent out through LoRa®. <br><br>• **X** - 0: unconfirm, 1: confirm | 
| at+set_config=lora:dev_eui:**XXXX** | Set the device EUI for OTAA. <br><br>• **XXXX** - the device EUI. | 
| at+set_config=lora:app_eui:**XXXX** | Set the application EUI for OTAA. <br><br>• **XXXX -** the application EUI. | 
| at+set_config=lora:app_key:**XXXX** | Set the application key for OTAA.<br><br>• **XXXX -** the application key. | 
| at+set_config=lora:dev_addr:**XXXX** | Set the device address for ABP.<br><br>• **XXXX -** the device address. | 
| at+set_config=lora:apps_key:**XXXX** | Set the application session key for ABP. <br><br>• **XXXX -** the application session<br>key. | 
| at+set_config=lora:nwks_key:**XXXX** | Set the network session key for ABP. <br><br>• **XXXX** - the network session key. | 
| at+set_config=lora:ch_mask:**X**:**Y** | Set a certain channel on or off. <br><br>• **X -** the channel number, and you<br>can check which channel can be set before<br>you set it.<br><br>• **Y** - 0: off, 1: on | 
| at+set_config=lora:adr:**X** | Open or close the ADR function of the Node.<br><br>• **X -** 0: Close ADR; 1: Open ADR. | 
| at+set_config=lora:dr:**X** | Set the DR of the Node.<br><br>• **X** - the number of DR. Generally,<br>the value of X can be 0~5. More details, please check the LoRaWAN® 1.0.2<br>specification. | 
| at+get_config=lora:channel | It will return the state of all LoRa® channels,<br>then you can see which channel is closed<br>and which channel is open very clearly | 
| at+set_config=lorap2p:**XXX**:**Y**:**Z**:**A**:**B**:<br>**C** | Set the parameters for LoRa® P2P mode. This AT command is valid when the work<br>mode is ·LoRaP2P. <br><br>• **XXX -** Frequency in Hz. <br><br>• **Y -** Spreading factor, [6, 7, 8, 9, 10, 11, 12]. <br><br>• **Z** - Bandwidth, **0**: 125 kHz, **1**: 250 kHz, **2**: 500kHz.<br><br>• **A** - Coding Rate, **1**: 4/5, **2**: 4/6, **3**: 4/7, **4**: 4/8.<br><br>• **B -** Preamble Length, 5-65535. <br><br>• **C -** Power in dbm, 5-20. | 
| at+send=lorap2p:**XXX** | Send data through LoRaP2P. This AT<br>command is valid when it works in LoRaP2P<br>mode. <br><br>• **XXX -** the data in HEX. | 


