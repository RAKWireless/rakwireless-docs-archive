---
type: page
title: LoRa Network Server
listed: true
slug: lora-network-server
---published

The Gateway comes with an integrated LoRa Networks server. This makes the Gateway a standalone solution for the whole LoRaWAN chain in one device, which is immensely helpful for testing purposes, and provided for flexibility in deployment options.

Naturally, one can opt to disable this feature and use a LoRa Network Server hosted separately.

## 1. General

In order to use the LoRa Server you need to enable its protocol from the following menu: LoRa Gateway Menu -> LoRa Packet Forwarder -> Protocol -> Built-in LoRa Server. Now you can choose to enable/disable it via the slider in the General Configuration tab.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1564891040\/18280\/ocx0yxqvh3j8jtqfj9sv.jpg",
        "mode": "responsive",
        "width": 2110,
        "height": 998,
        "caption": "**Figure 1.** General parameters tab"
    }
}]$

Below is a short explanation of the main parameters:
H2M_LI_HEADER **Region (Frequency Plan)**:The time in _seconds_ between node status request messages sent by the Gateway. Default value of 0 (disabled status requests). A drop down menu list including the following: EU-863-870, IN868-867, US902-928, AS923, CN470-510, AU915, KR920

- **Enable ADR**: If you choose to use Adaptive Data Rate, you need to enable it via the slider and further configure the Minimum and Maximum allowed value.
- **Minimum and maximum allowed data-rate**: Note the _DR0 to DR15_ values represent a bits/s value and max payload size. Those are dependent on your region of operation and the bandwidth and SF used. However as they are predefined by the LoRa Alliance the menu does not list the full parameter values. Please refer to the official documentation for details.
- **Network ID**: The ID of the network to be advertised to end devices in case you want to have roaming to other networks
- **Downlink Tx Power**: This is the maximum power in _dBm_ the Gateway is allowed to use when transmitting frames to the nodes. It is region specific (for example EU868 is 14dBm)
- **Device-status request interval**:The time in seconds between node status request messages sent by the Gateway. Default value of 0 (disabled status requests).

## 2. Gateway

In this section you can add and External Gateways to work with your LoRa Network Server.
This way packets forwarded by the listed Gateways will be forwarded as though they were
within the range of this device.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1564891435\/18280\/g8nzfyg5zsahmbkwdp6d.jpg",
        "mode": "responsive",
        "width": 2028,
        "height": 1216,
        "caption": "**Figure 2.** Gateway tab"
    }
}]$

Below is a short explanation of the main parameters:

- **Gateway:** Here you can add a Gateway. You simply need to input the EUI into the text box and press the Add button. Additionally you can add a **Name**, **Description** and the **coordinates** of the Gateway.
- **Gateway Backend Configuration**: By filling this section, you are pointing the LoRa Network Server to the MQTT Broker
- **MQTT Broker Address:**: The IP Address where the MQTT Broker is hosted.
- **MQTT Broker Port:** The corresponding port.
- **Enable User Authentication:** If this is switched on, a Username, Password, and a Certificate (Disabled by default) will be required for user authentication. 
- **SSL/TLS Mode:** Choose the certificate type here: CA Signed server certificate, Self-signed server certificate, Self-signed server & client certificate. All certificated have support for TLSv1, TLSv1.1, and TLSv1.2.
- **MQTT Topic**: Here you can get information on the topic templates: Uplink MQTT topic, Downlink MQTT Topic, Downlink Acknowledge MQTT Topic, Gateway Statistic MQTT Topic.

## 3. Application

The first time you access the menu it will have no applications listed. Create one by Entering a name in the field and pressing the **Add **button.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1564891837\/18280\/wkhe2oqb3ajs7cx2blwo.jpg",
        "mode": "responsive",
        "width": 2120,
        "height": 640,
        "caption": "**Figure 3.** Adding an application"
    }
}]$

You will be automatically forward to the Application Edit screen. You have two tabs here, which are explained after the image:

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1564891862\/18280\/gcdhvvvn8cye6kw126lu.jpg",
        "mode": "responsive",
        "width": 2112,
        "height": 676,
        "caption": "**Figure 4.** Application configuration"
    }
}]$

