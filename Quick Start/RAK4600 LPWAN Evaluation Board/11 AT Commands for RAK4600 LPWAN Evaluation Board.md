---
type: page
title: AT Commands for RAK4600 LPWAN Evaluation Board
listed: true
slug: at-commands-for-rak4600
---published

The purpose of this document is to demonstrate on how to configure the RAK4600 LPWAN Evaluation Board thru the use of AT Commands via a Serial Port Tool running in your Windows PC. The list below shows the AT Commands available for use:

| **AT Command** | **Description** | 
| ---- | ---- | 
| at+help | This AT command can<br>show all available AT commands of this module/product for you. | 
| at+version | Get the current<br>firmware version number. | 
| at+set_config=device:restart | After set, the device<br>will restart. | 
| at+run | Stop boot mode and<br>run as normal. It is valid when the device works in boot mode. | 
| at+set_config=device:sleep:**X** | After setting, the<br>device will go to sleep mode or wake up<br>immediately. <br><br>• **0** - sleep<br><br>• **1** - wake up | 
| at+join | Start to join LoRa®<br>network. | 
| at+send=lora:**X**:**YYY** | Send a customized data.<br><br>• **X -** LoRa® port<br><br>• **YYY -** the data which you want to send. The limited length is 50 Bytes, and the data must be in HEX format. | 
| at+set_config=lora:work_mode:**X** | Set the work mode for LoRa®.<br><br>• **X** - **0**: LoRaWAN®, **1**: LoRaP2P, **2**: Test Mode. | 
| at+set_config=lora:join_mode:**X** | Set the join mode for<br>LoRaWAN®. <br><br>• **X** - **0**: OTAA, **1**: ABP | 
| at+set_config=lora:class:**X** | Set the class for<br>LoRa®. <br><br>• **X** - **0**: Class A, **1**: Class B, **2**: Class C | 
| at+set_config=lora:region:**XXX** | Set the region for<br>LoRa®. <br><br>• **XXX** -one of the<br>following items: EU868 EU433, CN470,<br>IN865, EU868, AU915, US915, KR920, AS923. | 
| at+set_config=lora:confirm:**X** | Set the type of<br>messages which will be sent out through LoRa®.<br><br>• **X** - **0**: unconfirm, **1**: confirm | 
| at+set_config=lora:dev_eui:**XXXX** | Set the device EUI for OTAA. <br><br>• **XXXX** - the device EUI. | 
| at+set_config=lora:app_eui:**XXXX** | Set the application EUI for OTAA. <br><br>• **XXXX** - the application EUI. | 
| at+set_config=lora:app_key:**XXXX** | Set the application key for OTAA. <br><br>• **XXXX** - the application key. | 
| at+set_config=lora:dev_addr:**XXXX** | Set the device address for ABP. <br><br>• **XXXX** -the device address. | 
| at+set_config=lora:apps_key:**XXXX** | Set the application session<br>key for ABP. <br><br>• **XXXX** - the application session<br>key | 
| at+set_config=lora:nwks_key:**XXXX** | Set the network<br>session key for ABP. <br><br>• **XXXX** - the<br>network session key. | 
| at+set_config=lora:ch_mask:**X**:**Y** | Set a certain channel on or off.<br><br>• **X -** the channel number, and you can check which channel can be set before you set it.<br><br>• **Y** - **0**: off, **1**: on | 
| at+set_config=lora:adr:**X** | Open or close the ADR<br>function of the Node.<br><br>• **X - 0**: Close ADR; **1**: Open ADR. | 
| at+set_config=lora:dr:**X** | Set the DR of the Node.<br><br>• **X** -the<br>number of DR. Generally, the value of X can be 0~5. More details, please check<br>the LoRaWAN® 1.0.2 specification. | 
| at+get_config=lora:status | It will return all of<br>the current information of LoRa®, except LoRa® channel. | 
| at+get_config=lora:channel | It will return the state<br>of all LoRa® channels, then you can see which channel is closed and which<br>channel is open very clearly. | 
| at+set_config=ble:work_mode:**X**:**Y** | Set the work mode for<br>BLE.<br><br>• **X** - **0**: BLE peripheral mode, **1**: BLE central mode, **2**: Beacon scan mode<br><br>• **Y** - **0**: normal range, **1**: BLE long range<br><br>More information about BLE Connection Modes is explained in [auto$](/rak4600-lora-evaluation-board/bluetooth-connection-modes) | 


