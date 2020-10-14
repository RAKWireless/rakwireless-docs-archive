---
type: page
title: Configuring your Gateway
listed: true
slug: configuring-your-gateway
---published

### Packet Forwarder Set-up

1.In the Web Management Platform, navigate through **LoRa® Network-> Network Settings-> Packet Forwarder Settings-> General Setup**, and set the Protocol in the drop-down list to **Semtech UDP GWMP Protocol**. You need only change
the Server Address in order to forward the traffic to your ChirpStack running
on the Ubuntu Instance (AWS). Enter your Instance Public IP Address in the
field marked with the red rectangle in the image below:

$plugin[{
    "type": "callout",
    "data": {
        "text": "Read the [LoRa Network](\/quick-start\/rak7258-micro-gateway\/lora-network#1-network-settings) section in the Web Management Platform to know more about the other modes aside from the Packet Forwarder Setup.",
        "type": "info",
        "title": "Note:"
    }
}]$

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1592935582\/27018\/sldjary92luuwyxje1ch.png",
        "mode": "responsive",
        "width": 1932,
        "height": 1094,
        "caption": "**Figure 1**: ChirpStack Packet\nForwarder Configuration"
    }
}]$

1. Click "**Save and Apply**" and go to your ChirpStack Web UI running on the AWS Instance (IP Address:8080). Go to the Gateway tab. Press the “**Create**” button.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1592935726\/27018\/xfhlmxxfa6myf32llvxj.png",
        "mode": "responsive",
        "width": 1932,
        "height": 1094,
        "caption": "**Figure 2**: ChirpStack Gateways\nCreation"
    }
}]$

3.In the next window, input the **Gateway Name**, **EUI and Description**. Select a network server and Service Profile from the drop-down menu (remember those are pre-configured with the RAKwireless image). Finally click the “**Create Gateway**” button.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1592935666\/27018\/p3kyxeac50t43dzhfhue.png",
        "mode": "responsive",
        "width": 1931,
        "height": 1094,
        "caption": "**Figure 3**: ChirpStack Gateway\nParameters"
    }
}]$

4.Assuming you entered the parameters correctly, you should see your Gateway status as seen is a few second in the Gateway Details tab. You can also monitor Live LoRa® Frames in the tab with the same name to see incoming traffic.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1592935769\/27018\/s8pa98gfedjuounjul1t.png",
        "mode": "responsive",
        "width": 1932,
        "height": 1094,
        "caption": "**Figure 4**: ChirpStack Gateway\nDetails"
    }
}]$

### MQTT Bridge Set-up

If you want to use the MQTT Bridge to forward your LoRa® Traffic to your LoRa® Network Server you need to configure your Gateway use the Bridge instead of the Packet Forwarder.

1.Navigating through **LoRa® Network-> Network Settings-> Packet Forwarder Settings-> General Setup**, set the Protocol in the drop-down list to **LoRa® Gateway MQTT Bridge**. Afterwhich, click "**Save and Apply**".

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1592935810\/27018\/fluo2qe3leupwuioy33u.png",
        "mode": "responsive",
        "width": 1934,
        "height": 1094,
        "caption": "**Figure 5**: Gateway MQTT Bridge\nProtocol"
    }
}]$

2.Next, choose the type of LoRa Network Server you are going to be using.”

3.Set the address to the address of the AWS Instance and the port to 1883, Save and Apply.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1592937083\/27018\/jzshctxw7i4soaq7fqur.png",
        "mode": "responsive",
        "width": 1934,
        "height": 1094,
        "caption": "**Figure 6**: Gateway MQTT Bridge\nParameters"
    }
}]$

4.Lastly, register your Gateway to Chirpstack if you have not done so. You can follow the steps undergone in the Packet Forwarder Set-up section of the [Configuring your Gateway](/quick-start/rak7258-micro-gateway/configuring-your-gateway#packet-forwarder-set-up) document.