**Devices:** You need to add devices to your application. You can do this one by one by entering their EUIs in the field pressing the _Add_ button. Another option is to use the Batch Add function.

**Batch add devices:** You need to fill in the following parameters: Start EUI, Step, Count, and Application Key.

The step is a decimal value that represents by how much the value of the EUI will be increased with each consecutive device. This will be done starting from the least significant bit.

The count is the maximum number of devices to be added. Note that if your step is anything different than 1 you will essentially add less devices than the Step value. Basically you will end up with a number of devices that is the Integer Division of the Count by the Step. For example if your Step is 3 and your Count is 10 you will end up with 3 Devices.

The Application Key is an AES-128 value, which is common for all devices under a given application.

Note: When Batch Adding devices they are all configured in Class A, OTAA mode, with Frame counter validation enabled.

Additionally you can Export/Import the device list in _CSV_ format.

**Application Configuration:** The user can edit the _Name_ and add a _Description_ for the application

**Adding and configuring a device:** Below is in depth explanation of the data available per device. You can enter this section by either inputting a valid EUI and pressing the _Add_ button, or pressing the _Edit_ button for an existing device:

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1564891947\/18280\/vm6n8kl6nmhkyhuegplk.jpg",
        "mode": "responsive",
        "width": 2110,
        "height": 730,
        "caption": "**Figure 5.** Adding and configuring a device"
    }
}]$

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1564891984\/18280\/ufd2ejbddrbpc2w5xmtv.jpg",
        "mode": "responsive",
        "width": 2102,
        "height": 856,
        "caption": "**Figure 6.** Device parameters"
    }
}]$

- **Configuration**: Here you can edit device parameters as follows:
- **Name**_:_does not need to match the EUI, batch loading results in a match by default
- **Class**_:_ both Class A and Class C devices are supported
- **Join Mode:**both OTAA and ABP are supported
- **Application Key:**note those can be different per device, however devices will still be grouped by application name
- **Activation:**Once you have properly configure the parameters of the device mentioned above you should see the data in the following picture (**Activation tab**):

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1564892151\/18280\/f31smejsxxir1gz1vzhe.jpg",
        "mode": "responsive",
        "width": 2094,
        "height": 800,
        "caption": "**Figure 7.** Device activation"
    }
}]$

- **Device Address**: The field is generated automatically and displays the address assigned to the node. This is how you distinguish devices in the LoRa Packet Logger.
- **Application session key**: The key assigned to the device upon OTAA Activation, or the one input manually if ABP is used.
- **Network session key**: Same as for the Application Session Key
- **Uplink frame-counter**: The number of messages that have been received by the Gateway since the device activation
- **Downlink frame-counter**: The number of messages the Gateway has sent to the node
- **Live Device Data**: You can see the packets for the selected devices in real time in this section.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1564892260\/18280\/ob3pyxmqowayzwxdbcdy.jpg",
        "mode": "responsive",
        "width": 2060,
        "height": 1210,
        "caption": "**Figure 8.** Live device data"
    }
}]$

## 4. Global Integration

This feature allows for integration of the Built-in LoRa Server with an External MQTT broker.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1564892390\/18280\/fas1pr2eid5jbwthr4zn.jpg",
        "mode": "responsive",
        "width": 1319,
        "height": 456,
        "caption": "**Figure 9.** LoRa Server Global Integration"
    }
}]$

**General Setup:** The configuration is very similar to the LoRa Gateway MQTT Bridge as can be seen below:

**MQTT Broker Address**: the IP Address of the external MQTT broker

**MQTT Broker Port**:the Port of the external MQTT broker

**Enable User Authentication**: a slider to enable/Disable Authentication

In addition to setting a _Username_ and _Password_, there is a drop down menu for the SSL/TLS Mode (Disabled by default). The following certificates are supported: _CA Signed server certificate, Self-signed server certificate, Self-signed server & client certificate_

**MQTT Topic Template Setup**:Here you can get information on the topic templates: _Join Topic, Uplink Topic, Downlink Topic, Ack Topic._

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1564892565\/18280\/gfggi05fmjsyjxac3yi7.jpg",
        "mode": "responsive",
        "width": 2130,
        "height": 844,
        "caption": "**Figure 10.** MQTT topic templates"
    }
}]$

