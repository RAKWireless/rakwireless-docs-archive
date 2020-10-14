---
type: page
title: Spectrum Settings
listed: true
slug: spectrum-settings-eu868
---published

Let us take as an example the **EU863-870 frequency band**. When accessing the Web Management Platform, there is a template for it that you can
import directly which would not need to set every channel manually. However, the way it has been configured is in accordance with principles that apply for any band.

## Setting the Center Frequencies

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1583203886\/26653\/wbgj7m0kijxnxdtdkhij.png",
        "mode": "600",
        "width": 732,
        "height": 341,
        "caption": "**Figure 1**: Default Frequency Template in the Web Management Platform"
    }
}]$

**1**.Set the Center Frequencies for the two Radios

| **RX Channels** | **Frequency** (Hz) | 
| ---- | ---- | 
| **Radio 0** Center Frequency | 867500000 (867.5 MHz) | 
| **Radio 1** Center Frequency | 868500000 (868.5 MHz) | 


**2**.Set the **Minimum** and **Maximum** frequency range of Radio

| **TX Channels** | **Frequency** (Hz) | 
| ---- | ---- | 
| **Radio 0** Tx Minimum Frequency | 863000000 (863 MHz) | 
| **Radio 1** Tx Maximum Frequency | 870000000 (870 MHz) | 


## Selecting the Radios/Channels

Let us have a summary of the parameters that can be seen in the image below, which is below the Radio
0 and Radio 1 frequency fields we talked about in the previous section.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1583208845\/26653\/a5zrosrqmo3ko7lmti0r.png",
        "mode": "responsive",
        "width": 982,
        "height": 491,
        "caption": "**Figure 2**: Concentrator Channel Panel"
    }
}]$

| **Chain. ID** | Unique identifier of the channel (8 Multi-SF Channels, 1 LoRa Standard, 1 FSK) | 
| ---- | ---- | 
| **Enable** | Slider for turning a channel on/off | 
| **Radio** | The Radio the channel will be assigned to (max 5 per Radio) | 
| **If** [Hz] | The frequency offset from the center frequency for the given channel | 
| **Freq** [Hz] | The resulting frequency for the channel after summing the center frequency with the __If__ field value | 
| **Bandwidth** [KHz] | This is only selectable for the LoRa® Standard and FSK channels. The MultiSF are static | 
| **Datarate** | Essentially this is the **Spreading Factor (SF)** as it is directly related to the bitwise data rate. The MultiSF channels can dynamically use any of the available SFs (SF7 – SF12). The Standard LoRa® channel has to have a single value assigned (SF7 - SF12). The FSK channel has a field with a numeric value to be entered in **bps**. <br>In order to have each channel at the desired frequency the user needs to set the appropriate offset from the central frequency. This way you can end up with a number of channels spread above and below the center frequency | 


## Setting the Frequency Offset

The (The Things Network) TTN Frequency Plan for the EU863-868 region is listed below. You may check the (The Things Network) TTN [documentation](https://www.thethingsnetwork.org/docs/lorawan/frequency-plans.html) for other Frequency Plans.

**Uplink**:

1. 868.1 - SF7BW125 to SF12BW125
2. 868.3 - SF7BW125 to SF12BW125 and SF7BW250
3. 868.5 - SF7BW125 to SF12BW125
4. 867.1 - SF7BW125 to SF12BW125
5. 867.3 - SF7BW125 to SF12BW125
6. 867.5 - SF7BW125 to SF12BW125
7. 867.7 - SF7BW125 to SF12BW125
8. 867.9 - SF7BW125 to SF12BW125
9. 868.8 - FSK

**Downlink**:

- Uplink channels 1-9 (RX1)
- 869.525 - SF9BW125 (RX2 downlink only)

With the Frequency Plan provided by The Things Network (TTN) it is now easy to see why we have chosen the values shown in **Figure 1**: Default Frequency Template in the Web Management Platform. Two (2) things should be taken into account.

- We need to cover the whole spectrum for the **Uplink**, from the lowest to the highest frequency.
- Additionally, we need to have the 5 channels per radio to be as close as possible with each other. So, we would group the Radios by frequency and not by number of channels.

For the aforementioned reason, **TTN channels 1,2,3,9** should be assigned to the **first Radio (Radio 0)** (additionally there is one more channel, number 2, but with SF7 and 250KHz bandwidth). The **second Radio (Radio 1)** can get the other **five channels 4,5,6,7,8**.

Now, in order to keep the bandwidth tight, we pick a channel in each of the two Radio ranges
as close as possible to the middle. Ideally, as we have five channels, this would be the 3rd one. The **center frequency channels** are than **TTN channels 3 and 6**. This leads us to the center frequencies
that are in **Figure 1**: Default Frequency Template in the Web Management Platform. As for the Uplink, we simply need to cover the whole band, in this case
863 MHz to 870 MHz.

## Offset Frequency Calculation

Now we can start calculating the frequency offset we need to have from the center frequency
for each channel. We will use the following formula:

$plugin[{
    "type": "callout",
    "data": {
        "text": "**If** = **MultiSF** - **Radio Freq**",
        "type": "info",
        "title": "Equation:"
    }
}]$

### RADIO 1

**MultiSF 0** = TTN 1 = 868100000 Hz

- If 0 = MultiSF 0 - Radio 1 Freq = 868100000 – 868500000 = -400000 Hz

**MultiSF 1** = TTN 2 = 868300000 Hz

- If 1 = MultiSF 1 - Radio 1 Freq = 868300000 – 868500000 = -200000 Hz

**MultiSF 2** = TTN 3 = 868500000 Hz

- If 2 = MultiSF 2 - Radio 1 Freq = 868500000 – 868500000 = 0 Hz

Those are the first 3 TTN channels. The next channel however is at a lower frequency than all
the previous ones. Thus, it will be assigned to Radio 0

### RADIO 0

**MultiSF 3** = TTN 4 = 867100000 Hz

- If 3 = MultiSF 3 - Radio 0 Freq = 867100000 – 867500000 = -400000 Hz

**MultiSF 4** = TTN 5 = 867300000 Hz

- If 4 = MultiSF 4 - Radio 0 Freq = 867300000 – 867500000 = -200000 Hz

**MultiSF 5** = TTN 6 = 867500000 Hz

- If 5 = MultiSF 5 - Radio 0 Freq = 867500000 – 867500000 = 0 Hz

**MultiSF 6** = TTN 7 = 867700000 Hz

- If 6 = MultiSF 6 - Radio 0 Freq = 867700000 – 867500000 = 200000 Hz

**MultiSF 7** = TTN 8 = 867900000 Hz

- If 7 = MultiSF 7 - Radio 0 Freq = 867900000 – 867500000 = 400000 Hz

Finally we have all the If frequency values and we only need plug them in the fields to get the
TTN EU863-868 Frequency Plan through Web Management Platform

$plugin[{
    "type": "callout",
    "data": {
        "text": "Do not forget to manually set the Bandwidth and DataRate of the LoRa std at 250K Hz (SF7) and FSK at 125K Hz (50000 bps).",
        "type": "info",
        "title": "Note:"
    }
}]$

This concludes setting up the two Radios with the appropriated frequencies, bandwidths and
data rates.

