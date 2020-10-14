---
type: page
title: Configuring your RAK811 WisNode LoRa
listed: true
slug: configuring-your-rak811-wisnode-lora
---published

You can configure your RAK811 WisNode LoRa Module by sending AT commands into it from a serial port tool running on your PC.

The following list shows the AT commands with the description:

| AT Command | Description | 
| ---- | ---- | 
| at+version | Get the current firmware version number. | 
| at+get_config=device:status | Get all information about the device’s hardware components and their current status. | 
| at+set_config=device:restart | After set, the device will restart. | 
| at+set_config=device:boot | Let the device work in boot mode | 
| at+run | Stop boot mode and run as normal. It is valid when the device works in boot mode. | 
| at+set_config=device:sleep:X | After setting, the device will go to sleep mode or wake up immediately. X definition: 0: sleep, 1: wake up | 
| at+join | Start LoRa Network join procedure. | 
| at+send=lora:X:YYY | Send customized data.&nbsp;X definition: LoRa frame port&nbsp;YYY definition: the data, which you want to&nbsp;send. The length limit is 50 Bytes and the data must be in HEX format. | 
| at+set_config=lora:work&nbsp;mode:X | Set the work mode for LoRa.&nbsp;X definition: 0: LoRaWAN, 1: LoRaP2P, 2:&nbsp;Test Mode. | 
| at+set_config=lora:join_mode:X | Set the join mode for LoRaWAN.&nbsp;X definition: 0: OTAA, 1: ABP | 
| at+set_config=lora:class:X | Set the class for LoRa.X definition: 0: Class A, 1: Class B, 2: Class C | 
| at+set_config=lora:region:XXX | Set the region for LoRa.XXX define: one of the following items:&nbsp;EU868 EU433, CN470, IN865, EU868,&nbsp;AU915, US915, KR920, AS923. | 
| at+set_config=lora:confirm:X | Set the type of messages which will be sent&nbsp;out through LoRa.X definition: 0: unconfirmed, 1: confirmed | 
| at+set_config=lora:dev_eui:XXXX | Set the device EUI for OTAA.XXXX definition: the device EUI. | 
| at+set_config=lora:app_eui:XXXX | Set the application EUI for OTAA.XXXX definition: the application EUI. | 
| at+set_config=lora:app_key:XXXX | Set the application key for OTAA.XXXX definition: the application key. | 
| at+set_config=lora:dev_addr:XXXX | Set the device address for ABP.XXXX definition: the device address. | 
| at+set_config=lora:apps_key:XXXX | Set the application session key for ABP.XXXX definition: the application session&nbsp;key. | 
| at+set_config=lora:nwks_key:XXXX | Set the network session key for ABP.XXXX definition: the network session key. | 
| at+set_config=lora:ch_mask:X:Y | Set a certain channel on or off.X definition: the channel number, and you&nbsp;can check which channel can be set before&nbsp;you set it.Y definition: 0: off, 1: on | 
| at+get_config=lora:status | It will return all of the current information of&nbsp;LoRa, except LoRa channel. | 
| at+get_config=lora:channel | It will return the state of all LoRa channels,&nbsp;then you can see which channel is closed&nbsp;and which channel is open very clearly. | 


