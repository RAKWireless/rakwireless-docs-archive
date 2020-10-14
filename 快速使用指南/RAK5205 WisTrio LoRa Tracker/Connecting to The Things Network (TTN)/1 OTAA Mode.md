---
type: page
title: OTAA Mode
listed: true
slug: otaa-mode
---published

According to The Things Network, Over-the-Air Activation (OTAA) is the preferred and most secure way to connect with The Things Network. Thus it is chosen as the default method when registering a device.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1562334522\/-1\/n9lyydr7tyf6eejxvcwd.jpg",
        "mode": "responsive",
        "width": 1319,
        "height": 644,
        "caption": "**Figure 1:** Activation Method - OTAA"
    }
}]$

- Take note of the **Device EUI**, **Application EUI** and the **App Key**

$plugin[{
    "type": "callout",
    "data": {
        "text": "Make sure your LoRa Tracker is still Connected to the RAK Serial Port Tool.",
        "type": "info",
        "title": "Note"
    }
}]$

In your RAK Serial Port Tool, enter the following AT Commands in order with the corresponding values:

- `at+dev_eui=DEV_EUI`- where DEV_EUI is your Device EUI copied from TTN.
- `at+app_eui=APP_EUI` - where APP_EUI is your Application EUI copied from TTN.
- `at+app_key=APP_KEY` - where APP_KEY is your Application Key copied from TTN.

Enter the Following AT Command to set the frequency to EU868:

- `at+region=EU868` - this will set the frequency band to the 868Mhz for the EU region, you need to enter the corresponding frequency band for your location.

Now let's configure your RAK5205 to join via OTAA, by using the following AT Commands:

- at+join_mode=otaa - this will perform OTAA Activation with the 3 parameters from the previous commands in the EU868 band (Check the corresponding frequency plan by country [here](https://www.thethingsnetwork.org/docs/lorawan/frequencies-by-country.html)).

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1562335900\/17326\/val6fxcjzv9xgq9a6v9k.jpg",
        "mode": "responsive",
        "width": 1147,
        "height": 748,
        "caption": "**Figure 2**: Device EUI, Application EUI and Application Key"
    }
}]$

This will perform OTAA (Over the air activation) and authenticate the node with TTN. It should now be registered and you can send and receive data. Finally reset the node via the Reset button. If there are no issues you should see a window like the one in Figure 3

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1562336078\/17326\/n9euxavuhpqqemqlt3d5.jpg",
        "mode": "responsive",
        "width": 581,
        "height": 379,
        "caption": "**Figure 3:** Successful node OTAA Join Procedure"
    }
}]$

Now your device is online and is visible as such (Status is green, red circle) in TTN :

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1562336198\/17326\/vi9nywrppi5vaprvdzcg.jpg",
        "mode": "responsive",
        "width": 698,
        "height": 475,
        "caption": "**Figure 4:** Device Active Status"
    }
}]$

Now your RAK5205 is transmitting sensor data to TTN. You can see it in its raw form in TTN, by going to the Data tab (circled in red in the image) under your RAK5205 device as shown in Figure 5

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1562336241\/17326\/qt67vuraifjhgt0kqly3.jpg",
        "mode": "responsive",
        "width": 1362,
        "height": 602,
        "caption": "**Figure 5:** Device Data Tab"
    }
}]$

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1562336273\/17326\/ymkkixfveub3wkjwojkh.jpg",
        "mode": "responsive",
        "width": 1348,
        "height": 623,
        "caption": "**Figure 6:** Raw Device Data"
    }
}]$

This is the raw data sent by the RAK5205. In the next section, we will be analyzing the data,  we will visualize it all in a platform called Cayenne.

