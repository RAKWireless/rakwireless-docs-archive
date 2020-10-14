---
type: page
title: LoRa® Channel Customizing
listed: false
slug: lora-channel-customizing
---published

## 1. LoRa® Concentrator

The LoRa® Concentrator is the heart of the LoRaWAN™ Gateway. In practical applications, a Gateway will have one or more LoRa® Concentrator modules according to the actual use scenario, usually one or two.

Each LoRa® Concentrator can simultaneously monitor eight multi-rate LoRa® channels (MultiSF Channel, DR0-DR5), one standard LoRa® channel and one FSK channel, totaling 10 channels. At the same time, a LoRa® Concentrator contains two radio units, **Radio 0** and **Raido 1**, respectively. Radio 0 can be used to receive and transmit, while Radio 1 is only used to receive.

Each Radio can monitor up to five channels (including MultiSF channels, LoRa® Std channel, FSK channel). Users can assign channels to the two Radio units according to their actual needs.

$plugin[{
    "type": "callout",
    "data": {
        "text": "Each country has different frequency band parameters and different number of channels. Be sure to configure the Gateway in accordance with the parameters of your region.",
        "type": "warning",
        "title": "Note:"
    }
}]$

| **LoRa® Concentrator Unit** | **Radio Unit** | **Channel Type** | **Channel Max Number** | 
| ---- | ---- | ---- | ---- | 
|  |  | MultiSF Channel | 5 | 
| LoRa® Concentrator 0 | Radio 0 | LoRa®Standard Channel (LoRa® Std) | 1 | 
|  |  | FSK | 1 | 
|  |  | MultiSF Channel | 5 | 
| LoRa® Concentrator 1 | Radio 1 | LoRa® Standard Channel (LoRa® Std) | 1 | 
|  |  | FSK | 1 | 


## 2. Radio Parameter Setting

We are going to use the EU868 band as an example, in order to explain how to set the channels in **Advanced mode**. As the RAK7249 is a Gateway capable of working with dual LoRa® Concentrators it can support up to 16 LoRa® Channels. For this reason, we are going to divulge from the standard 8 Channel plans (for example the one TTN is using). We are going to configure the Gateway to work with a custom scheme of 16 channels. Those are just to explain how to configure the frequencies and are not in any way what you should be used in practice (even though they are valid).

We have decided on the following 16 channels:

| **Radio Unit** | **Frequency** [MHz] | 
| ---- | ---- | 
| Concentrator 0 | 866.9<br>867.1<br>867.3<br>867.5<br>867.7<br>867.9<br>868.1<br>868.3 | 
| Concentrator 1 | 868.5<br>868.7<br>868.9<br>869.1<br>869.3<br>869.5<br>869.7<br>869.9 | 


Based on the above we need to allocate up to 5 channels per Radio and choose the center frequency. See the tables below for those settings for the two Concentrators.

**Below are the settings for Concentrator 0:**

| **Radio Unit** | **Frequency** [Hz] | 
| ---- | ---- | 
| Radio 0 Center Frequency | 867300000 | 
| Radio 1 Center Frequency | 868300000 | 
| Minimum Tx Frequency | 863000000 | 
| Maximum Tx Frequency | 870000000 | 


**Below are the settings for Concentrator 1:**

| **Radio Unit** | **Frequency** [Hz] | 
| ---- | ---- | 
| Radio 0 Center Frequency | 868900000 | 
| Radio 1 Center Frequency | 868900000 | 


$plugin[{
    "type": "callout",
    "data": {
        "text": "In case of having a two Concentrator setup, only the first one is used for Transmitting (Downlink)",
        "type": "info",
        "title": "Info"
    }
}]$

Using the parameters in the tables above allows us to fit all 16 channels in the allocated band. Next we will configure the channels themselves and enter them in the appropriate fields in the Conventrator 0 and Concentrator 1 tabs.

## 3. Channel Setting

Now that we have the Center frequencies, we can start assigning channels. Those are 200KHz apart and are set by introducing an offset in Hz via the **If** field value. Thus, we end up with the following table of the channel frequencies and the offsets we need to enter:

**Concentrator 0:**

| **Radio Unit** | **Frequency** [Hz] | **If** (Offset in Hz) | 
| ---- | ---- | ---- | 
| Radio 0 | 866900000<br>867100000<br>867300000<br>867500000<br>867700000 | -400000<br>-200000<br>0 (Center)<br>+200000<br>+400000 | 
| Radio 1 | 867900000<br>868100000<br>868300000 | -400000<br>-200000<br>0 (Center) | 


After Entering the data from the table above the Panel looks as the one in Figure below. Note that we have also entered the LoRa® std and FSK channels (not mandatory).

We need only enter the parameters in the panel as in Figure 1:

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1580556154\/18282\/k2gnxlekibbf5lpy7kbp.jpg",
        "mode": "responsive",
        "width": 984,
        "height": 492,
        "caption": "**Figure 1**: Concentrator 0 Channel panel"
    }
}]$

Here is the explanation of the all the fields in the panel:

| **Parameter** | **Meaning** | 
| ---- | ---- | 
| Chain. ID | Unique identifier of the channel (8<br>Multi-SF Channels, 1 LoRa® Standard, 1 FSK) | 
| Enable | Slider for turning a channel on/off | 
| Radio | The Radio the channel will be assigned to (max 5 per Radio) | 
| If [Hz] | The frequency offset from the center frequency for the given channel | 
| Freq [Hz] | The resulting frequency for the channel after summing the center<br>frequency with the **If** field value | 
| Bandwidth [KHz] | This is only selectable for the LoRa® Standard and FSK channels. The<br>MultiSF are static | 
| Datarate | Essentially this is the Spreading Factor (SF) as it is directly related to the bitwise data rate. The MultiSF channels can dynamically use any of the available SFs (SF7 – SF12). The Standard LoRa® channel has to have a single value assigned (SF7 - SF12). The FSK channel has a field with a numeric value to be entered in _bps._<br><br>In order to have each channel at the desired frequency the user needs to set the appropriate offset from the central frequency. This way you can end up with a number of channels spread above and below the center frequency | 


Now, we need to do the same for the second Concentrator.

**Concentrator 1:**

| Radio Unit | Frequency [Hz] | If (Offset in Hz) | 
| ---- | ---- | ---- | 
| Radio 0 | 868500000<br>868700000<br>868900000<br>869100000<br>869300000 | -400000<br>-200000<br>0 (Center)<br>+200000<br>+400000 | 
| Radio 1 | 869500000<br>869700000<br>869900000 | -400000<br>-200000<br>0 (Center) | 


$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1580556260\/18282\/z4udu9rqctif2j9d02df.jpg",
        "mode": "responsive",
        "width": 1934,
        "height": 914,
        "caption": "**Figure 2**: Concentrator 1 Channel panel"
    }
}]$

Remember to click **Save & Apply** and you are done.

