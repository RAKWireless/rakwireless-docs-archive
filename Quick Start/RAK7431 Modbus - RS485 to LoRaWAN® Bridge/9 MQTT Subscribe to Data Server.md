---
type: page
title: MQTT Subscribe to Data Server
listed: true
slug: mqtt-subscribe-to-data-server
---published

To better demonstrate the functionality we will use the Application Server Integration feature to subscribe to the Built-In Network Server Topics, using the MQTT client, to obtain data and send instructions to the RAK7431.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1597151962\/45751\/y4slj6by82tyfdaexjwu.jpg",
        "mode": "responsive",
        "width": 1909,
        "height": 1059,
        "caption": "**Figure 1**: Gateway MQTT Topic Templates"
    }
}]$

To communicate with the MQTT bridge in the gateway we need to use MQTT Topic Templates.

**MQTT Topic Configuration**:

$plugin[{
    "type": "code-block",
    "data": {
        "languageBlocks": [
            {
                "code": "Application\/{{application_ID}}\/device\/{{device_EUI}}\/join Application\/{{application_ID}}\/device\/{{device_EUI}}\/rx Application\/{{application_ID}}\/device\/{{device_EUI}}\/tx Application\/{{application_ID}}\/device\/{{device_EUI}}\/ack Application\/{{application_ID}}\/device\/{{device_EUI}}\/status",
                "language": "none"
            }
        ]
    }
}]$

1.Download and install [MQTTfx tool](https://mqttfx.jensd.de/) to read the topics and send data to the gateway and node.

2.After installation, the MQTT Client must be configured. Select **local mosquitto** from the drop-down list and click the **edit connection profiles** icon marked in the image below to open the settings page.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1597206106\/45751\/qujf0ibxykcqooitytjb.jpg",
        "mode": "responsive",
        "width": 1388,
        "height": 216,
        "caption": "**Figure 2**: MQTT.fx Client"
    }
}]$

3.On the next window, input the **Broker Adress** and **Broker Port**. If the Client ID is empty press **Generate**. Then click **OK**.

- **Broken Address**: Address of MQTT server – the gateway IP. 
- **Broker Port**: Consistent with MQTT Broker Port set by the gateway - by default 1883.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1597206214\/45751\/fmwyfrsnrsoftfrcxrd4.jpg",
        "mode": "responsive",
        "width": 1073,
        "height": 1071,
        "caption": "**Figure 3**: MQTT.fx settings"
    }
}]$

4.Click on the **Connect** button. The green dot indicates that the connection is successfully subscribed to the MQTT Broker.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1597206289\/45751\/tqymt9f28jwqcwscal7c.jpg",
        "mode": "responsive",
        "width": 1387,
        "height": 167,
        "caption": "**Figure 4**: MQTT.fx connected successfully"
    }
}]$

- If we want to receive all data from the MQTT Bridge, we can use the wildcard character **#**.

5.Choose the **Subscribe tab**, enter the wildcard and press **Subscribe**.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1597206367\/45751\/monj4hnb6o8x6zjrpkvy.jpg",
        "mode": "responsive",
        "width": 1388,
        "height": 276,
        "caption": "**Figure 5**: Subscribing to MQTT Broker with wildcard"
    }
}]$

- If the node sends data, the MQTT client will display it as it is subscribed to the topic.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1597206426\/45751\/d4enpqyuodv3zjvn3dfj.jpg",
        "mode": "responsive",
        "width": 1920,
        "height": 2100,
        "caption": "**Figure 6**: Subscribed topic data"
    }
}]$

- Notice that the data field is in **base64** format, which has to be converted to hex string to be useful. We can change the data format from the built-in server settings. 

6.This is done by going to **Gateway>Application>Integrations>Data Encode/Decode Type** and chose **HEX String** form the drop-down menu. Press **Save & Apply**.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1597206495\/45751\/kyab6cnpkbuhhkzrs03e.jpg",
        "mode": "responsive",
        "width": 1918,
        "height": 1163,
        "caption": "**Figure 7**: Change the Data Encode\/Decode Type"
    }
}]$

- Now, all received data will be in HEX String. 

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1597206543\/45751\/acrwlncodqrq5nwxse7b.jpg",
        "mode": "responsive",
        "width": 1920,
        "height": 2100,
        "caption": "**Figure 8**: Received data field in HEX format"
    }
}]$

