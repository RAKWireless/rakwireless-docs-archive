---
type: page
title: LoRaWAN® Gateway Configuration
listed: false
slug: lorawan-gateway-configuration
---published

This is a very important section of the Web UI. Here you set the frequency of operation of the Gateway. It is these frequency channels that it will be monitoring and both receiving from and transmitting to LoRa® nodes.

In case you want to use a custom set, you can enter a channel’s frequency (in MHz) in the text box and add it via the blue button. This applies for the Standard LoRa® Channel and FSK Channel as well (normally you would have one per Concentrator.

You can also “Switch to Advanced Mode”, where you have more granular control per concentrator and per radio. (up to 2 concentrators and 2 radios per concentrator for up to 4 total radios).

## 1.LoRa® Packet Forwarder

As this is the most important part of the gateway, the number of settings and options is greatest here. Thus, this section will be larger and provide information in more detail than previous ones. For the aforementioned reasons this section has several configuration tabs, which are listed in the following paragraphs. Additionally, some of the configuration options have their own documents, with detailed explanation of the configuration process, which you can find in the [RAKwireless documentation hub](https://doc.rakwireless.com/).

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1584108444\/18279\/cgynu2f4hazhe8my6j3l.png",
        "mode": "responsive",
        "width": 1918,
        "height": 875,
        "caption": "**Figure 1**: LoRa\u00ae Packet Forwarder Page"
    }
}]$

### General Setup

This is where the core settings are: **Gateway EUI**, **Frequency channels**, etc.

1.**Gateway EUI**

The value in this field is necessary for registering your gateway with any LoRaWAN® Network Server.

2.**Protocol**

You have three options, which define how the Gateway will function:

- **Semtech UDP GWMP Protocol**: By default, this is the Semtech Packet Forwarder, which sends packets to the Server Address of your choice (IP or URL). By default it points to the local TTN router. The **default port value** is **1700** used by TTN. One can also set parameters as the Statistic Interval (s), Push Timeout (ms), and the Auto-quit Threshold.
- **LoRaWAN® Gateway MQTT Bridge**: By choosing this option, you make the Gateway act as a bridge to the MQTT Broker, which is hosted somewhere separate. You need to configure the Gateway to point to the correct address of the MQTT broker
- **Built-in LoRa® Server**: In case you require an integrated solution where the LoRa® Network Server is hosted on the gateway itself you choose this option. 

3.**Frequency Plan Template**

Currently, the Indian, Russian and European Union bands are supported. After selecting the appropriate choice and pressing the Import button, the Concentrator module settings at the bottom of the page will be populated automatically.

4.**Automatic Data Recovery**

This is an important feature that allows LoRa® Frames to be stored on the **SD card** (provided there is one in the slot), if there is no connection to the LoRaWAN® Network Server. Upon restoring connectivity, these buffed messages will be forwarded, so no data will be lost. This is done in blocks of 8 (FIFO), until all are cleared from the buffer.

 5.**Is LoRaWAN**® **Network**

If you choose “**NO**” here, you will enable frames that are not compliant with the LoRaWAN® specification to be forwarded (in case you have your proprietary LoRa® Server solution). By default, “**YES**” is selected and non-LoRaWAN® packets are dropped.

 6.**Log Level**

You can choose from 5 different log levels (**Error/Warning/Notice/Info/Debug**). This will affect System Log. From Errors only to full system log for debugging.

### Beacon Setup

In the case of Class B LoRa® devices, you need to have a beacon in order to synchronize downlink message windows. Thus, you have to configure its parameters: Beacon Period, Beacon Frequency (Hz), Beacon Channel Number, Beacon Frequency Step, Beacon Data Rate (SF9-SF12), Beacon Bandwidth (125000 Hz by default), Beacon Tx Power (14 dBm by default), Beacon Information Descriptor.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1584112187\/18279\/cw5wt1kkh6ssyprcepwj.png",
        "mode": "responsive",
        "width": 1916,
        "height": 612,
        "caption": "**Figure 2**: Beacon Setup Page"
    }
}]$

### Packet Filter

By enabling this functionality, you can filter any incoming traffic and only forward packets received from the desired nodes in order to optimize bandwidth usage over backhaul.  You can filter by OUI or Network ID by white-listing.

The **Enable Auto Filter** slider allows nodes to be automatically dropped in accordance with a set of parameters. One can set threshold values for Discard Period, Join Period, Join Interval, and Join Count (1 and 2 for Join Interval and Join Period respectively).

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1584112308\/18279\/c38h81koglxfflcskrek.png",
        "mode": "responsive",
        "width": 1917,
        "height": 760,
        "caption": "**Figure 3**: Packet Filter Page"
    }
}]$

### GPS Information

In case, you want to enter the GPS parameters for the Gateway manually. Just input your **Latitude**, **Longitude** and **Altitude** then press "**Save and Apply**" at the bottom of the page.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1584112896\/18279\/evpr14xoi5z5abl221bq.png",
        "mode": "responsive",
        "width": 1918,
        "height": 451,
        "caption": "**Figure 4**: GPS Information Page"
    }
}]$

### Frequency Plan

This is a part of the page, common for all gateway from the RAK72xx series, however depending on the number of Concentrator modules installed there are variations. The difference when there is a second Concentrator is that first it has to also be configured, and second only the fields for the central frequencies for Radio 0 and Radio 1 need be set.

There are two mode for setting the frequencies:

- **Standard Mode**: You can start by importing a region via the drop down menu (EU868 is the default one). You will get the defaults channels for the chosen frequency band and the option to add additional ones. Simply enter the frequency in the text box (in MHz) and click the “**Add**” button. You can add as many channels as you need as long as they fall in the Regional band. Additionally for the LoRa® Standard and FSK channels, you are also required to select the Bandwidth and Data Rate.

