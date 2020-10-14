---
type: page
title: LoRa® Channel Customizing
listed: false
slug: lora-channel-customizing
---published

## 1. LoRa® Concentrator

The LoRa® Concentrator is the heart of the LoRaWAN® Gateway. In practical applications, a Gateway will have one or more LoRa® Concentrator modules according to the actual use scenario, usually one or two.

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

| **LoRa Concentrator Unit** | **Radio Unit** | **Channel Type** | **Channel Max Number** | 
| ---- | ---- | ---- | ---- | 
|  |  | MultiSF Channel | 5 | 
| LoRa Concentrator 0 | Radio 0 | LoRa Standard Channel (LoRa Std) | 1 | 
|  |  | FSK | 1 | 
|  |  | MultiSF Channel | 5 | 
| LoRa Concentrator 1 | Radio 1 | LoRa Standard Channel (LoRa Std) | 1 | 
|  |  | FSK | 1 | 


## 2. Radio Parameter Setting

We are going to use the EU868 band as an example, in order to explain how to set the channels in **Advanced mode**. We are going to use the channels allocated for use by TTN, thus the following 8 channels:

| **Radio Unit** | **Frequency** [MHz] | 
| ---- | ---- | 
| Radio 0 | 867.1<br>867.3<br>867.5<br>867.7<br>867.9 | 
| Radio 1 | 868.1<br>868.3<br>868.5 | 


Thus, we have the following settings

| **Radio Unit** | **Frequency** [Hz] | 
| ---- | ---- | 
| Radio 0 Center Frequency | 867500000 | 
| Radio 1 Center Frequency | 868500000 | 
| Minimum Tx Frequency | 863000000 | 
| Maximum Tx Frequency | 870000000 | 


Using the parameters in the table above allows us to fit all 8 channels in the allocated band. Next, we will configure the channels themselves and enter them in the appropriate fields in the Concentrator tab.

## 3. Channel Setting

Now that we have the Center frequencies, we can start assigning channels. Those are 200KHz apart and are set by introducing an offset in Hz via the **If** field value. Thus we end up with the following table of the channel frequencies and the offsets we need to enter:

| **Radio Unit** | **Frequency** [Hz] | **If** (Offset in Hz) | 
| ---- | ---- | ---- | 
| Radio 0 | 867100000<br>867300000<br>867500000<br>867700000<br>867900000 | -400000<br>-200000<br>0 (Center)<br>+200000<br>+400000 | 
| Radio 1 | 868100000<br>868300000<br>868500000 | -400000<br>-200000<br>0 (Center) | 


After Entering the data from the table above the Panel looks as the one in Figure 1. Note that we have also entered the LoRa® STD and FSK channels (optional).

We need only enter the parameters in the panel as in Figure 1:

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1580556387\/16620\/mb6ipmkmxj3i1egvr5ke.jpg",
        "mode": "responsive",
        "width": 984,
        "height": 492,
        "caption": "**Figure 1**: Concentrator 0 Channel panel"
    }
}]$

Here is the explanation of the all the fields in the panel:

| **Parameters** | **Meaning** | 
| ---- | ---- | 
| Chan. ID | Unique identifier of the channel (8 Multi-SF Channels, 1 LoRa Standard, 1 FSK) | 
| Enable | Slider for turning a channel on/off | 
| Radio | The Radio the channel will be assigned to (max 5 per Radio) | 
| If [Hz] | The frequency offset from the center frequency for the given channel | 
| Freq [Hz] | The resulting frequency for the channel after summing the center frequency with the **If** field value | 
| Bandwidth [KHz] | This is only selectable for the LoRa Standard and FSK channels. The MultiSF are static | 
| Datarate | Essentially this is the Spreading Factor (SF) as it is directly related to the bitwise data rate. The MultiSF channels can dynamically use any of the available SFs (SF7 – SF12). The Standard LoRa® channel has to have a single value assigned (SF7 - SF12). The FSK channel has a field with a numeric value to be entered in _bps._<br><br>In order to have each channel at the desired frequency the user needs to set the appropriate offset from the central frequency. This way you can end up with a number of channels spread above and below the center frequency | 


Remember to click **Save & Apply** and you are done.

