---
type: page
title: GNSS Receiver
listed: true
slug: gnss-receiver-rak8213
---published

RAK8213 includes a fully integrated **Global Navigation Satellite System (GNSS)** solution that supports Gen8C-Lite of Qualcomm (GPS, GLONASS, BeiDou/Compass, Galileo andQZSS).

 The module supports standard NMEA-0183 protocol, and outputs NMEA sentences at         1Hz data update rate via USB interface by default.

$plugin[{
    "type": "callout",
    "data": {
        "text": "By default, RAK8213 GNSS engine is switched off. It has to be switched on via AT command.",
        "type": "info",
        "title": "Note"
    }
}]$

### GNSS Performance

 The following table shows the GNSS performance of RAK8213:

| **Parameter** | **Description** | **Conditions** | **Typical** | **Unit** | 
| ---- | ---- | ---- | ---- | ---- | 
| Sensitivity<br><br>(GNSS) | Cold start | - Autonomous | -146 | dBm | 
|  | Re-acquisition | - Autonomous | -157 | dBm | 
|  | Tracking | - Autonomous | -157 | dBm | 
| TTFF<br><br>(GNSS) | Cold start @open sky | - Autonomous <br>- XTRA enabled | 31<br><br>11.54 | s<br><br>s | 
|  | Warm start @open sky | - Autonomous <br>- XTRA enabled | 21<br><br>2.52 | s<br><br>s | 
|  | Hot start @open sky | - Autonomous<br>- XTRA enabled | 27<br><br>1.82 | s<br><br>s | 
| Accuracy <br><br>(GNSS) | CEP-50 | - Autonomous @open sky | < 2.5 | m | 


$plugin[{
    "type": "callout",
    "data": {
        "text": "1.**Tracking sensitivity**: the lowest GNSS signal value at the antenna port on which the module can keep on positioning for 3 minutes.\n\n2.**Re-acquisition sensitivity**: the lowest GNSS signal value at the antenna port on which the module can fix position again within 3 minutes after loss of lock.\n\n3.**Cold start sensitivity**: the lowest GNSS signal value at the antenna port on which the module fixes position within 3 minutes after executing cold start command.",
        "type": "info",
        "title": "Note"
    }
}]$

