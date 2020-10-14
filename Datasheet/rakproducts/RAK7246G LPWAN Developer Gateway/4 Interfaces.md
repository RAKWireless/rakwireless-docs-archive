---
type: page
title: Interfaces
listed: false
slug: interfaces-rak7246g
---published

### RAK2246 Concentrator

The concentrator is available with an SPI interface:

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1582527159\/26045\/qdr3oj29xkjdfu0a3bys.jpg",
        "mode": "300",
        "width": 600,
        "height": 336,
        "caption": "**Figure 1:** RAK2246 Bottom View"
    }
}]$

### SX1308

The RAK2246 includes Semtech’s SX1308, which is a digital baseband chip including a massive digital signal processing engine specifically designed to offer breakthrough gateway capabilities in the worldwide ISM band. 

The SX1308 is a smart baseband processor for long range ISM communication. In the receiver part, it receives I and Q digitized bit stream for one or two receivers (SX1257), demodulates these signals using several demodulators, adapting the demodulators settings to the received signal and stores the received demodulated packets in a FIFO to be retrieved from a host system (PC, MCU). In the transmitter part, the packets are modulated using a programmable (G)FSK/LoRa® modulator and sent to one transmitter (SX1257). Received packets can be time-stamped using a GPS PPS input. 

The SX1308 has an internal control block that receives microcode from the host system (PC, MCU). The microcode is provided by Semtech as a binary file to load into the SX1308 at power-on (_see Semtech application support for more information)._

The control of the SX1308 by the host system (PC, MCU) is made using a Hardware Abstraction Layer (HAL). The Hardware Abstraction Layer source code is provided by Semtech and can be adapted by the host system developers. 

It is highly
recommended to utilize the latest HAL as provided by Semtech on [https://github.com/Lora-net](https://github.com/Lora-net)

### Block Diagram

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1586178784\/26045\/lwlwm5p9t7vg7oshxox0.jpg",
        "mode": "responsive",
        "width": 2191,
        "height": 1187,
        "caption": "**Figure 2:** Block Diagram"
    }
}]$

The SX1308 digital baseband chip contains 10 programmable reception paths. Those paths have differentiated levels of programmability and allow for different use cases. It is important to understand the differences between those demodulation paths to make the best possible use of the system.

### IF8 LoRa® channel

This channel is connected to one SX1257 using any arbitrary intermediate frequency within the allowed range. This channel is LoRa® only. The demodulation bandwidth can be configured to be 125, 250 or 500 kHz. The data rate can be configured to any of the LoRa® available data rates (SF7 to SF12), but as opposed to the IF0 to IF7 channels, only the configured data rate will be demodulated. This channel is intended to serve as a high speed backhaul link to other gateways or infrastructure equipment. This demodulation path is compatible with the signal transmitted by the SX1272 and SX1276 chip family.

### IF9 (G)FSK channel

The IF9 channel is connected to a (G)FSK demodulator. The channel bandwidth and bit rate can be adjusted. This demodulator offers a very high level of configurability, going well beyond the scope of this document. The demodulator characteristics are essentially the same as the (G)FSK demodulator implemented in the SX1232 and SX1272 Semtech chips. This demodulation path can demodulate any legacy FSK or GFSK formatted signal.

### IF0 to IF7 LoRa® channels

These channels are connected to one SX1257. The channel bandwidth is 125 kHz and cannot be modified or configured. Each channel’s IF frequency can be individually configured. On each of these channels any data rate can be received without prior configuration. 

Several packets using different data rates (different SF) may be demodulated simultaneously even on the same channel. Those channels are intended to be used for a massive asynchronous star network of 1000’s of sensor nodes. Each sensor may use a random channel (amongst IF0 to IF7) and a different data rate for any transmission. 

Sensors located near the Gateway will typically use the highest possible data rate in the fixed 125 kHz channel bandwidth (e.g. 6 kbit/s) while sensors located far away will use a lower data rate down to 300 bit/s (the minimum LoRa® data rate in a 125 kHz channel). 

The SX1308 digital baseband chip scans the 8 channels (IF0 to IF7) for preambles of all data rates at all times. 

The chip is able to demodulate simultaneously up to 8 packets. Any combination of spreading factor and intermediate frequency for up to 8 packets is possible (e.g. one SF7 packet on IF0, one SF12 packet on IF7 and one SF9 packet on IF1 simultaneously). 

The SX1308 can detect simultaneously preambles corresponding to all data rates on all IF0 to IF7 channels. However, it cannot demodulate more than 8 packets simultaneously. This is because the SX1308 architecture separates the preamble detection and signal acquisition task from the demodulation process. The number of simultaneously demodulated packets (in this case 8) is an arbitrary system parameter and may be set to other values for a customer specific circuit. 

The unique multi data-rate multi-channel demodulation capacity SF7 to SF12 and of channels IF0 to IF7 allows innovative network architectures to be implemented.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1590743031\/26045\/pl2e6ny3nbtjyyqg7lu9.png",
        "mode": "responsive",
        "width": 6222,
        "height": 3574,
        "caption": "**Figure 3:** LoRa\u00ae Channel"
    }
}]$

## External Module Interfaces

### SPI

The PINs on the connector provide an SPI connection, which allows direct access to the SX1308 SPI interface. This gives the target system the possibility to use existing SPI interfaces to communicate.

$plugin[{
    "type": "callout",
    "data": {
        "text": "After powering up RAK2246, it is required to reset\nSX1308 via PIN 11.",
        "type": "info",
        "title": "Note"
    }
}]$

### UART and I2C

The PINs on the bottom side provide an UART connection and I2C connection, which allows direct access to the GPS module. The 1PPS has been connected to the SX1308 internally.

### Digital IOs

There are two digital IO PINs, which give the user an interface to reset the GPS module or set it into standby mode.