$plugin[{
    "type": "callout",
    "data": {
        "text": "In case you have the RAK7249 or RAK7240 with a second concentrator module, you can add this one too by pressing the Add\/Remove LoRa Concentrator button at the bottom of the page and add additional channels (Multi-SF) for a total of 16.",
        "type": "info",
        "title": "Note:"
    }
}]$

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1584113454\/18279\/lhablbmlgjw7ujcrupfy.png",
        "mode": "responsive",
        "width": 1332,
        "height": 642,
        "caption": "**Figure 5**: Frequency Plan (Standard Mode)"
    }
}]$

- **Advanced Mode**: Because of the presence of double SX1257s, you need to configure the two radios separately. You have eight Multi Spreading Factor Channels, The LoRa® Standard Channel and the FSK Channel. The sliders can enable or disable those, so you can choose to have any number of them active. Additionally you can choose which radio to use for a given, channel as long as you do not assign more than five channels per radio. In order to set the desired channel to a given frequency you need to input an offset value in the **If field**. Thus, the channel frequency will be the central frequency (Radio 0 Freq or Radio 1 Freq parameter) summed with the offset value (in Hz). As mentioned before you can choose to import those settings for the Indian, Russian and EU Regions (in accordance with the LoRa Alliance® specifications).

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1584113655\/18279\/k9gpy6wg99hgxhhycm0m.png",
        "mode": "responsive",
        "width": 1916,
        "height": 804,
        "caption": "**Figure 6**: Frequency Plan (Advanced Mode)"
    }
}]$

## 2.LoRaWAN® Gateway MQTT Bridge

The Gateway is capable of working with an external LoRa® Server, where the MQTT Broker is functioning separately. For this purpose, there are several tabs with their corresponding parameters to be filled.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1584185503\/18279\/bncstxtjhow5yupqfdxg.png",
        "mode": "responsive",
        "width": 1929,
        "height": 854,
        "caption": "**Figure 7**: MQTT Bridge Setup Page"
    }
}]$

### General Setup

1.**Enable**

This slider is used to enable/disable this functionality.

2.**LoRa® Network Server Type**

Choose on the following options:

- **Built-in LoRa Network Server**: Choose this if you are going to be using the Built-in LoRa Network Server
- **loraserver 2x**: Choose this if you are pointing to an MQTT 2x Broker (JSON)
- **loraserver 3x**: Choose this if you are pointing to an MQTT 3x Broker (PROTOBUF)
- **loraserver 3x**: Choose this if you are pointing to an MQTT 3x Broker (JSON-V3)

3.**MQTT Broker Address**

The IP Address where the MQTT Broker is hosted.

$plugin[{
    "type": "callout",
    "data": {
        "text": "The MQTT Broker IP Address for Built-in is **127.0.0.1**",
        "type": "info",
        "title": "Note:"
    }
}]$

4.**MQTT Broker Port**

The corresponding port.

$plugin[{
    "type": "callout",
    "data": {
        "text": "The MQTT Broker default port is **1883**.",
        "type": "info",
        "title": "Note:"
    }
}]$

5.**MQTT Protocol Version**

You can choose between V3.1 and V3.1.1

6.**Client ID**

An ID that is used to associate with the topic. If left empty a random one will be generated.

7.**Clean Session**

With this button enabled, the broker will not store any subscription information or undelivered messages.  

8.**Will Retain**

With this button enabled, the last message published will be retained. 

9.**Quality of Service (Qos)**

You can set the desired Quality of Service level.

 10.**keepalive**

The keep alive interval in seconds. The default alive interval is 10 seconds.

 11.**Enable Authentication**

The switch turns on Encryption of the transmitted data. You need to configure the Certificates used to encrypt the data in order for secure authentication to be performed.

 12.**SSL/TLS Mode**

By default, this isDisabled.You can choose one of 3 other modes:

- CA signed server certificate
- Self-signed server certificate
- Self-signed server & client certificate.

13.**TLS Version**

The version of the TLS protocol to be used. Choose in the options below:

- TLSv1
- TLSv1.1
- TLSv1.2

14.**CA Certificate, TLS Certificate, TLS Key**

Those are to be generated via the appropriate algorithm and distributed between the MQTT Broker and the LoRaWAN® Server.

$plugin[{
    "type": "callout",
    "data": {
        "text": "Please refer to the [MQTT Bridge with TLS Encryption Configuration Manual](https:\/\/downloads.rakwireless.com\/en\/LoRa\/DIY-Gateway-RAK7249\/Application-Notes\/LoRaWAN_Gateway_MQTT_Bridge%2BTLS_Configuration_Guide_V1.1.pdf) for details on how to edit the settings in order for the Gateway to work as an MQTT Bridge with TLS Encryption.",
        "type": "info",
        "title": "Note:"
    }
}]$

15.**Log Level**

The granularity of the log information is chosen from the following levels: 

- ERROR
- INFO (default)
- DEBUG
- TRACE

### MQTT Topic Template Setup

Refer to the image below for the MQTT 2x Topic Template:

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1584198498\/18279\/z8mjsk2kvrgvmjikvalo.png",
        "mode": "responsive",
        "width": 1930,
        "height": 523,
        "caption": "**Figure 8**: MQTT 2x Setup Page"
    }
}]$

Refer to the image below for the MQTT 3x Topic Template, which both the loraserver 3x and Built-in server use:

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1584198649\/18279\/wf3qpj37itqtmtkj1z8k.png",
        "mode": "responsive",
        "width": 1932,
        "height": 525,
        "caption": "**Figure 9**: MQTT 3x Setup Page"
    }
}]$

