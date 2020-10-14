---
type: page
title: Status Page
listed: true
slug: status-page
---published

## 1. Overview

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1561453280\/16619\/ikhkiq5kppvpvnmhac5u.jpg",
        "mode": "responsive",
        "width": 991,
        "height": 559,
        "caption": "**Figure 1.** Status Overview of the WEB Management Platform."
    }
}]$

- **Received**: Shows the total nuмber of LoRa messages received by the LoRa gateway
- **Transmitted**: Shows the LoRa message sent by the LoRa gateway
- **Active Nodes**: Shows the number of active LoRa nodes within the LoRa gateway coverage (have transmitted in the last 10min)
- **Busy Nodes**: Shows the number of busy nodes within the LoRa gateway coverage (average message spacing of less than 60s)
- **Dutycycle Of LoRa Channel**: The graph represents the "[duty cycle](https://www.thethingsnetwork.org/docs/lorawan/duty-cycle.html)" load by frequency channel (Data is kept for the last 12
hours). The minimum resolution along the time axis is 60s. Each value is an average over
60s. The values are color code – green to red, low to high.
- **LoRa Traffic**: The graph shows the packet per minute rate as a function of time. Above the image, one
can see the color-coding of the different Spreading Factors, where the actual height of the
values is a sum of all the packets over all spreading factors for the time sample.

## 2. LoRaWAN Packet Logger

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1561453435\/16619\/v8newrb1ws9qvu1vnguh.jpg",
        "mode": "responsive",
        "width": 991,
        "height": 558,
        "caption": "**Figure 2.** LoRaWAN Packet Logger View of the WEB Management Platform."
    }
}]$

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1561453480\/16619\/z0vyntqwirufxmfd3qxm.jpg",
        "mode": "responsive",
        "width": 992,
        "height": 559,
        "caption": "**Figure 3.** Detailed Information of each Message in the LoRaWAN Packet Logger"
    }
}]$

- **LoRaWAN Packet Logger**: Real-time recording and parsing of messages sent and received by the LoRaWAN Gateway, can be filtered according to message type and node address.
- **Type**: Filter by message type. Select ALL as unfiltered and display all messages.
- **DevAddr**: Filter messages based on node addresses.
- **Hide CRC_ERR packet**: When it is selected, no "[CRC](https://en.wikipedia.org/wiki/Cyclic_redundancy_check)"  check error message will be displayed.
- **Pause/Play**: Pause/start message recording.
- **Clear**: Clear the current record.
- **Download**: Save the current record locally in "[CSV](https://en.wikipedia.org/wiki/Comma-separated_values) "format.

## 3. System Log

The system log, updated in real time can be seen in this menu. It includes in addition to the host processes, the LoRa frames received/transmitted by the gateway. If the connection to the LoRa Network server is lost, it is automatically backed up on the SD card (provided one is inserted in the slot).

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1562363322\/16619\/w7w5pstfdqbbx28hssdv.jpg",
        "mode": "600",
        "width": 2054,
        "height": 1200,
        "caption": "**Figure 4.** System logger"
    }
}]$

## 4. Firewall

This section houses the Firewall settings. It also where you go to reset the Firewall

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1562363532\/16619\/hrjlkpomervhuwhymebb.jpg",
        "mode": "600",
        "width": 2079,
        "height": 1221,
        "caption": "**Figure 5.** Firewall"
    }
}]$

**NETWORK**

## 3. WAN Interface

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1561454586\/16619\/wfhib4ovjp8gp7vyaa7z.jpg",
        "mode": "responsive",
        "width": 954,
        "height": 481,
        "caption": "**Figure 6.** WAN Interface Configuration"
    }
}]$

- This is for Ethernet up-link network (WAN) configuration. It supports the [**DHCP**](https://en.wikipedia.org/wiki/Dynamic_Host_Configuration_Protocol)/[**PPPoE**](https://en.wikipedia.org/wiki/Point-to-Point_Protocol_over_Ethernet)/[**static IP**](https://www.lifewire.com/what-is-a-static-ip-address-2626012) three protocols.

## 4. Cellular Network Configuration

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1561454790\/16619\/nzfsxurrkvr4eq8xwali.jpg",
        "mode": "responsive",
        "width": 952,
        "height": 481,
        "caption": "**Figure 5.** Cellular Network Configuration"
    }
}]$

- This is for **LTE cellular** up-link network (WWAN) configuration. Please fill in **APN / User / Password** correctly, according to the information provided by the network operators.

## 5. Packet Forwarder Configuration

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1561454897\/16619\/xzczcvqdyiug8ckewouf.jpg",
        "mode": "responsive",
        "width": 975,
        "height": 494,
        "caption": "**Figure 6.** LoRa Packet Forwarder Configuration"
    }
}]$

- **General Setup** : LoRa Network Server Configuration

$plugin[{
    "type": "callout",
    "data": {
        "text": "Only the firmware after version 1.1.0036 supports the LoRa Gateway MQTT Bridge function. If you need to use this function, make sure that your firmware is up to date.",
        "type": "info",
        "title": "Note:"
    }
}]$

- **Beacon Setup** : Class B / Beacon Configuration
- **GPS Information** ：GPS Location Setup

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1561455369\/16619\/crggjhtasb1ap9xguday.jpg",
        "mode": "responsive",
        "width": 992,
        "height": 519,
        "caption": "**Figure 7.** Frequency Plan Template Import Option"
    }
}]$

