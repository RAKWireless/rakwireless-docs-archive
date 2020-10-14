---
type: page
title: AT Commands for RAK5010 WisTrio NB-IoT Tracker
listed: true
slug: at-commands-for-rak5010
---published

The purpose of this document is to demonstrate on how to configure the RAK5010 Wistrio NB-IoT Tracker thru the use of AT Commands via a Serial Port Tool running in your Windows PC. The list below shows the AT Commands available for use:

| **AT Command** | **Description** | 
| ---- | ---- | 
| at+version | Get the current firmware<br>version number. | 
| at+set_config=device:restart | After set, the device will<br>restart. | 
| at+get_config=device:status | Get all information about<br>the device’s hardware components and their current status. | 
| at+set_config=device:sleep:**X** | After set, the device will<br>go to sleep or wake up immediately.<br><br>• **0** - sleep<br><br>• **1** - wake up | 
| at+set_config=device:gps:**X** | • **X** - **0**: close, **1**: open, **2**: sleep, **3**: standby | 
| at+set_config=device:cellular:**X** | • **X** - **0**: close, **1**: open | 
| at+set_config=cellular:send_interval:**X**:**Y** | Set the interval of sending packet loop.<br><br>• **X** - **0**: off, **1**: on.<br><br>• **Y -** the interval<br>time (ms)<br>This value must be more<br>than 150000 (150s).<br>If the X is set to 1, it<br>means that the device will sleep for Y ms after sending a packet automatically<br>in a loop, until you set X to 0. | 
| at+scan=cellular | Scan the around Cellular<br>networks | 
| at+set_config=cellular:**XXX**:**Y**:**ZZZ**:<br>**AAA**:**BBB**:**C** | Set the IP address and port which you want to send data to through Cellular. <br><br>• **XXX -** The IP address you want to send data to. <br><br>• **Y -** The port you want to send data to.<br><br>• **ZZZ -** The cellular operator’s long name you want to connect, for example: CHINA MOBILE. <br><br>• **AAA -** The short name of the Cellular operator, for example: CMCC.<br><br>• **BBB -** The operator’s APN name, for example CMNET.<br><br>• **C -** The number of<br>the Cellular network type. For example, 0 indicates GSM, 8 indicates LTE<br>cat.M1, and 9 indicates LTE cat.NB1. | 
| at+set_config=cellular:(**XXX**) | Set the Cellular module<br>using the Cellular module’s common AT commands which come from its manufacture. <br><br>• **XXX -** The<br>Cellular module’s common AT commands. <br><br>For the full list of supported Quectel BG96 AT Commands, go [here](https://www.quectel.com/product/bg96.htm). | 
| at+send=cellular:**XXX** | Send a data through cellular.<br><br>• **XXX -**The data you want to send. | 
| at+set_config=hologram:**XXX** | Configure the Hologram SIM card.<br><br>• **XXX -** the device key of the Hologram SIM card. You can find it on [**Hologram web page**](https://dashboard.hologram.io) after activating the Hologram SIM card. | 
| at+send=hologram:user:**XXX** | Send a data to Hologram<br>server.<br><br>• **XXX** - the data<br>you want to send. | 
| at+send=hologram:sensor | Send a packet of the<br>current sensor’s data to Hologram server. | 
| at+set_config=ble:work_mode:**X**:**Y** | Set the work mode for BLE.<br><br>• **X** - **0**: BLE peripheral mode, **1**: BLE central mode, **2**: Beacon scan mode<br><br>• **Y** - **0**: normal range, **1**: BLE long range<br><br>More information about BLE Connection Modes is explained in [auto$](/rak5010-wistrio-nb-iot-tracker/bluetooth-connection-modes) | 


