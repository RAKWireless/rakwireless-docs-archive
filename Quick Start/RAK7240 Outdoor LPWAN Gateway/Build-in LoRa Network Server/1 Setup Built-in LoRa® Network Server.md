---
type: page
title: Setup Built-in LoRa® Network Server
listed: true
slug: setup-built-in-lora-ns
---published

This section is the detailed discussion on how to set-up the built-in LoRa® Server for your RAK7240 Outdoor LPWAN Gateway using the Web Management Platform. Before going through the steps, access the Web Management Platform as discussed in the prior section .

### Packet Forwarder Set-up

$plugin[{
    "type": "callout",
    "data": {
        "text": "For other settings and detailed documentation for this section, kindly browse the [LoRaWAN\u00ae Gateway Configuration](\/quick-start\/rak7240-outdoor-lpwan-gateway\/lorawan-gateway-configuration#2-general)",
        "type": "info",
        "title": "Note:"
    }
}]$

1.By navigating through LoRa® Gateway tab-> LoRa® Packet Forwarder-> General Setup, set the Protocol in the drop-down list to **Build-in LoRa ® Server**.

2.You can leave the rest of the settings with their default values. Remember to "**Save & Apply**".

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1584344992\/26978\/qpjev8rq0v3ufwhhfjgz.png",
        "mode": "responsive",
        "width": 1934,
        "height": 858,
        "caption": "**Figure 1**: Build-in LoRa Server Protocol in Gateway"
    }
}]$

### Configure the LoRa® Server

$plugin[{
    "type": "callout",
    "data": {
        "text": "For other settings and detailed documentation for this section, kindly browse the [auto$](\/rak7240-outdoor-lpwan-gateway\/lora-network-server) section.",
        "type": "info",
        "title": "Note:"
    }
}]$

1.Navigate through LoRa® Network Server tab -> General and turn-on this feature using the Enable slider.

2.Select your Region (Frequency Band). For this demonstration, we are going to use EU863-870 frequency band.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1584346870\/26978\/llifq4lis4tcb2yaz5me.png",
        "mode": "responsive",
        "width": 1914,
        "height": 878,
        "caption": "**Figure 2**: LoRa\u00ae Network Server General"
    }
}]$

### Register RAK7240 Gateway

1.Navigate through LoRa® Network Server-> Gateway and enter the **Gateway EUI** in the field.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1584424409\/26978\/rmhju6hnvebpzmgvnzon.png",
        "mode": "responsive",
        "width": 1912,
        "height": 877,
        "caption": "**Figure 3**: Adding Gateway EUI"
    }
}]$

2.By pressing the "**Add**" button, you will be redirected into a new tab where you will need to fill the mandatory parameters: **Name** and **Description**.

$plugin[{
    "type": "callout",
    "data": {
        "text": "The **Latitude**, **Longitude** and **Altitude** parameters are not mandatory. You can leave them for later, or leave them empty if the gateway is not stationary.",
        "type": "info",
        "title": "Note:"
    }
}]$

3.If everything is set-up correctly, you should see the same set-up with the image shown below:

$plugin[{
    "type": "callout",
    "data": {
        "text": "In order to see the Last Seen status update you need to refresh the page. There should be a value of a couple of seconds, if so than everything went well. In case there is a message \u201c**Never Seen**\u201d, there is an issue and you best redo the configuration.",
        "type": "info",
        "title": "Note:"
    }
}]$

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1584424486\/26978\/ywkvdae1pmqfkvo8lhul.jpg",
        "mode": "responsive",
        "width": 1268,
        "height": 633,
        "caption": "**Figure 4**: Gateway Successful Adding"
    }
}]$

