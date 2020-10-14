---
type: page
title: Source Code
listed: false
slug: source-code---rak2287-lora-gateway
---draft

The RAK2287 has an open source code available from **[here](https://github.com/RAKWireless/RAK833-LoRaGateway-RPi). **It is an open source project which is based on the latest SX1302 driver lora_gateway v5.0.1 and semtech packet_forwarder v4.0.1.

## Installation Procedure

The source code can be installed by performing these simple and easy steps. 

**1.**Download and install [Raspbian Stretch LITE](https://www.raspberrypi.org/downloads/raspbian/).

**2.**Clone the installer and start the installation.

$plugin[{
    "type": "code-block",
    "data": {
        "languageBlocks": [
            {
                "code": "$ git clone https:\/\/github.com\/RAKWireless\/RAK833-LoRaGateway-RPi.git ~\/rak833-loragateway",
                "language": "none"
            }
        ]
    }
}]$

$plugin[{
    "type": "code-block",
    "data": {
        "languageBlocks": [
            {
                "code": "$ cd ~\/rak833-loragateway",
                "language": "none"
            }
        ]
    }
}]$

$plugin[{
    "type": "code-block",
    "data": {
        "languageBlocks": [
            {
                "code": "$ sudo .\/install.sh",
                "language": "none"
            }
        ]
    }
}]$

**3.**Now you have a running gateway after restart! in addition you can check
the log info at /var/log/syslog.

Here is another very useful Github Link for RAK833, not only support the Semtech latest driver, but also doucmented a ready to use container containing the Gateway and the Network Forwarder:

- **[LoRa Gateway](https://github.com/Ellerbach/lora_gateway)**
- [**Packet Forwarder**](https://github.com/ellerbach/packet_forwarder)

---published

The RAK2287 has an open source code available from **[here](https://github.com/RAKWireless/RAK833-LoRaGateway-RPi). **It is an open source project which is based on the latest SX1302 driver lora_gateway v5.0.1 and semtech packet_forwarder v4.0.1.

## Installation Procedure

The source code can be installed by performing these simple and easy steps. 

**1.**Download and install [Raspbian Stretch LITE](https://www.raspberrypi.org/downloads/raspbian/).

**2.**Clone the installer and start the installation.

$plugin[{
    "type": "code-block",
    "data": {
        "languageBlocks": [
            {
                "code": "$ git clone https:\/\/github.com\/RAKWireless\/RAK833-LoRaGateway-RPi.git ~\/rak833-loragateway",
                "language": "none"
            }
        ]
    }
}]$

$plugin[{
    "type": "code-block",
    "data": {
        "languageBlocks": [
            {
                "code": "$ cd ~\/rak833-loragateway",
                "language": "none"
            }
        ]
    }
}]$

$plugin[{
    "type": "code-block",
    "data": {
        "languageBlocks": [
            {
                "code": "$ sudo .\/install.sh",
                "language": "none"
            }
        ]
    }
}]$

**3.**Now you have a running gateway after restart! in addition you can check
the log info at /var/log/syslog.

Here is another very useful Github Link for RAK833, not only support the Semtech latest driver, but also doucmented a ready to use container containing the Gateway and the Network Forwarder:

- **[LoRa Gateway](https://github.com/Ellerbach/lora_gateway)**
- [**Packet Forwarder**](https://github.com/ellerbach/packet_forwarder)

