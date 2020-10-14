---
type: page
title: Setup the External MQTT Broker
listed: true
slug: setup-the-external-mqtt-broker
---published

This section provides the procedure in setting the external MQTT Broker for your Application Setup.

## Preparing the Raspberry Pi

$plugin[{
    "type": "callout",
    "data": {
        "text": "We are going to use going to use a **Raspberry Pi 3B+** for this tutorial, as the device that is going to be hosting Mosquitto (a popular MQTT broker).",
        "type": "info",
        "title": "Note:"
    }
}]$

The following items listed below with its download links for the tools and files needed for this demonstration:

- [Raspbian Buster Lite Image](https://www.raspberrypi.org/downloads/raspbian/)
- [Balena Etcher Tool](https://www.balena.io/etcher/)
- [PuTTY SSH Client](https://www.chiark.greenend.org.uk/~sgtatham/putty/latest.html)

1.Download the Raspbian Buster Lite image and flash it into your SD Card using the Balena Etcher. You can follow the steps provided in the [auto$](/rak2245-pi-hat-edition-lorawan-gateway-concentrator-module/device-firmware-setup) document. Once done, plug the SD card into the **Raspberry Pi 3B+** SD card slot and power it.

$plugin[{
    "type": "callout",
    "data": {
        "text": "It is highly recommended to follow the configurations of [Raspberry Pi headless](https:\/\/www.raspberrypi.org\/documentation\/configuration\/wireless\/headless.md).",
        "type": "info",
        "title": "Note:"
    }
}]$

2.Using the PuTTY SSH client, connect to the Raspberry Pi 3B+ with the following credentials:

- **Username**: pi
- **Password**: raspberry

3.Execute the following command and note the IP address of the interface you will be using to connect to the network. You will need this, as it will be the address for your MQTT Broker when configuring the Gateway:

$plugin[{
    "type": "code-block",
    "data": {
        "languageBlocks": [
            {
                "code": "ifconfig",
                "language": "none"
            }
        ]
    }
}]$

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1580972353\/23155\/zcd2yvspvxiphkvmkifj.jpg",
        "mode": "responsive",
        "width": 870,
        "height": 552,
        "caption": "**Figure 1**: Raspberry Pi interfaces"
    }
}]$

## Installing Mosquitto

**1**.Install the MQTT Broker (Mosquitto) via the command:

$plugin[{
    "type": "code-block",
    "data": {
        "languageBlocks": [
            {
                "code": "sudo apt install mosquitto mosquitto-clients",
                "language": "none"
            }
        ]
    }
}]$

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1580973008\/23155\/ixbl2ek8ayybbhe52xap.jpg",
        "mode": "responsive",
        "width": 869,
        "height": 527,
        "caption": "**Figure 2**: Mosquitto installation"
    }
}]$

**2**.Mosquitto clients help us easily test MQTT through a command line utility. We will use two command windows; one to subscribe to a topic and one to publish a message to it. Those will be explained in detail further in the tutorial.

$plugin[{
    "type": "callout",
    "data": {
        "text": "This command is not mandatory, however it is recommended as it creates a mosquitto service that will run the broker on startup.",
        "type": "info",
        "title": "Note:"
    }
}]$

$plugin[{
    "type": "code-block",
    "data": {
        "languageBlocks": [
            {
                "code": "sudo systemctl enable mosquitto.service",
                "language": "none"
            }
        ]
    }
}]$

## Publish to the MQTT Broker

We will now then configure the Gateway to connect to our external MQTT broker. For the purpose of this example, we are going to use the built-in LoRa® Server.

**1**.First go to the Packet Forwarder Tab and choose Built-in LoRa® Server as your Protocol:

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1580973267\/23155\/lc0cfzutfozzjnrw9m7j.jpg",
        "mode": "responsive",
        "width": 869,
        "height": 421,
        "caption": "**Figure 3**: Protocol selection"
    }
}]$

**2**.Make sure you have the LoRa® Network Server **Enabled** in the General tab:

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1580973355\/23155\/nc3w6wzrwdu8lhk6vywa.jpg",
        "mode": "responsive",
        "width": 868,
        "height": 453,
        "caption": "**Figure 4**: Built-in LoRa\u00ae Server activation"
    }
}]$

