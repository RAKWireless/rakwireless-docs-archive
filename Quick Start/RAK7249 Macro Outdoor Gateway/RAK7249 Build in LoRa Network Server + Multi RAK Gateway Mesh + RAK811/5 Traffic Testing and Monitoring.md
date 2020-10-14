---
type: page
title: Traffic Testing and Monitoring
listed: true
slug: traffic-testing-and-monitoring
---published

### UPLINK

Now your RAK811 is authenticated with the built-in LoRa® Server. As it is connected to the external MQTT Broker via the Global Integration, you can monitor traffic in both the Live Data tab and on the Raspberry Pi 3B+ where the Mosquitto resides. Let us test this by sending an uplink frame via the RAK811.

1.In the command line window of the Raspberry Pi 3B+, we need to subscribe to the Application/Device we are going to monitor the traffic. This is done via the following command. Take note of the following syntax in the list below to have the command executed correctly:

- **application_ID**: is the application ID from the Application tab in the Gateway.
- **device_EUI**: is the Device EUI of the RAK811

$plugin[{
    "type": "code-block",
    "data": {
        "languageBlocks": [
            {
                "code": "mosquitto_sub -t application\/{{application_ID}}\/device\/{{device_EUI}}\/rx -v",
                "language": "none"
            }
        ]
    }
}]$

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1584496093\/27013\/idz7pfzz8vktxo95xzf4.jpg",
        "mode": "full",
        "width": 894,
        "height": 477,
        "caption": "**Figure 1**: Application ID"
    }
}]$

2.After executing the command, you need to send some data via the RAK Serial Port Tool. Use the command below to send an uplink frame on Frame port 1, with the Payload 1110:

$plugin[{
    "type": "code-block",
    "data": {
        "languageBlocks": [
            {
                "code": "at+send=lora:1:1110",
                "language": "none"
            }
        ]
    }
}]$

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1584496974\/27013\/h3r4bufmbj5j6bbekga8.jpg",
        "mode": "full",
        "width": 895,
        "height": 469,
        "caption": "**Figure 2**: Test Uplink (Application)"
    }
}]$

- Now if you look at the three windows in the image above, in the RAK Serial Port Tool, Live Device Data and the CLI of the Raspberry, you will see that the message arriving is displayed.

3.You can also monitor the Gateway traffic itself. You can do this via the command. Take note of the following syntax in the list below to have the command executed correctly:

- eui: is the Gateway EUI

$plugin[{
    "type": "code-block",
    "data": {
        "languageBlocks": [
            {
                "code": "mosquitto_sub -t gateway\/{{eui}}\/rx -v",
                "language": "none"
            }
        ]
    }
}]$

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1584497229\/27013\/bptwp93qandurtttzx8t.jpg",
        "mode": "full",
        "width": 829,
        "height": 442,
        "caption": "**Figure 3**: Test Uplink (Gateway)"
    }
}]$

- This is very convenient as you have three ways to monitor and you can see the metadata and payload in both the Gateway and via the MQTT Broker.

### DOWNLINK

There is a convenient tool in the Built-in LoRa® Server for sending a Downlink frame.

1.You can find it in the Device tab in the LoRa® Network Server section. You can choose your Type of frame (confirmed/unconfirmed), the Frame port and the Hex Data shown in the image below:

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1584500071\/27013\/vr9jeczyilh3htijhbc4.jpg",
        "mode": "full",
        "width": 821,
        "height": 402,
        "caption": "**Figure 4**: LoRa\u00ae Network Server Device Downlink Tool"
    }
}]$

2.Once you schedule a message for downlink, it will be displayed in the Live Device Data window. Upon sending the next uplink via the RAK Serial Port Tool you will also see it there, as it needs an uplink frame in order to send the downlink in the RX1 window shown in the image below.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1584500119\/27013\/iikvibpvxpg8cbsmekzr.jpg",
        "mode": "full",
        "width": 855,
        "height": 417,
        "caption": "**Figure 5**: Received Downlink Frame"
    }
}]$

3.If you want to test the Gateway downlink via the external MQTT Broker, you need to first create a json file which you will be sensing your data in. Below is what the file formatting structure needs to look like:

- "confirmed": true : This is the LoRa® frame type. true (confirmed), false (unconfirmed)
- "data": "TEST" : example data to be sent
- "fPort": 10 : the frame port number

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
        "text": "You need to have a Base64 encoded HEX data for the above to work.",
        "type": "info",
        "title": "Note:"
    }
}]$

4.Create the file, for example with the following command and copy the data in discussed above:

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

5.After you have created the file, you need to schedule it for downlink. This means that you have to publish it via Mosquitto with the command:

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
- When the next uplink frame that comes for the Application/Device specified by the **application_ID** and **device_EUI** is received, the Gateway will send the data in the RX1 window to the node. You should have a response similar to the one in **Figure 5**.

