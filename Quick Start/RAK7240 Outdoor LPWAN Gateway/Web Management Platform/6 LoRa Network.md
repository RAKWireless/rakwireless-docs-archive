---
type: page
title: LoRa Network
listed: true
slug: lora-network
---published

All the LoRa® Settings reside in this section. Its subsections change depending on what “**Mode**” you choose to work-in in the “**Network Settings**” subsection. As the three modes (**Network Server**, **Basic Station**, and **Packet Forwarder**) are very different, we will go through each one in detail.

$plugin[{
    "type": "callout",
    "data": {
        "text": "The one thing that is the same for all of the modes is the \u201c**LoRaWAN Network Settings**\u201d area at the top of the \u201c**Network Settings**\u201d sub-section. It is in this area where the Gateway EUI and the Mode drop-down menu reside.",
        "type": "info",
        "title": "Note:"
    }
}]$

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1592478303\/30961\/qnhsr9fjvqpip6okywce.jpg",
        "mode": "responsive",
        "width": 1930,
        "height": 411,
        "caption": "Figure 1: LoRaWAN Network Settings"
    }
}]$

**As there are additional menus that appear when one uses the “Network Server” Mode, it is the one that will be discussed in the greatest detail. The other two Modes only have the “Network Settings” sub-menu and relatively less configuration options.**

## 1. Network Settings

This page changes depending on which of the 3 options for the Mode you have chosen.

### Network Server

As this Mode provides a fully functioning LoRa® Server instance, there is a complete set of features to configure.

- **Region**: It is only displayed, can’t be changed as this is done in the “Channel Plan” menu.
- **Enable ADR**: Adaptive Data Rate, turned on/off.
- **Minimum/Maximum Allowed data-rate**: Dr0 to DR7 can be selected in order to limit the ADR possible values range.
- **ADR Margin** (dB): A value to keep in dB to make sure that the data rate is not overestimated resulting in a poor performance (error rate and range). Default value is 10.
- **Network ID**: A decimal number to distinguish between networks if you are deploying multiple ones.
- **Rx 1 Delay** (sec): The delay of the first receive window in seconds.
- **Rx 1 DataRate Offset**: It determines the data rate of the downlink frames originating from the Gateway for the Rx1 window. By default, it is 0 – identical to the uplink.
- **Rx 2 Frequency** (Hz): The frequency of the second receive window in Hz.
- **Rx 2 Datarate**: The Data Rate of the frames to be sent in the second receive window.
- **Downlink Tx Power** (dBm): This is useful in case you want to opt for a larger antenna with more gain, however you want to stay within regulations. Values from -6 to 20 are permissible.
- **Disable Frame-counter Validate**: This will turn on/off Frame counter validation.
- **Device-status request interval** (sec): It show how often should the end devices be polled for their status Log Level -choose one of for, useful for troubleshooting.
- **Statistic Period**: It shows how often the statistics will be gathered. Possible values are: 1 min, 10 min, 1h, 1 day.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1592480643\/30961\/zl20akuntu0udikjhm1c.jpg",
        "mode": "responsive",
        "width": 1914,
        "height": 1662,
        "caption": "**Figure 2**: Network Settings - Network Server"
    }
}]$

### Basic Station

This Mode allows one to utilize the Basic Station, which is Semtech’s latest packet-forwarder iteration. For more information on how Basic Station operates please refer to the [Basic Station official website](https://doc.sm.tc/station/).

There are 3 sub-sections listed below. Each of the above needs an URI and Port, together with the corresponding token/key/certificate of TLS authentication is used.

- Cups Boot Server
- XUPS Server
- LNS Server

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1592488680\/30961\/dql084lcqp4ts2uo0pgt.jpg",
        "mode": "responsive",
        "width": 1916,
        "height": 1526,
        "caption": "**Figure 3**: Network Settings \u2013 Basic Station"
    }
}]$

### Packet Forwarder

This Mode utilizes the **Semtech Legacy Packet-forwarder**. An important thing to mention is the fact that this mode has two protocol options that change the core functionality. One can choose via the Protocol drop-down menu to use the Gateway either as a pure **Semtech Packet forwarder** or as an **MQTT bridge**.

**1. General Setup - Semtech UDP GWMP Protocol**

This is something that every Gateway supports, that has been there from the very beginning of the LPWAN days. Just a general means of forwarding your LoRa® frame data over UDP to a LoRa® Server instance. The most popular/well-known setup of this is to use it together with TTN (The Things Network), which was more or less what made LoRa® popular back in 2016. This can naturally be pointed toward any LoRa® Server, not necessarily TTN.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1592489271\/30961\/xizjzxbmml2ymn52h8oo.jpg",
        "mode": "responsive",
        "width": 1209,
        "height": 919,
        "caption": "**Figure 4**: Network Settings \u2013 Semtech UDP GWMP Protocol"
    }
}]$

