---
type: page
title: RAK7249 Macro Outdoor Gateway Setup
listed: true
slug: rak7249-macro-outdoor-gateway-setup
---published

For the RAK7249 Macro Outdoor Gateway be able to connect to The Things Network (TTN), it must work in **Semtech UDP Packet Forwarder** mode as prescribed by The Things Network (TTN) [document](https://www.thethingsnetwork.org/docs/gateways/packet-forwarder/semtech-udp.html). 

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1583412777\/26717\/gcspmdhtnguzkblwxrom.png",
        "mode": "responsive",
        "width": 1927,
        "height": 1332,
        "caption": "**Figure 1**: LoRa\u00ae Packet Forwarder page"
    }
}]$

Follow the steps below to successfully connect your RAK7249 Macro Outdoor Gateway to The Things Network (TTN). Take note of the parameters needed for the LoRaWAN® Gateway to connect successfully.

**Parameters Needed**:

- **Protocol**: Semtech UDP GWMP Protocol
- **Server Address**: Other term is  **Router Address**. (Taken from the list provided in the Semtech UDP Packet Forwarder document.)
- **Server Port Up**: 1700
- **Server Port Down**: 1700
- **Frequency Plan**: Your chosen RAK7249 Macro Outdoor Gateway Frequency. (This must coincide with your Frequency Plan Setting in the Register Gateway setup in TTN.)

**1**.Follow the [auto$](/rak7249-macro-outdoor-gateway/web-management-platform) document to access the **LoRa®  Packet Forwarder** Section and you shall see the **General Setup** Tab in the right side of the platform.

**2**.Fill in the required parameters mentioned beforehand especially in the working frequency of your purchased RAK7249 Macro Outdoor Gateway Frequency.

