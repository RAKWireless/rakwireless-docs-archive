---
type: page
title: Interfaces
listed: false
slug: interfaces-rak831
---published

## SX1301

The RAK831 includes Semtech’s SX1301 which is a digital baseband chip which includes a massive digital signal processing engine specifically designed to offer breakthrough gateway capabilities in the ISM bands worldwide. SX1301 integrates the LoRa® concentrator IP.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1587100967\/17920\/ovbhkvsg4w0jzsc0oesd.jpg",
        "mode": "responsive",
        "width": 2864,
        "height": 1547,
        "caption": "**Figure 1:**  SX1301 Chip Block Diagram"
    }
}]$

The SX1301 is a smart baseband processor for long range ISM communication. In the receiver part, it receives I and Q digitized bit stream for one or two receivers (SX1257), demodulates these signals using several demodulators, adapting the demodulators settings to the received signal and stores the received demodulated packets in a FIFO to be retrieved from a host system (PC, MCU). In the transmitter part, the packets are modulated using a programmable (G)FSK/LoRa® modulator and sent to one transmitter (SX1257). Received packets can be time-stamped using a GPS PPS input.

The SX1301 has an internal control block that receives microcode from the host system (e.g. PC, MCU). The microcode is provided by Semtech as a binary file to load into the SX1301 at power-on (see Semtech application support for more information).

The control of the SX1301 by the host system (PC, MCU) is made using a Hardware Abstraction Layer (HAL). The Hardware Abstraction Layer source code is provided by Semtech and can be adapted by the host system developers.

It is highly recommended to fully re-use the latest HAL as provided by Semtech on [https://github.com/Lora-net](https://github.com/Lora-net).

### Block Diagram

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1564063393\/17920\/gurshves2hi1e8xoqiro.png",
        "mode": "responsive",
        "width": 1246,
        "height": 836,
        "caption": "**Figure 2:** RAK831 LPWAN Gateway Block Diagram"
    }
}]$

The SX1301 digital baseband chip contains ten (10) programmable reception paths. These paths have differentiated levels of programmability and allow different use cases. It is important to understand the differences between these demodulation paths to make the best possible use from the system.

### IF8 LORA® channel

This channel is connected to one SX1257 using any arbitrary intermediate frequency within the allowed range. This channel is LoRa® only. The demodulation bandwidth can be configured to be 125, 250 or 500 kHz. The data rate can be configured to any of the LoRa® available data rates (SF7 to SF12) but, as opposed to IF0 to IF7, only the configured data rate will be demodulated. This channel is intended to serve as a high speed backhaul link to other gateways or infrastructure equipment. This demodulation path is compatible with the signal transmitted by the SX1272 and SX1276 chip family.

### IF9 (G) FSK channel

The IF9 channel is connected to a GFSK demodulator. The channel bandwidth and bit rate can be adjusted. This demodulator offers a very high level of configurability, going well beyond the scope of this document. The demodulator characteristics are essentially the same than the GFSK demodulator implemented on the SX1232 and SX1272 Semtech chips. This demodulation path can demodulate any legacy FSK or GFSK formatted signal.

### IF0 to IF7 LORA® channels

Those channels are connected to one SX1257. The channel bandwidth is 125 kHz and cannot be modified or configured. Each channel IF frequency can be individually configured. On each of those channels any data rate can be received without prior configuration.

Several packets using different data rates (different spreading factors) may be demodulated simultaneously even on the same channel. Those channels are intended to be used for a massive asynchronous star network of 10000’s of sensor nodes. Each sensor may use a random channel (amongst IF0 to IF7) and a different data rate for any transmission.

Sensors located near the gateway will typically use the highest possible data rate in the fixed 125 kHz channel bandwidth (e.g. 6 kbit/s) while sensors located far away will use a lower data rate down to 300 bit/s (minimum LoRa® data rate in a 125 kHz channel).

The SX1301 digital baseband chip scans the 8 channels (IF0 to IF7) for preambles of all data rates at all times.

The chip is able to demodulate simultaneously up to 8 packets. Any combination of spreading factor and intermediate frequency for up to 8 packets is possible (e.g. one SF7 packet on IF0, one SF12 packet on IF7 and one SF9 packet on IF1 simultaneously).

The SX1301 can detect simultaneously preambles corresponding to all data rates on all IF0 to IF7 channels. However, it cannot demodulate more than 8 packets simultaneously. This is because the SX1301 architecture separates the preamble detection and signal acquisition task from the demodulation process. The number of simultaneously demodulated packets (in this case 8) is an arbitrary system parameter and may be set to other values for a customer specific circuit.

The unique multi data-rate multi-channel demodulation capacity SF7 to SF12 and of channels IF0 to IF7 allows innovative network architectures to be implemented.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1586328062\/17920\/t6dyb6uwey9yfsqaeg7c.jpg",
        "mode": "responsive",
        "width": 6222,
        "height": 3574,
        "caption": null
    }
}]$

## External Module Connector

### SPI

The connector on the bottom side provides an SPI connection, which allows direct access to the Sx1301 SPI interface. This gives the target system the possibility to use existing SPI interfaces to communicate.

After powering up RAK831 ,it is required to **reset** SX1301 via **PIN 19.** If the HAL driver from Github is used this functionality is already implemented.

### GPS PPS

In case of available PPS signals in the target system, it is possible to connect this available signal to the appropriate pin at the connector.

### Digital IOs

There are five GPIOs of the Sx1301 available, which gives the user some possibilities to get information about the system status. Theses pins are the same, as they are used for the LEDs on the RAK831 .

As default setting the LEDs 

1. Backhaul packet
2. TX packet
3. RX Sensor packet
4. RX FSK packet
5. RX buffer not empty
6. Power