Things to note are the following (use Figure 4 as reference for example
values):

- **Gateway EUI**: The value in this field is necessary for registering your gateway with any LoRa® Network Server.
- **Protocol**: As mentioned, this is either a Packet forwarder or an MQTT bridge. (The former is chosen for the purpose of going through the settings.)
- **Server Address**: The URL of the LoRa® Server. (In the example: the EU TTN address)
- **Server Port Up/Down**: The ports of the LoRa® Server that are going to be used for inbound and outbound traffic.
- **Push Timeout** (ms): Time delay for the server response after sending uplink data.
- **Statistic Interval** (s): How often statistics are pushed to the server.
- **Keepalive Interval** (s): This exists to make sure that periodically data is pushed via the Gateway to make sure the server is aware that the Gateway is online (for example the MQTT bridge will unsubscribe from the topics after certain period of inactivity).
- **Automatic Data Recovery**: This is an important feature that allows LoRa® frames to be stored on the SD card (provided there is one in the slot), if there is no connection to the LoRa® Network Server. Upon restoring connectivity, these buffed messages will be forwarded, so no data will be lost. This is done in blocks of 8 (FIFO), until all are cleared from the buffer.
- **Auto-restart Threshold**: A number that defines how many times the Keepalive Interval can expire before the Packet forwarder restarts.
- **Is LoRaWAN Network**: If you choose “NO” here you will enable frames that are not compliant with the LoRaWAN® specification to be forwarded (in case you have your proprietary LoRa® Server solution). By default, “YES” is selected and non LoRaWAN® packets are dropped.
- **Log Level**: You can choose from 5 different log levels (Error/Warning/Notice/Info/Debug). This will affect System Log. From Errors only to full system log for debugging.

**2. General Setup - LoRa Gateway MQTT Bridge**

The Gateway is capable of working with an external LoRa® Server, where the MQTT Broker is pointed toward an external Server or the Built-in Server. For this purpose, there are several tabs with their corresponding parameters to be filled.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1592533408\/30961\/pnb9cplls4ebtr0ziwyx.jpg",
        "mode": "responsive",
        "width": 1567,
        "height": 1805,
        "caption": "**Figure 5**: LoRa MQTT Bridge - General Setup"
    }
}]$

**General Setup**: The is where you configure the behavior of the MQTT Bridge.

- **LoRa Network Server Type**: You have 4 options:

1. Built-in LoRa® Network Server – pointing to the Built-in Server
2. ChirpStack 2.x – for MQTT 2.x Broker (JSON) endpoints
3. ChirpStack 3.x – for MQTT 3.x Broker (PROTOBUF) endpoints
4. ChirpStack 3.x – for MQTT 3x 3.x Broker (JSON-V3) endpoint

- **MQTT Broker Address**: The IP Address of the machine where the MQTT Broker is hosted (127.0.0.1 for the Built-in one).
- **MQTT Broker Port**: The corresponding port (1883 default).
- **MQTT Protocol Version**: You can choose between V3.1 and V3.1.1.
- **Client ID**: An ID that is used to associate with the topic. If left empty, a random one will be generated.
- **Clean Session**: With this button enabled, the broker will not store any subscription information or undelivered messages.
- **Will Retain**: With this button enabled, the last message published will be retained.
- **QoS**: You can set the desired Quality of Service level
- **Keepalive**: The keep alive interval in seconds (10 default)
- **Enable Authentication**: The switch turns on Encryption of the transmitted data. You need to configure the Certificates used to encrypt the data in order for secure authentication to be performed
- **Username**: The username, if one is use, leave blank if there isn’t one
- **Password**: The password, if one is use, leave blank if there isn’t one. Can be randomly generated with the green arrows to the side of the field
- **SSL/TLS Mode**: By default, this is Disabled. You can choose one of 3 other modes: CA signed server certificate, Self-signed server certificate, Self-signed server & client certificate
- **TLS Version**: The version of the TLS protocol to be used. Options are TLSv1, TLSv1.1, TLSv1.2
- **CA Certificate, Client Certificate, Client Key, Client Key Passphrase**: You can have one or all of these to set up depending on the SSL/TLS Mode chosen. These are to be generated via the appropriate algorithm and distributed between the MQTT Broker and the LoRa® Server Please refer to the MQTT Bridge with TLS Encryption Configuration Manual for details on how to edit the settings in order for the Gateway to work as an MQTT Bridge with TLS Encryption
- **Log Level**: The granularity of the log information is chosen from the following levels: ERROR, INFO (default), DEBUG, TRACE

