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
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1564893426\/18282\/nr18ncglba5nmitmc50w.jpg",
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
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1564893459\/18282\/u2sszilocveei3r8pzdt.jpg",
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
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1564893519\/18282\/ly6qo6gz43ntard10dip.jpg",
        "mode": "responsive",
        "width": 1191,
        "height": 254,
        "caption": "**Figure 3.** Tabular Individual Channel Setting Panel"
    }
}]$

The channel setting page is tabulated. Each column of the table represents a channel. Each LoRa Concentrator supports **eight multi-rate channels (MultiSF)**, **one standard LoRa channel (LoRa std) and one FSK channel**. By setting the center frequency of Radio 0 or 1, and then selecting the corresponding frequency offset, a certain frequency value can be determined.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1564893646\/18282\/jcgaohuarsxjoyskslzt.png",
        "mode": "responsive",
        "width": 848,
        "height": 487,
        "caption": null
    }
}]$

### Example of Channel Settings

Here we take TTN frequency plans as an example.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1564893676\/18282\/pxs0vcui9u9g7xwlszb6.png",
        "mode": "responsive",
        "width": 849,
        "height": 439,
        "caption": null
    }
}]$

- **Setup Radio central frequency band**

Each Radio allocates 8 multi-rate LoRa channels, ranging from 1 to 4 belongs to **Radio 0**, the central frequency is **486,600,000** Hz. 5-8 belongs to **Radio 1**, the central frequency is **487,400,000** Hz.

- **Setup the transmission frequency**

It is necessary to ensure that all frequency points of downlink channel are included in the transmitting Radio, so Radio 0 Tx Min is set to 506 000 000, Radio 1 Tx Max is set to 508 600 000. It is suggested that the minimum frequency should be less than the effective minimum value (e.g. 5067 000 000 000 000) and more than 500 KHz in the using frequency, and the maximum value should be greater than the effective maximum value (e.g. 5081 000 000 000) and more than 500 KHz in the using frequency.

- **Setup channels**

**MultiSF 0 ~ 3** Radio is set to **Radio 0**, and If frequency offset is set to -300000/- 100000/100000/300000.

**MultiSF 4 ~ 7** Radio is set to **Radio 1**, and If frequency offset is set to -300000/- 100000/100000/300000.

LoRa Std and FSK channels shutdown

- **Setup completed, click Save & Apply**

