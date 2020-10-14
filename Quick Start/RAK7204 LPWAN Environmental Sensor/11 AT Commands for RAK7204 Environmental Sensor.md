---
type: page
title: AT Commands for RAK7204 Environmental Sensor
listed: true
slug: configuring-the-rak7204-environmental-sensor-using-at-commands
---published

You can configure your RAK7204 Environmental Sensor by sending AT Commands via a Serial port tool running on your PC. The following list shows the AT Commands that you can use:

| **AT Command** | **Description** | 
| ---- | ---- | 
| at+version | Get the current<br>firmware version number. | 
| at+get_config=device:status | Get all information<br>about the device’s hardware components and their current status. | 
| at+set_config=device:restart | After set, the device<br>will restart. | 
| at+set_config=device:boot | Let the device work<br>in boot mode. | 
| at+run | Stop boot mode and<br>run as normal. It is valid when the device works in boot mode | 
| at+set_config=device:sleep:**X** | After setting, the<br>device will go to sleep mode or wake up immediately.<br><br>• **0** - Wake Up<br><br>• **1** - Sleep | 
| at+join | Start to join LoRa®<br>network. | 
| at+send=lora:**X**:**YYY** | Send a customized data.<br><br>• **X -** LoRa® Port <br><br>• **YYY -** The data which you want to send. Limited length is 50 bytes in  HEX Format | 
| at+set_config=lora:work_mode:**X** | Set the work mode for LoRa®<br><br>• **X** - **0**: LoRaWAN®, **1**: LoRaP2P, **2**: Test Mode. | 
| at+set_config=lora:join_mode:**X** | Set the Join Mode for LoRaWAN®<br><br>• **X** - **0**: OTAA, **1**: ABP | 
| at+set_config=lora:class:**X** | Set the class for<br>LoRa®<br><br>• **X** - **0**: Class A, **1**: Class B, **2**: Class C | 
| at+set_config=lora:region:**XXX** | Set the region for<br>LoRa®<br><br>• **XXX -** Options : EU868 EU433, CN470,<br>IN865, EU868, AU915, US915, KR920, AS923. | 
| at+set_config=lora:confirm:**X** | Set the type of<br>messages which will be sent out through LoRa®<br><br>• **X** - **0**: unconfirm, **1**: confirm | 
| at+set_config=lora:dev_eui:**XXXX** | Set the device EUI<br>for OTAA<br><br>• **XXXX -**The Device EUI | 
| at+set_config=lora:app_eui:**XXXX** | Set the application<br>EUI for OTAA<br><br>• **XXXX** - The Application EUI | 
| at+set_config=lora:app_key:**XXXX** | Set the application<br>key for OTAA<br><br>• **XXXX** - the<br>application key | 
| at+set_config=lora:dev_addr:**XXXX** | Set the device<br>address for ABP<br><br>• **XXXX** - the<br>device address. | 
| at+set_config=lora:apps_key:**XXXX** | Set the application<br>session key for ABP<br><br>• **XXXX** - the<br>application session key. | 
| at+set_config=lora:nwks_key:**XXXX** | Set the network session key for ABP.<br><br>• **XXXX** - the<br>network session key | 
| at+set_config=lora:ch_mask:**X**:**Y** | Set a certain channel on or off.<br><br>• **X** - the channel number, and you can check which channel can be set before you set it. <br><br>• **Y** - **0**: off, **1**: on | 
| at+set_config=lora:send_interval:**X**:**Y** | Set the interval of sending data.<br><br>• **X** - open or<br>close the interval mechanism of sending data. If X is set to 0, it means the<br>device will not send data automatically. If X is set to 1, it means that the device will send data every **Y** second. <br><br>• **Y -** Interval time in seconds. This parameter is only valid when **X** is set to 1 | 
| at+set_config=lora:adr:**X** | Open or close the ADR function of the Node.<br><br>• **X - 0**: Close ADR; **1**: Open ADR. | 
| at+set_config=lora:dr:**X** | Set the DR of the Node.<br><br>• **X -** the number of DR.<br>Generally, the value of X can be 0~5. More details, please check the LoRaWAN®<br>1.0.2 specifications. | 
| at+get_config=lora:status | Returns all of the current information of LoRa®, except LoRa® channel. | 
| at+get_config=lora:channel | Returns the state of all LoRa®<br>channels, then you can see which channel is closed and which channel is open<br>very clearly. | 
| at+set_config=lorap2p:**XXX**:**Y**:**Z**:**A**:**B**:**C** | Set the parameters for LoRa® P2P mode. This AT command is valid when the work mode is LoRa®P2P. <br><br>• **XXX -** Frequency (Hz)<br><br>• **Y -** Spreading Factor [6,7,8,9,10,11,12] <br><br>• **Z** - Bandwidth, **0**: 125 kHz, **1**: 250 kHz, **2**: 500kHz.<br><br>• **A** - Coding Rate, **1**: 4/5, **2**: 4/6, **3**: 4/7, **4**: 4/8.<br><br>• **B -** Preamble Length: 5-65535 <br><br>• **C -** Power in  dbm , 5-20 | 
| at+send=lorap2p:**XXX** | Send data through LoRaP2P. This AT command is valid when it works in LoRaP2P mode.<br><br>• **XXX -** Data in HEX Format | 


