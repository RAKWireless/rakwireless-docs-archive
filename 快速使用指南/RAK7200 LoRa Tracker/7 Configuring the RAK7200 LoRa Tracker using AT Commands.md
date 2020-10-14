---
type: page
title: Configuring the RAK7200 LoRa Tracker using AT Commands
listed: true
slug: configuring-the-rak7200-lora-tracker-using-at-commands
---published

You can configure your LoRa Tracker by sending AT Commands via a Serial port tool running on your PC. The following list shows the AT Commands that you can use:

| AT Command | Description | 
| ---- | ---- | 
| at+version | Get the current firmware version number | 
| at+get_config=device:status | Get all information about the device’s hardware components and their current status. | 
| at+set_config=device:restart | Restart the Device | 
| at+set_config=device:X:Y | Set a certain sensor’s status. X&nbsp;: the sensor’s flag&gt; gps&nbsp;-&nbsp; GPS, &gt; acc - Acceleration, &gt; magn - Magnetic, &gt;&nbsp;gyro - Gyroscope, &gt; pressure - Pressure, &gt; temperature - Temperature, &gt; voltage - Voltage. Y&nbsp;: 1 - Activate , 0- Deactivate | 
| at+join | Start the join procedure for the LoRaWAN network | 
| at+send=lora:X:Y | Send an uplink with a custom payload:X - LoRa Frame PortY&nbsp;- The data which you want to send. (Length limit is 50 bytes and the data must be in Hex Format) | 
| at+set_config=lora:work_mode:X | Set the Working Mode:X :&nbsp; 0 - LoRaWan, 1: LoRaP2P,&nbsp;&nbsp;2: Test Mode | 
| at+set_config=lora:join_mode:X | Set the Join Mode:&nbsp;X :&nbsp; 0 - OTAA, 1 -&nbsp; ABP | 
| at+set_config=lora:class:X | Set the Class for LoRa.X :&nbsp; 0 - Class A, 1 - Class B, 2 - Class C | 
| at+set_config=lora:region:X | Set the Region:X : Options - EU433, CN470, IN865, EU868, AU915, US915, KR920, AS923 | 
| at+set_config=lora:confirm:X | Set the type of LoRa Frames the node will be sendingX : 0 - Unconfirmed, 1: Confirm | 
| at+set_config=lora:ch_mask:X:Y | Turn a certain channel on/offX : The Channel Number you want to toggle. You can check the channel number using the command : at+get_config=lora:channelY : 0 - Off , 1 - On | 
| at+setconfig=lora:dev_eui:X | Set the device EUIX : The Device EUI | 
| at+setconfig=lora:app_eui:X | Set the application EUI&nbsp;(for OTAA)X : The Application EUI | 
| at+setconfig=lora:apps_key:X | Set the Application key for (for OTAA)X : The Application Key | 
| at+setconfig=lora:nwks_key:X | Set the network session key (for ABP)X : The Network Session Key | 
| at+setconfig=lora:apps_key:X | Set the Application session key (for ABP)X : The Application Session Session Key | 
| at+set_config=lora:send_interval:X | Set the interval time of sending dataX : The Time Interval in seconds | 
| at+get_config=lora:status | It will return all of the current information of LoRa, except the LoRa Channel | 
| at+get_config=lora:channel | It will return the state of all LoRa channels, then you can see which channel is closed and which channel is open very clearly | 


