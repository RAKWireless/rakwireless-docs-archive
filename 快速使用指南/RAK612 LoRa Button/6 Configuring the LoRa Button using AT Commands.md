---
type: page
title: Configuring the LoRa Button using AT Commands
listed: true
slug: configuring-the-lora-button-using-at-commands
---published

You can configure your LoRa Button by sending AT Commands via a Serial port tool running on your PC. The following list shows the AT Commands that you can use:

| AT Command | Description | 
| ---- | ---- | 
| at+version | Get the current firmware version. | 
| at+mode=0 | Set the LoRa Button to work&nbsp;LoRaWAN mode. | 
| at+band=EU868 | Set the Region, which you want the LoRa Button to work in. EU868&nbsp; is just an example. You can set it to AS923, US915, AU915, KR920,&nbsp;or IN865 when you are using a "HF" (High Frequency) Firmware. You can also set it to EU433 or CN470 when you are using a "LF" (Low Frequency) Firmware. | 
| at+get_config=dev_eui | Check the current device EUI | 
| at+set_config=join_mode:1 | Set the activation method: 1 corresponds to OTAA, 0 to&nbsp;APB. | 
| at+set_config=dev_eui:xxxxxxxxxxxxxxxx | Set the device EUI. Used in case of&nbsp;OTAA. | 
| at+set_config=app_eui:xxxxxxxxxxxxxxxx | Set the application EUI. Used in case of&nbsp;OTAA. | 
| at+set_config=app_key:xxxxxxxxxxxxxxxxx | Set the application key. Used in case of&nbsp;OTAA. | 
| at+set_config=dev_addr:xxxxxxxx | Set the device address. Used in case of&nbsp;ABP. | 
| at+set_config=nwks_key:xxxxxxxxxxxxxxxx | Set the network session key.&nbsp;Used in case of&nbsp;ABP. | 
| at+set_config=apps_key:xxxxxxxxxxxxxxxx | Set the application session key. Used in case of ABP. | 
| at+set_config=timer_sleep :&lt;time_interval&nbsp;&gt; | &lt;time_interval&gt; is the cycle time (in seconds) before the LoRa Button will turn off. If you don't press any key on the LoRa Button in this specific cycle time, it will turn off to save some power. The default value is 0, which means the LoRa Button will not power cycle. | 
| at+get_config=timer_sleep | Get the current sleep timer value. | 
| at+key_config=&lt;key_num&gt;,&lt;port&gt;,&lt;data&gt; | Customize the function of each key.&nbsp; &lt;key_num&gt; is the number of the key that you want to customize in the LoRa Button. &lt;port&gt; is the frame port where you are sending the data. &lt;data&gt; is the actual data that you want to send when you press this specific key of the LoRa Button. | 
| at+send=&lt;type&gt; | &lt;type&gt; is the type of data that you are sending. 0 for unconfirmed messages, 1 for confirmed. | 
| at+join=otaa | Join via OTAA. | 
| at+join=abp | Join via ABP. | 
| at+reset=0 | Restart the LoRa Button. | 


