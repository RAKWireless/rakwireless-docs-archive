---
type: page
title: Status Page
listed: true
slug: status-page
---published

This document shows you the settings where in the statistics about the Gateway behavior can be monitored in real time.

## 1. Overview

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1564883824\/18277\/wqe88iiqoiwx91tvkygn.jpg",
        "mode": "responsive",
        "width": 1319,
        "height": 610,
        "caption": "**Figure 1.** Status Overview of the WEB Management Platform."
    }
}]$

The following are the parts of the Overview window: 

- **Received**:
Shows the total number of uplink LoRa messages received by the gateway. 
- **Transmitted**:
Shows the total number of downlink LoRa message sent by the gateway.
- **Active Nodes**:
Shows the number of active LoRa nodes within the LoRa gateway coverage (those that
have sent no data for more than 10 min are discarded from the count). 
- **Busy Nodes**:
Shows the number of busy nodes within the LoRa gateway coverage (nodes with an
average message spacing of less than 60s). 
- **Duty Cycle of the LoRa Channel**: The graph represents the Duty Cycle load by frequency channel (Data is kept for the last 12
hours). The minimum resolution along the time axis is 60s. Each value is an average over
60s. The values are color code – green to red, low to high. 
- **LoRa Traffic**:
The graph shows the packet per minute rate as a function of time. Above the image, one
can see the color-coding of the different Spreading Factors, where the actual height of the
values is a sum of all the packets over all spreading factors for the time sample. 

## 2. LoRaWAN Packet Logger

This is where a log of the LoRa messages is shown in real time. There are several options
for filtering as well as the possibility to download the statistics in a file. Additionally there is a
summary (Total, Uplink, and Downlink), below the filter fields.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1564884181\/18277\/ghputbsyh3moy2l2x1wi.jpg",
        "mode": "responsive",
        "width": 991,
        "height": 558,
        "caption": "**Figure 2.** LoRaWAN Packet Logger View of the WEB Management Platform."
    }
}]$

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1564884108\/18277\/sidmybzb76jxnrvqv7ip.jpg",
        "mode": "responsive",
        "width": 1919,
        "height": 889,
        "caption": "**Figure 3.** Detailed Information of each Message in the LoRaWAN Packet Logger"
    }
}]$

- **LoRaWAN Packet Logger**: Real-time recording and parsing of messages sent and received by the LoRaWAN Gateway, can be filtered according to message type and node address.
- **Type**: Filter by message type. Select ALL as unfiltered and display all messages.
- **DevAddr**: Filter messages based on node addresses.
- **Hide CRC_ERR packet**: When it is selected, no "[CRC](https://en.wikipedia.org/wiki/Cyclic_redundancy_check)" check error message will be displayed.
- **Pause/Play**: Pause/start message recording.
- **Clear**: Clear the current record.
- **Download**: Save the current record locally in "CSV "format.\

## 3. System Log

The system log, updated in real time can be seen in this menu. It includes in addition to the host processes, the LoRa frames received/transmitted by the gateway. If the connection to the LoRa Network server is lost, it is automatically backed up on the SD card (provided one is inserted in the slot).

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1564884325\/18277\/hbhufae7rxm0z7dbqc0y.jpg",
        "mode": "responsive",
        "width": 2054,
        "height": 1200,
        "caption": "**Figure 4.** System logger"
    }
}]$

## 4. Firewall

This section houses the Firewall settings. It also where you go to reset the Firewall

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1564884382\/18277\/qgeysrx1bklzusgofo2i.jpg",
        "mode": "responsive",
        "width": 2079,
        "height": 1221,
        "caption": "**Figure 5.** Firewall"
    }
}]$