**3**.Add Your Gateway in the Gateway tab if you haven’t done so already. You can also add multiple gateways depending on your preference.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1580973580\/23155\/lcyrxuegza65jzkpdvo8.jpg",
        "mode": "responsive",
        "width": 873,
        "height": 446,
        "caption": "**Figure 5**: LoRa\u00ae Server Gateway configuration"
    }
}]$

**4**.Finally, go to the **Global Integration** tab and enter the address where you have your Mosquitto instance running in the MQTT Broker Address field leaving the Port with the default **1883** value.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1580974748\/23155\/ni4gyww0ovpmkbcp5bbz.jpg",
        "mode": "responsive",
        "width": 868,
        "height": 445,
        "caption": "**Figure 6**: Setting up the Global Integration"
    }
}]$

Now that the Gateway parameters are set, we will now register your application in order to be able to send and receive data. We are going to use the **RAK811** as an example in the next sub-section.

### DOWNLINK

There is a convenient tool in the Built-in LoRa® Server for sending a Downlink frame.

**1**.You can find it in the Device tab in the LoRa® Network Server section. You can choose your Type of frame (confirmed/unconfirmed), the Frame port and the Hex Data shown in the image below:

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1580978572\/23155\/uva7wf2snbti9ed6m8bn.jpg",
        "mode": "600",
        "width": 821,
        "height": 402,
        "caption": "**Figure 7**: LoRa\u00ae Network Server Device Downlink tool"
    }
}]$

**2**.Once you schedule a message for downlink it will be displayed in the Live Device Data window. Upon sending the next uplink via the RAK Serial Port Tool you will also see it there, as it needs an uplink frame in order to send the downlink in the RX1 window shown in the image below.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1580978597\/23155\/ujzm6fzfpqkpgimxw1cz.jpg",
        "mode": "600",
        "width": 855,
        "height": 417,
        "caption": "**Figure 8**: Received Downlink Frame"
    }
}]$

**3**.If you want to test the Gateway downlink via the external MQTT Broker, you need to first create a json file which you will be sensing your data in. Below is what the file formatting structure needs to look like:

$plugin[{
    "type": "callout",
    "data": {
        "text": "\"**confirmed**\": **true** \u2013 This is the LoRa\u00ae frame type. True (confirmed), False (unconfirmed)\n\n\"**data**\": \"**TEST**\" \u2013 example data to be sent\n\n\"**fPort**\": **10** \u2013 the Frame Port Number",
        "type": "info",
        "title": "Note:"
    }
}]$

$plugin[{
    "type": "code-block",
    "data": {
        "languageBlocks": [
            {
                "code": "{\n\"confirmed\": true,\n\"fPort\": 10,\n\"data\": \"1001\"\n}",
                "language": "none"
            }
        ]
    }
}]$

$plugin[{
    "type": "callout",
    "data": {
        "text": "You need to have a Base64 encoded HEX data for the above to work!",
        "type": "info",
        "title": "Note:"
    }
}]$

**4**.Create the file, for example with the following command and copy the data in discussed above:

$plugin[{
    "type": "code-block",
    "data": {
        "languageBlocks": [
            {
                "code": "sudo nano test.json",
                "language": "none"
            }
        ]
    }
}]$

**5**.After you have created the file, you need to schedule it for downlink. This means that you have to publish it via Mosquitto with the command:

$plugin[{
    "type": "code-block",
    "data": {
        "languageBlocks": [
            {
                "code": "sudo mosquito_pub application\/{{application_ID{{\/device\/{{device_EUI}}\/ tx \u2013f test.json",
                "language": "none"
            }
        ]
    }
}]$

- The packet will be scheduled for downlink, which you can see in the Gateway Packet logger.
- When the next uplink frame that comes for the Application/Device specified by the **application_ID** and **device_EUI** is received, the Gateway will send the data in the RX1 window to the node. You should have a response similar to the one in **Figure 8**.

