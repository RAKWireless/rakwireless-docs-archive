---
type: page
title: Product Deployment Typical Application
listed: false
slug: product-deployment-typical-application
---published

We will deploy a typical scenario. We will walk through the configuration process of all devices that are required. Additionally we will explain in details after we are done configuring, what are the benefits of this particular use-case, the message formats, etc.

Configuration of the devices will be done in order as per the topology in the next subsection.

### Network Topology

- Gateway-A: RAK7249/58 Nexus Gateway (LoRa® Server in use) 
- Gateway-B: RAK7249/58 External Gateway (MQTT Bridge in use) 
- RAK 811 LoRa® Evaluation Board

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1580547276\/22610\/iggjiirykmlbjhldy7de.jpg",
        "mode": "responsive",
        "width": 966,
        "height": 548,
        "caption": "**Figure 1**: Network Topology"
    }
}]$

This is the minimum of devices required. However, you can integrated more nodes and also more External Gateways. As an advanced configuration feature, we will forward all the traffic from the Nexus Gateway to an MQTT broker hosted separately. This is not mandatory, however, it is good practice and is required in some cases.