**MQTT Topic Template Setup**: MQTT Topic Template SetupThere are two types of templates, depending on which LoRa® Network Server Type you choose.

- ChirpStack 2.x Topic Template

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1592536507\/30961\/kpxo1gyicv1gfstxmn93.jpg",
        "mode": "responsive",
        "width": 1587,
        "height": 531,
        "caption": "**Figure 6**: LoRa\u00ae MQTT Bridge \u2013 MQTT Topic Template Setup 1"
    }
}]$

- ChirpStack 3.x Topic Template, Built-in Server

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1592536555\/30961\/kui8csxfitnpvnknee6s.jpg",
        "mode": "responsive",
        "width": 1582,
        "height": 532,
        "caption": "**Figure 7**:  LoRa\u00ae MQTT Bridge \u2013 MQTT Topic Template Setup 2"
    }
}]$

**3. Packet Filter**

By enabling this functionality, you can filter incoming traffic and only forward packets from the desired nodes in order to optimize bandwidth usage over backhaul.  You can filter by OUI or Network ID by whitelisting.

The Enable Auto Filter slider allows nodes to be automatically dropped in accordance with a set of parameters. One can set threshold values for **Discard Period (1800s), Join Period (1800s), Join Interval (6), Join Count 1 (5) and Join Count 2 (20)**.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1592538039\/30961\/tam4vp6yzwygnp8cmldw.jpg",
        "mode": "responsive",
        "width": 1913,
        "height": 1402,
        "caption": "**Figure 8**: Packet Filter"
    }
}]$

**4. GPS Information**

In case, you want to enter the GPS parameters for the Gateway manually. Flipping the Fake GPS switch turns this functionality on/off.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1592538144\/30961\/h7okkoad4jdbilcpfl53.jpg",
        "mode": "responsive",
        "width": 1913,
        "height": 932,
        "caption": "**Figure 9**: GPS Information"
    }
}]$

## 2. Network Server Status

There is a dedicated page for the status of your Built-in Network Server. You get Data in both Table and Graph form.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1592542432\/30961\/wcqhijiyghcpxpyrwjen.jpg",
        "mode": "responsive",
        "width": 1894,
        "height": 1776,
        "caption": "**Figure 10**: Network Server Status"
    }
}]$

**1. Tabular Data**

- **Uptime**: how long the Built-in Server has been working without interruption
- **Devices**: The total amount of end-devices that are currently authenticated with the server
- **Gateways**: the total amount of gateways that re forwarding frames to the server
- **Total Uplink**: total uplink frames processed
- **Total Downlink**: total downlinks frames transmitted
- **Data Downlink**: total downlink frames that carry data (non-services)
- **Total OTAA Requests**: total authentication requests submitted by end-nodes
- **Rejected OTAA Request**: total authentication requests that were rejected

**2. Graphical Data**

- **RSSI Distribution**: reflects the RSSI in increments of 20dBm starting from -120dBm and going up to -40dBm. One can get an idea of how many of the total packets received fall within a certain RSSI level and draw conclusions.
- **SNR Distribution**: reflects the SNR in increments of 5dB starting from -15dB and going up to 5dB. One can get an idea of how many of the total packets received fall within a certain SNR level and draw conclusions.
- **DataRate Distribution**: the percentage of packets that have a certain Data Rate (DR0 to DR7)
- **Traffic History**: general graphs reflecting the amount of traffic in packets versus time. Good for evaluating the time of the heaviest traffic to prevent potential fallouts.

## 3. Gateway

In this section you can add and External Gateways to work with your LoRa® Network Server. This way packet forwarded by the listed Gateways will be forwarded as though they were within the range of this device and processed by the Application Server.

$plugin[{
    "type": "callout",
    "data": {
        "text": "By default, you do not need to add the current Gateway\nas the Network Server works on it anyway, even though it is not listed.",
        "type": "info",
        "title": "Note:"
    }
}]$

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1592543568\/30961\/x0wvslf8nm0uz1a7uxeg.jpg",
        "mode": "responsive",
        "width": 1916,
        "height": 1479,
        "caption": "**Figure 11**: Gateway Settings"
    }
}]$

Below is a short explanation of the main parameters:

### Gateway

Here you can add a Gateway. You simply need to input the EUI into the text box and press the Add button. Additionally, you can add a Name, Description and the coordinates of the Gateway.

