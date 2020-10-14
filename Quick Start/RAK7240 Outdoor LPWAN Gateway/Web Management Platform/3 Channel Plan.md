---
type: page
title: Channel Plan
listed: true
slug: channel-plan
---published


This is a very important section of the Web UI. Here you set the frequency of operation of the Gateway. It is these frequency channels that it will be monitoring and both receiving from and transmitting to LoRa® nodes.

- For your convenience there is a drop-down list at the top of the page where you can choose one of several pre-set Regions. This will populate the Multi-SF LoRa® Channels with the mandatory channels (in accordance with the LoRa Alliance Regional Parameters).
- In case you want to use a custom set, you can enter a channel’s frequency (in MHz) in the text box and add it via the blue button. This applies for the Standard LoRa® Channel and FSK Channel as well (normally you would have one per Concentrator.
- You can also “**Switch to Advanced Mode**”, where you have more granular control per concentrator and per radio. (up to 2 concentrators and 2 radios per concentrator for up to 4 total radios).


$plugin[{
    "type": "callout",
    "data": {
        "text": "If you have 2 Concentrator modules as the Outdoor\nGateways allow the maximum number of channels will be double (16). These are\nall grouped together if you configure in Standard Mode and split in 8 per\nconcentrator in Advanced Mode.",
        "type": "info",
        "title": "Note:"
    }
}]$



$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1592477653\/30959\/wlsiirjma31zcpeosxcr.jpg",
        "mode": "responsive",
        "width": 1922,
        "height": 1034,
        "caption": "**Figure 1**: Channel Plan \u2013 Standard Mode"
    }
}]$



$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1592477709\/30959\/eplxxmulgegfjscgjme6.jpg",
        "mode": "responsive",
        "width": 1927,
        "height": 1483,
        "caption": "**Figure 2**: Channel Plan \u2013 Advanced Mode"
    }
}]$




