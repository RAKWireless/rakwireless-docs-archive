---
type: page
title: Networking Applications
listed: true
slug: networking-applications---rak7431-rs485-to-lorawan-converter
---published

RAK7431 can convert the data of RS485 devices into LoRaWAN® that can be sent to the cloud via a standard Gateway. Cloud servers can also actively send data to RS485 terminals to achieve two-way data transmission. Using RAK7431, what used to be a costly and time-consuming cable line network deployment can be transformed into a rapid and cost-efficient wireless network deployment.

An example would be using the RAK7249 Macro Outdoor Gateway coupled with the RAK WisDM cloud management platform, in order to realize an end-to-end industrial field data acquisition and control system. Using the built-in LoRa® Server, that comes standard with any RAK Gateway, one could seamlessly achieve transmission of the end device data to any application server. Furthermore, the MQTT integration allows for a high level of security and efficiency.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1597337217\/24681\/msjhjg3pu2odf1ilr2aa.png",
        "mode": "responsive",
        "width": 1515,
        "height": 611,
        "caption": "**Figure 1:** RS485 to LoRaWAN\u00ae network structure"
    }
}]$

### Polling Mode

RAK7431 can work in polling mode in order to send query instructions to RS485 nodes, and convert the data returned into LoRa® frames to be relayed to the application server through a Gateway.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1597337178\/24681\/p86veaxbnkfoo04gp6in.png",
        "mode": "responsive",
        "width": 1141,
        "height": 446,
        "caption": "**Figure 2:** RAK7431 polling mode"
    }
}]$

RAK7431 can store a maximum of 32 query instructions in polling mode, each of which has a maximum length of 128 bytes. Polling time interval and waiting time can be adjusted as required.

RAK7431 converts the data returned by RS485 nodes into LoRa® packets that can be sent to Gateway in two ways: transparent or packet. 

- In transparent mode, RS485 data is encapsulated in the payload of LoRa® frames as it is.
- In packet mode, RS485
data is encapsulated in LoRa® frames with the addition of a header and verification.

No matter whether polling mode is enabled or not, the server can actively send commands to query the RS485 nodes through the Gateway via the RAK7431. The commands issued and the returned data can also be transmitted in transparent mode or in packet mode.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1597337155\/24681\/luxsdfhgwafoif4nidnm.png",
        "mode": "responsive",
        "width": 1123,
        "height": 464,
        "caption": "**Figure\n3:** RAK7431\ntransparent mode"
    }
}]$