### Gateway Backend Configuration

This section allows you to configure the Gateway to use the Built-in Server to act as a MQTT Bridge.

**1. General Setup**

These setting are the same as for the LoRa® Gateway MQTT Bridge, refer to its section [LoRa Network](/quick-start/rak7249-macro-outdoor-gateway/lora-network#general-setup-lora-gateway-mqtt-bridge) for more information.

**2. MQTT Topic**

Here you can get information on the topic templates: Uplink MQTT Topic, Downlink MQTT Topic, Downlink acknowledge MQTT Topic, Gateway Statistic MQTT Topic.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1592544179\/30961\/chjagc9gajmnsumixxch.jpg",
        "mode": "responsive",
        "width": 1599,
        "height": 611,
        "caption": "**Figure 12**: Gateway Settings"
    }
}]$

## 4. Application

In order for End-node data to be processed by the Built-in LoRa® Server you need to have an Application under which you register the device. This will allow a node to join the network and you can decrypt its data payload.

The first time you access this section there will be no applications created by default. Enter a name in the field, choose one of the two type from the drop-down menu (more on this further down) and press the “**Add**” button.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1592547006\/30961\/a9vfehsxvazvh5q1yu8e.jpg",
        "mode": "responsive",
        "width": 1909,
        "height": 725,
        "caption": "**Figure 13**: NS Application"
    }
}]$

Now, you need to configure some parameters. These are separated in 3 tabs, which we will go through in order:

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1592547093\/30961\/tzli2l9tzy0vvoew2yxi.jpg",
        "mode": "responsive",
        "width": 1911,
        "height": 817,
        "caption": "**Figure 14**: NS Application Configuration"
    }
}]$

### Application Configuration

These are the mandatory things to configure, so they come first.

- **Device Authentication Mode**: This reflects the choice you made when creating the Application.

1. **Unified Application Key**: have the same key for every device that is a part of the Application
2. **Separate Application Key**: allow for devices in the same application to use different application keys

- **Name**: Chose something distinguishable
- **Auto Add LoRa Device**: If this is turned on, a field appears where you enter the Application EUI (or generate a random one). The idea here is to have your device be automatically added to the device pool if the Device EUI it has not already been added, provided the join request has the correct Application EUI and Key. This speeds up the process of adding a device to your network (from user perspective)
- **Application EUI**: You can enter one manually or generate a random one via the “green arrows” button. Make sure this one matches the one in the node
- **Application Key**: Manual or random generation options are available.
- **Description**: Not a mandatory field

### Payload Format

There are only two options here. More features to come on future updates.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1592548989\/30961\/ca3myaokjnhs6nnqitbx.jpg",
        "mode": "responsive",
        "width": 1911,
        "height": 724,
        "caption": "**Figure 15**: NS Application Payload Format"
    }
}]$

You can choose to have no encoding or to use **Cayenne LPP** (a popular low power format). This allows to directly work with services using the format, without the need to do post processing.
As this functionality separates the data field (provided you have chosen the Cayenne LPP and your node has the corresponding encoding) you should be able to have the parsed data field. You can choose to only forward the parsed data via the flip-switch. This will effectively not forward data objects that are not adhering to the Cayenne LPP format.

### Integrations

This tab allows the user to make a simple HTTPS integration to directly publish data.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1592549282\/30961\/pv7n35vbs1eckv04xo8c.jpg",
        "mode": "responsive",
        "width": 1905,
        "height": 1146,
        "caption": "**Figure 16**: NS Integrations"
    }
}]$

- There are several fields that need to be filled in, starting with the **Data Encoder/Decoder type** (Base 64 or HEX String). Once selected you can Enable the functionality with the slider.
- Afterwards make sure to fill the rest of the fields: HTTP/HTTPS Headers, Uplink data URL, Join notification URL, Ack notification URL, Device-status notification URL.
- You can test the HTTP endpoint integration with a free service like [https://webhook.site](https://webhook.site/)
- Last but not least, select a value for the Maximum number of concurrent connections and the Maximum length of the queue (default values are 16 and 64 respectively).
- The parameters and their configuration are out of the scope of this document as they are not specific to this device and there is plenty on information on the topic from various sources. Furthermore, you can check our documentation hub information and examples on the topic.
- Once your Application configuration is as you desire you can press the “**Save & Apply**” button. This will return you to the main Application section screen.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1592549819\/30961\/juvklwuejbzb8vnjxumd.jpg",
        "mode": "responsive",
        "width": 1210,
        "height": 418,
        "caption": "**Figure 17**: NS Main Application screen"
    }
}]$

