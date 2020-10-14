---
type: page
title: Web Channel Customizing
listed: true
slug: web-channel-customizing
---published

## 1. LoRa Concentrator

LoRa Concentrator is the basic unit of a gateway. In practical application, a gateway will have one or more LoRa Concentrators according to the actual use scenario, usually one or two.

Each LoRa Concentrator can simultaneously monitor eight multi-rate LoRa channels (MultiSF Channel, DR0-DR5), one standard LoRa channel and one FSK channel, totaling 10 channels. At the same time, a LoRa Concentrator contains two radio units, **Radio 0** and **Raido 1**, respectively. Radio0 can be used to receive and transmit radio signals, while Radio1 is only used to receive radio signals.

Each Radio can monitor up to five channels (including MultiSF channel, LoRa Std channel, FSK channel). Users can assign channels to two Radio units according to the actual needs.

$plugin[{
    "type": "callout",
    "data": {
        "text": "Each country has different band parameters and different number of channels. Be sure to configure the gateway according to the actual parameters.",
        "type": "warning",
        "title": "Note:"
    }
}]$

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1561475571\/16620\/fethhxtaoikz4uwmtyv7.jpg",
        "mode": "responsive",
        "width": 981,
        "height": 848,
        "caption": "**Figure 1**. LoRa Concentrator Channel Classification"
    }
}]$

## 2. Radio Parameter Setting

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1561475785\/16620\/hhybcpsfteezfjwou3ls.jpg",
        "mode": "600",
        "width": 886,
        "height": 320,
        "caption": "**Figure 2.** LoRa Concentrator Radio Frequency Editing Panel"
    }
}]$

- **Radio0 Freq**. : LoRa Concentrator Radio0 Receiving center frequency
- **Radio0 Tx Freq. Min**：LoRa Concentrator Radio0 minimum transmit frequency
- **Radio0 Tx Freq. Max** : LoRa Concentrator Radio0 Maximum transmit frequency
- **Radio1 Freq**. : LoRa Concentrator Radio Receiving center frequency

$plugin[{
    "type": "callout",
    "data": {
        "text": "1. Only Radio 0 supports transmitting signals in LoRa Concentrator;\n2. LoRa Concentrator 1 (LoRa1) transmitter frequency range of channel is consistent with that of LoRa Concentrator 0 (LoRa0), and the LoRa0 is not allowed to be modified.",
        "type": "info",
        "title": "Note:"
    }
}]$

## 3. Channel Setting

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1561477460\/16620\/opdbszemszjg69q9ldzk.jpg",
        "mode": "responsive",
        "width": 1191,
        "height": 254,
        "caption": "**Figure 3.**  Tabular Individual Channel Setting Panel"
    }
}]$

The channel setting page is tabulated. Each column of the table represents a channel. Each LoRa Concentrator supports **eight multi-rate channels (MultiSF)**, **one standard LoRa channel (LoRa std) and one FSK channel**. By setting the center frequency of Radio 0 or 1, and then selecting the corresponding frequency offset, a certain frequency value can be determined.

| Parameters | Description | 
| ---- | ---- | 
| Chan. ID | Channel ID of LoRa Concentrator | 
| Enable | Enabling or Disabling Channels | 
| Radio | Radio0 or Radio1 of the LoRa Concentrator | 
| If | The offset relative to the central frequency of Radio 0 or Radio 1.This parameter and the center frequency of Radio determine the frequency of the&nbsp;current channel. | 
| Freq. | The central frequency of the current channel. Set by Raido and If&nbsp;parameters. | 
| Bandwidth | Channel bandwidth. MultiSF LoRa channel:125 KHz which cannot be modified.&nbsp;LoRa Std channel and FSK channel are set by users themselves. | 
| Datarate | Channel rate. MultiSF LoRa channel is a multi-rate channel. It monitors&nbsp;the SF7~SF12 rate at the same time, and it can not be modified. LoRa Std&nbsp;channel and FSK channel are set by users themselves. | 


### Example of Channel Settings

Here we take TTN frequency plans as an example.

| Uplink: | Downlink: | 
| ---- | ---- | 
| 1.&nbsp; &nbsp;486.3- SF7BW125 to SF12BW1251.&nbsp; &nbsp; | 1.&nbsp; &nbsp;506.7- SF7BW125 to SF12BW125 | 
| 2.&nbsp; &nbsp;486.5- SF7BW125 to SF12BW125 | 2.&nbsp; &nbsp;506.9- SF7BW125 to SF12BW125 | 
| 3.&nbsp; &nbsp;486.7- SF7BW125 to SF12BW125 | 3.&nbsp; &nbsp;507.1- SF7BW125 to SF12BW125 | 
| 4.&nbsp; &nbsp;486.9- SF7BW125 to SF12BW125 | 4.&nbsp; &nbsp;507.3- SF7BW125 to SF12BW125 | 
| 5.&nbsp; &nbsp;487.1- SF7BW125 to SF12BW125 | 5.&nbsp; &nbsp;507.5- SF7BW125 to SF12BW125 | 
| 6.&nbsp; &nbsp;487.3- SF7BW125 to SF12BW125 | 6.&nbsp; &nbsp;507.7- SF7BW125 to SF12BW125 | 
| 7.&nbsp; &nbsp;487.5- SF7BW125 to SF12BW125 | 7.&nbsp; &nbsp;507.9- SF7BW125 to SF12BW125 | 
| 8.&nbsp; &nbsp;487.7- SF7BW125 to SF12BW125 | 8.&nbsp; &nbsp;508.1- SF7BW125 to SF12BW125 | 
|  | 9.&nbsp; &nbsp;505.3- SF12BW125 (RX2 downlink only) | 


- **Setup Radio central frequency band**

Each Radio allocates 8 multi-rate LoRa channels, ranging from 1 to 4 belongs to **Radio 0**, the central frequency is **486,600,000** Hz. 5-8 belongs to **Radio 1**, the central frequency is **487,400,000** Hz. 

- **Setup the transmission frequency**

It is necessary to ensure that all frequency points of downlink channel are included in the transmitting Radio, so Radio 0 Tx Min is set to 506 000 000, Radio 1 Tx Max is set to 508 600 000. It is suggested that the minimum frequency should be less than the effective minimum value (e.g. 5067 000 000 000 000) and more than 500 KHz in the using frequency, and the maximum value should be greater than the effective maximum value (e.g. 5081 000 000 000) and more than 500 KHz in the using frequency. 

- **Setup channels**

**MultiSF 0 ~ 3** Radio is set to **Radio 0**, and If frequency offset is set to -300000/- 100000/100000/300000.

**MultiSF 4 ~ 7** Radio is set to **Radio 1**, and If frequency offset is set to -300000/- 100000/100000/300000.

LoRa Std and FSK channels shutdown 

- **Setup completed, click Save & Apply**

