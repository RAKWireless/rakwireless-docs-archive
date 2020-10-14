---
type: page
title: LoRa Gateway Configuration
listed: true
slug: lora-gateway-configuration
---published

All settings related to the LoRaWAN performance of the gateway can be found in this section. Setting those in an optimum matter will ensure that packets from end nodes are forwarded correctly, nodes are registered and errors avoided.

## 1. LoRa Packet Forwarder

As this is the backbone of the LoRaWAN Gateway, the number of settings and options is greatest here. Thus, this section will be larger and provide information in more detail than previous ones. For the aforementioned reasons this section has several configuration tabs, which are listed in the following paragraphs. Additionally some of the configuration options have their own documents, with detailed explanation of the configuration process.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1562450935\/17414\/psmjorsdi2icgsu3lol5.jpg",
        "mode": "responsive",
        "width": 2090,
        "height": 1338,
        "caption": "**Figure 1.** LoRa Packet Forwarder page"
    }
}]$

**General Setup**

Additionally there is a field for adding the Standard LoRa Channel and FSK channel (you need also choose the SF, Bandwidth and data rate of each of the aforementioned).

This is where the core settings are: Gateway EUI, Frequency channels, etc.

**Gateway EUI:**

The value in this field is necessary for registering your gateway with any LoRaWAN Network Server.

**Frequency Plan Template:**

Currently the Indian, Russian and European Union bands are supported. After selecting the appropriate choice and pressing the Import button, the Concentrator module settings at the bottom of the page will be populated automatically.

Please refer to the [Custom Frequency Plan Configuration Manual ](https://doc.rakwireless.com/rak7258-micro-gateway/web-channel-customizing)for details on how to edit the settings in order to have your choice of channels to be used by the Gateway.

**Protocol:**

You have three options, which define how the Gateway will function:

**Semtech UDP GWMP Protocol:**

By default, this is the Semtech Packet Forwarder, which sends packets to the Server Address of your choice (IP or URL). By default it points to the local TTN router.

The default port value is 1700 used by TTN.

One can also set parameters as the Statistic Interval (s), Push Timeout (ms), and the Auto-quit Threshold.

**LoRa Gateway MQTT Bridge:**

By choosing this option, you make the Gateway act as a bridge to the MQTT Broker, which is hosted somewhere separate. You need to configure the Gateway to point to the correct address of the MQTT broker

**Built-in LoRa Server:**

In case you require an integrated solution where the LoRa Network Server is hosted on the gateway itself you choose this option. The configuration of the LoRa MQTT Bridge itself is done in a separate section of the configuration UI, which is discussed in Paragraph 3.3.2

**Beacon Setup**

In the case of Class B LoRa devices, you need to have a beacon in order to synchronize downlink message windows. Thus, you have to configure its parameters: Frequency Channel, SF, Bandwidth, Tx Power, etc. Make sure you adhere to the LoRa Alliance recommendations.

**Packet Filter**

By enabling this functionality, you can filter incoming traffic and only forward packets from the desired nodes in order to optimize bandwidth usage over back-haul.  You can filter by OUI or Network ID by white-listing.

The _Enable Auto Filter_ slider allows nodes to be automatically dropped in accordance with a set of parameters. One can set threshold values for _Discard Period_, _Join Period_, _Join Interval_, and _Join Count_ (1 and 2 for Join Interval and Join Period respectively).

**GPS Information**

In case, you want to enter the GPS parameters for the Gateway manually.

**Frequency Plan**

This is a part of the page, common for all gateway from the RAK72xx series, however depending on the number of Concentrator modules installed there are variations. The difference when there is a second Concentrator is that first it has to also be configured, and second only the fields for the central frequencies for Radio 0 and Radio 1 need be set.

There are two mode for setting the frequencies:

**Standard Mode:**

You can start by importing a region via the drop down menu (EU868 is the default one). You will get the defaults channels for the chosen frequency band and the option to add additional ones. Simply enter the frequency in the text box (in MHz) and click the “Add” button. You can add as many channels as you need as long as they fall in the Regional band.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1562452860\/17414\/hxiwqengvkvyz268bexx.jpg",
        "mode": "responsive",
        "width": 2050,
        "height": 1284,
        "caption": "**Figure 2.** Frequency Plan (Standard Mode)"
    }
}]$

**Advanced Mode:**

Because of the presence of double SX1257s, you need to configure the two radios separately. You have eight Multi Spreading Factor Channels, The LoRa Standard Channel and the FSK Channel. The sliders can enable or disable those, so you can choose to have any number of them active. Additionally you can choose which radio to use for a given, channel as long as you do not assign more than five channels per radio. In order to set the desired channel to a given frequency you need to input an offset value in the _If _field. Thus, the channel frequency will be the central frequency (Radio 0 Freq_ or Radio 1 Freq parameter) summed with the offset value (in Hz).

Additionally for the LoRa Standard and FSK channels, you are also required to select the Bandwidth and Data Rate.

As mentioned before you can choose to import those settings for the Indian, Russian and EU Regions (in accordance with the LoRa Alliance specifications).

For details on the procedure refer to the [Custom Frequency Plan Configuration Manual](https://app.developerhub.io/rakwireless-docs/quick-start/rak7258-micro-gateway/web-channel-customizing).

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1562453075\/17414\/zi0cxsgmnny6uihgpsan.jpg",
        "mode": "responsive",
        "width": 2102,
        "height": 1324,
        "caption": "**Figure 3.** Frequency Plan (Advanced Mode)"
    }
}]$

## 2. LoRa Gateway MQTT Bridge

The Gateway is capable of working with an external LoRa Server, where the MQTT Broker is functioning separately. For this purpose, there are several tabs with their corresponding parameters to be filled.

**General Setup**

The tab starts with the button to enable/disable this functionality, followed by:

_MQTT Broker Address:_

The IP Address where the MQTT Broker is hosted.

_MQTT Broker Port:_

The corresponding port.

**Enable Authentication:**

The switch turns on Encryption of the transmitted data. You need to configure the Certificates used to encrypt the data in order for secure authentication to be performed.

**TLS Version:**

The version of the TLS protocol to be used. Options are TLSv1, TLSv1.1, TLSv1.2

**Username/Password:**

Credentials the MQTT Bridge is to use for connecting to the LoRa Server instance

**CA Certificate, TLS Certificate, TLS Key:**

Those are to be generated via the appropriate algorithm and distributed between the MQTT Broker and the LoRa Server.

**Please refer to the [MQTT Bridge Configuration (TLS)](https://doc.rakwireless.com/rak7258-micro-gateway/mqtt-bridge-configuration--tls-) for details on how to edit the settings in order for the Gateway to work as an MQTT Bridge with TLS Encryption.**

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1562453235\/17414\/wt4wbrvvzwg68zlq9lo2.jpg",
        "mode": "responsive",
        "width": 2108,
        "height": 920,
        "caption": "**Figure 4.** LoRa Gateway MQTT Bridge"
    }
}]$

