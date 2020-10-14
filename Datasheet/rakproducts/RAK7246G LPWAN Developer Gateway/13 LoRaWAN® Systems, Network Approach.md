---
type: page
title: LoRaWAN® Systems, Network Approach
listed: true
slug: lorawan-systems-network-approach
---published

The use of LoRaWAN® technology can be distinguished in “Public” and “Private” networks. In both cases the usage of a concentrator module is a must if a multichannel performance is sought after. Public networks are operator (e.g. telecom) managed networks whereas private networks are individually managed networks. 

LoRaWAN® networks are typically star or multiple star networks where a Gateway relays the packets between the end-nodes and a central network server. For private network approaches the server can also be implemented on the Gateway host. 

Due to the long range LoR®a provides the connection between the end-nodes and the Gateway (RAK2246) is always a direct link. Repeaters are not common in a LoRaWAN® network. 

Depending on the used spreading factor and signal bandwidth different data rates (0.3 kbps to ~22 kbps) and sensitivities down to -142.5 dBm are possible. Spreading factor and signal bandwidth are a trade-off between data rate and communication range.

### Overview

The RAK2246 is able to receive on different frequency channels at the same time and is able to demodulate the LoRa® signal without knowledge of the used spreading factor of the sending node. Thus, any Gateway using it as its concentrator module has these inherent benefits as well.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1583119070\/26046\/f333yrqj2l328fhmkpaf.png",
        "mode": "600",
        "width": 3001,
        "height": 3000,
        "caption": null
    }
}]$

Due to the fact that the combination of spreading factors and signal bandwidths results in different data rates the use of “Dynamic Data-Rate Adaption” becomes possible. That means that nodes a large distance away from the Gateway can use higher spreading factors and therefore have a lower data rate. Nodes which are closer to the concentrator can use lower spreading factors and therefore can increase their data rate. 

Due to the fact that spreading factors are orthogonal and the RAK2246 Concentrator can demodulate on 8 channels at the same time, channel capacity of a Gateway is increased compared to traditional cellular networks.

### Firwmare

The LoRa® MAC specification is currently driven by the companies Semtech, IBM and Actility. Currently all available software, firmware and documentation can be found and downloaded from the open source project LoRa-net hosted on [https://github.com/Lora-net](https://github.com/Lora-net)

This project considers all parts that are needed to run a network based on LoRa® technology. It includes the node firmware (several hardware platforms are supported), the Gateway host software (HAL driver for SX1308, packet forwarder) and a server implementation. 

It is highly recommended to utilize the latest HAL as provided by Semtech.

### Configuring the Gateway

You can login to the Gateway using an SSH client like PuTTY. For more
details on the configuration and management of the Gateway please visit the
link below:

[RAK7246G LPWAN Developer Gateway User Manual](https://doc.rakwireless.com/rak7246g-lorawan----developer-gateway)

