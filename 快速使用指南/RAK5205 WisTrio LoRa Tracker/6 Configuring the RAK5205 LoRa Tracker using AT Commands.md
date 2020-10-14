---
type: page
title: Configuring the RAK5205 LoRa Tracker using AT Commands
listed: true
slug: configuring-the-rak5205-lora-tracker-using-at-commands
---published

You can configure your LoRa Tracker by sending AT Commands via a Serial port tool running on your PC. The following list shows the AT Commands that you can use:

| AT Command | Description | 
| ---- | ---- | 
| at+dev_eui=XXXXXXXX | Set the Device EUI | 
| at+app_eui=XXXXXXXX | Set the Application EUI | 
| at+app_key=XXXXXXXXXXXXXXXX | Set the Application Key | 
| at+dev_addr=XXXX | Set the Device Address, only for ABP mode | 
| at+nwks_key=XXXXXXXXXXXXXXXX | Set the Network Session Key, only for ABP mode | 
| at+apps_key=XXXXXXXXXXXXXXXX | Set the Application Session Key, only for ABP mode | 
| at+join_mode=otaa | Set the Activation Method to OTAA | 
| at+join_mode=abp | Set the Activation Method to ABP | 
| at+region=EU868 | Set the Region, which you want the LoRa Button to work in. EU868  is just an example. You can set it to AS920, AS923, US915, AU915, KR920, or IN865 when you are using a "HF" (High Frequency) Firmware. You can also set it to EU433 or CN470 when you are using a "LF" (Low Frequency) Firmware. | 
| at+app_interval=120 | Set the data transmission interval (60 - 86400 seconds) | 
| at+gps_stime=60 | Set the GPS Location acquisition wait time (30 - 600 seconds) | 
| at+msg_confirm=0 | Set Message Confirm (0 : unconfirmed , 1 : confirm) | 
| at+ps=1 | Set Power Save mode (0 : off , 1 : on) | 