- **Radio Configuration** : Rx Setup

$plugin[{
    "type": "callout",
    "data": {
        "text": "You can import the frequency plan template or you can customize the channels. For a guide on channel customization, kindly click the button below.",
        "type": "info",
        "title": "Note:"
    }
}]$

$plugin[{
    "type": "custom-html",
    "data": {
        "contents": "<a href=\"https:\/\/doc.rakwireless.com\/rak7258-micro-gateway\/web-channel-customizing\" target=\"_blank\" style=\"background-color: #0c419a; color: white; padding: 12px; border-radius: 3px;box-shadow: 2px 3px 5px 6px #ccc; text-decoration: none !important\">\n\n    RAK7258 Channel Customizing\n\n<\/a>"
    }
}]$

- **Tx Gains** ：Tx Power Setup

## 6. LoRa Gateway MQTT Bridge Configuration

test

$plugin[{
    "type": "callout",
    "data": {
        "text": "Only the firmware after 1.1.0036 version supports this function. The following figure shows the network structure of LoRa Gateway MQTT Bridge.",
        "type": "info",
        "title": "Note:"
    }
}]$

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1561457506\/16619\/swgnlbaxtldyepzpx8au.jpg",
        "mode": "responsive",
        "width": 909,
        "height": 704,
        "caption": "**Figure 8.** MQTT Bridge Configuration System Flow"
    }
}]$

### LoRa Gateway MQTT Bridge configuration steps:

- **Step 1**. Select the “LoRa Gateway MQTT Bridge” as the protocol of LoRa Packet Forwarder.
- **Step 2**. Configure the LoRa Gateway MQTT Bridge Broker IP/Port and TLS parameters.

$plugin[{
    "type": "callout",
    "data": {
        "text": "The certificates and keys can be directly filled in the contents of the PEM file, but be careful to copy the complete file content including the first and last line declaration, missing lines or missing words will cause the connection failure.",
        "type": "warning",
        "title": "Warning:"
    }
}]$

The following figure shows the general setup of LoRa Gateway MQTT Bridge.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1561457920\/16619\/ob6zzesu58jk7aqcvmro.jpg",
        "mode": "responsive",
        "width": 972,
        "height": 493,
        "caption": "**Figure 9.** LoRa Gateway MQTT Bridge Configuration"
    }
}]$

- **Step 3. (Optional Configuration)** Configure the MQTT Topic Profile, where MQTT Topic should be consistent with the gateway back-end MQTT Topic definition of LoRa Network Server.

The following figure shows the setup of MQTT Topic Profile.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1561458102\/16619\/tn2o9oagzptqaatlvwys.jpg",
        "mode": "responsive",
        "width": 974,
        "height": 270,
        "caption": "**Figure 10.** MQTT Topic Profile Setup"
    }
}]$

$plugin[{
    "type": "callout",
    "data": {
        "text": "For detailed configuration steps of MQTT Bridge, please click the button below:",
        "type": "info",
        "title": "Note:"
    }
}]$

$plugin[{
    "type": "custom-html",
    "data": {
        "contents": "<a href=\"https:\/\/doc.rakwireless.com\/rak7258-micro-gateway\/mqtt-bridge-configuration\" target=\"_blank\" style=\"background-color: #0c419a; color: white; padding: 12px; border-radius: 3px;box-shadow: 2px 3px 5px 6px #ccc; text-decoration: none !important\">\n\n    MQTT Bridge Configuration\n\n<\/a>"
    }
}]$

## 7. Network Ping Watchdog

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1561472400\/16619\/uidimyx3psprrzsphzoo.jpg",
        "mode": "responsive",
        "width": 1156,
        "height": 585,
        "caption": "**Figure 11.** Ping Watchdog Interface Overview"
    }
}]$

Ping Watchdog monitors the communication quality of network links by constantly pinging the specified IP address or domain name on the specified uplink network interface. When network link failures are found, scheduled measures are taken automatically, such as:

- .

$plugin[{
    "type": "callout",
    "data": {
        "text": "Reducing the priority of an uplink interface only works when the LoRa gateway uses both the Ethernet uplink link and the LTE cellular network uplink link.",
        "type": "info",
        "title": "Note:"
    }
}]$

**WAN** interface represents the **Ethernet uplink** interface and **WWAN** represents the **LTE cellular network uplink** interface. If Ping watchdog is opened on both uplink network interfaces simultaneously, the action is set to increase gateway Metric**.** The two uplinks would also form backup links and automatically switch to another link when one link fails. The priority of the two links is determined by the default gateway metric of their respective network interfaces. The default gateway metric can be set in **Network->WAN Network and Network- >Cellular Network**. The lower the gateway metric, the higher the priority of the link.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1561473075\/16619\/dueyv8uxs55weuar8mek.jpg",
        "mode": "responsive",
        "width": 955,
        "height": 683,
        "caption": "**Figure 12.**  Default Gateway Metric Setup"
    }
}]$

## 8. Backup or Upgrade

In **Backup/Flash Firmware** page, you can backup your configuration or restore your gateway, and you can upgrade to a new firmware. As shown in the following figure.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1561473167\/16619\/lhysuqt0nmjl7fchktpq.jpg",
        "mode": "responsive",
        "width": 990,
        "height": 558,
        "caption": "**Figure 13.**  Flash Operations Option of the RAK7258"
    }
}]$

