---
type: page
title: AT Commands for RAK7200 LPWAN Tracker
listed: true
slug: configuring-the-rak7200-lora-tracker-using-at-commands
---published

You can configure your LPWAN Tracker by sending AT Commands via a Serial port tool running on your PC. The following list shows the AT Commands that you can use:

| **AT Command** | **Description** | 
| ---- | ---- | 
| at+help | Get all available AT Commands | 
| at+version | Get the current firmware version number | 
| at+get_config=device:status | Get all information about the device’s hardware components and their current status. | 
| at+set_config=device:restart | Restart the Device | 
| at+set_config=device:boot | Set the device in Boot mode | 
| at+run | Stop Boot Mode and run as normal. Valid only when the device works in boot mode. | 
| at+set_config=device:sleep:**X** | After Setting, the device will go to sleep mode or wake up immediately<br><br>• **0 -** Wake Up<br><br>• **1 -** Sleep | 
| at+join | Start the join procedure for the LoRaWAN® network | 
| at+send=lora:**X**:**Y** | Send an uplink with a custom payload:<br><br>• **X** - LoRa® Frame Port <br><br>• **Y** - The data which you want to send. (Length limit is 50 bytes and the data must be in Hex Format) | 
| at+set_config=lora:work_mode:**X** | Set the Working Mode:<br><br>• **X** - **0**: LoRaWAN®, **1**: LoRaP2P, **2**: Test Mode. | 
| at+set_config=lora:join_mode:**X** | Set the Join Mode: <br><br>• **X** - **0**: OTAA, **1**: ABP | 
| at+set_config=lora:class:**X** | Set the Class for LoRa®. <br><br>• **X** - **0**: Class A, **1**: Class B, **2**: Class C | 
| at+set_config=lora:region:**XXX** | Set the Region for LoRa®<br><br>**XXX -** one of the following items: EU868 EU433, CN470, IN865, EU868, AU915, US915, KR920, AS923. | 
| at+set_config=lora:confirm:**X** | Set the type of messages which will be sent out through LoRa®: <br><br>• **X** - **0**: unconfirm, **1**: confirm | 
| at+set_config=lora:dev_eui:**XXXX** | Set the device EUI for OTAA.<br><br>• **XXXX** - the device EUI. | 
| at+set_config=lora:app _eui:**XXXX** | Set the application EUI for OTAA.<br><br>• **XXXX -** the application EUI. | 
| at+set_config=lora:app_key:**XXXX** | Set the application key for OTAA.<br><br>• **XXXX -** the application key. | 
| at+set_config=lora:dev_addr:**XXXX** | Set the device address for ABP.<br><br>• **XXXX -** the device address. | 
| at+set_config=lora:nwks_key:**XXXX** | Set the network session key for ABP.<br><br>• **XXXX** - the network session key. | 
| at+set_config=lora:apps_key:**XXXX** | Set the application session key for ABP.<br><br>• **XXXX -** the application session key. | 
| at+set_config=lora:ch_mask:**X**:**Y** | Turn a certain channel on/off<br><br>• **X** - The Channel Number you want to toggle. You can check the channel number using the command : at+get_config=lora:channel <br><br>• **Y** - **0**: off, **1**: on | 
| at+set_config=lora:dr:**X** | Set the DR of the Node<br><br>• **X** - the number of DR. Generally, the value of X can be 0~5. More details, please check the LoRaWAN® 1.0.2 specification. | 
| at+set_config=lora:tx_power:**X** | Set the TX Power Level<br><br>• **X** - The level of TX power. If you want to know the relationship between TX power level and dbm, please have a look at[ LoRaWAN® 1.0.2 region specification ](https://github.com/RAKWireless/Update-File/blob/master/LoRaWANRegionalParametersv1.0.2.pdf) | 
| at+set_config=lora:send_interval:**X**:**Y** | Set the time interval for sending data<br><br>• **X** - Enable/disable sending data in intervals. <br><br>**0**: the device will not send data automatically, <br><br>**1**: the device will send data every Y seconds.<br><br>• **Y** - Interval time in seconds. This parameter is only valid if X is set to 1. | 
| at+get_config=lora:status | It will return all of the current information of LoRa®, except the LoRa® Channel | 
| at+get_config=lora:channel | It will return the state of all LoRa® channels, then you can see which channel is closed and which channel is open very clearly | 
| at+set_config=device:gps:**X** | Turn<br>on or turn off GPS<br><br>• **X** - **0**: close, **1**: open, **2**: sleep, **3**: standby | 
| at+set_config=device:gps_timeout:**X** | Set<br>the timeout of searching GPS satellite<br><br>• **X** - Time in seconds | 