- Press the “**Edit**” button to get access to the Application parameters, these includes both the parameters you entered when creating it (you can adjust these if you like) and a new tab where you can add a Device. As this is a fresh Application there are no registered devices.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1592549871\/30961\/ohxgxtnupnqew3jl9qur.jpg",
        "mode": "responsive",
        "width": 1208,
        "height": 462,
        "caption": "**Figure 18**: NS Application \u2013 Devices tab"
    }
}]$

### Devices

You need to enter a valid **Device EUI** in the text box (16 HEX symbols) and press the “**Add**” button. This will start the process and bring you to the screen where the parameters are configured. Additionally, you can Batch Add devices and Import/Export.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1592549955\/30961\/hwm0d24k64cujijhealv.jpg",
        "mode": "responsive",
        "width": 1914,
        "height": 859,
        "caption": "**Figure 19**: NS Device \u2013 Configuration tab"
    }
}]$

**1. Configuration**

The configurable parameters are in this tab, the other tabs available are only for monitoring purposes.

- **Device name**: A distinguishable name for your device.
- **Class**: LoRa® device class (both A and C are supported, B will be available in future updates).
- **Join mode**: The type of authentication method (both OTAA and ABP are supported).
- **Frame-counter Width**: The option for 16 and 32 bit exists.
- **Enable LPTP**: A proprietary protocol that allows for jumbo packets to be transferred. If such a packet arrives the Application Server will buffer it and assemble it once all the portions are available.
- **Description**: A human readable description of what the devices is to do.

**2. Activation**

This portion of the interface is empty to start with and will be popular ted with values once the devices has been authenticated and has joined the network. This applies if you use OTAA. In the case of ABP, the parameters in the Activation tab are entered manually and they will be present from the start.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1592551589\/30961\/n8r8gutonwg4dzblvf8h.jpg",
        "mode": "responsive",
        "width": 1915,
        "height": 858,
        "caption": "**Figure 20**: NS Device \u2013 Activation tab"
    }
}]$

**3. Downlink**

The user is given the option to create dummy downlink frames in order to test. Option for selecting whether the frame requires an Acknowledgment or not is present. In order to successfully transmit a downlink, you need to enter a valued Frame port and the payload bytes in HEX format.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1592552196\/30961\/itqivtk8bvserw3ueie5.jpg",
        "mode": "responsive",
        "width": 1911,
        "height": 792,
        "caption": "**Figure 21**: NS Device \u2013 Downlink tab"
    }
}]$

**4. Live Device Data**

This is perhaps the most useful tool in the Application Server interface, as it allows the user to monitor the LoRa® traffic in real time. By clicking on a given packet one can expand its windows and access detailed information containing both meta data and payload. In case the node is transmitting in LPP the payload is decrypted and decoded and one can see the information (in the case of Figure 10 there is some environmental data – temperature, barometric pressure, etc.)

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1592552406\/30961\/kbunkra7vm0xzswccvd0.jpg",
        "mode": "responsive",
        "width": 1911,
        "height": 1544,
        "caption": "**Figure 22**: NS Device \u2013 Live Device Data tab"
    }
}]$

**5. Overview**

One last thing to note is that there is an additional page to the Device data, which however only appears when the device has been authenticated and has started transmitting. It provides statistics similar to the ones on the Main interface page (RSSI, SNR, etc.), however this are not for the Gateway as a whole, but only for the particular device.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1592552518\/30961\/qkwyaoabylcnt9o4chhy.jpg",
        "mode": "responsive",
        "width": 1887,
        "height": 1866,
        "caption": "**Figure 23**: NS Device \u2013 Overview tab"
    }
}]$

## 5. Global Integration

This feature allows for integration of the Built-in LoRa® Application Server with an External MQTT broker.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1592553074\/30961\/asg3ljctdonqwpgy0asv.jpg",
        "mode": "responsive",
        "width": 1907,
        "height": 1205,
        "caption": "**Figure 24**: NS Global Integration"
    }
}]$

### General Setup

You can refer to the Gateway MQTT Bridge section for a detailed explanation of the parameters.

### MQTT Topic Template Setup

Here you can get information on the topic templates: Join Topic, Uplink Topic, Downlink Topic, Ack Topic, Status Topic.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1592553252\/30961\/qfjnd3u27oxswlt7locu.jpg",
        "mode": "responsive",
        "width": 1908,
        "height": 1047,
        "caption": "**Figure 25**: NS Global Integration MQTT Topic Template"
    }
}]$

