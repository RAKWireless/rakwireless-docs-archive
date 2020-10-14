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
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1563422763\/-1\/bhl3jwxg1e1lqkiwukpn.jpg",
        "mode": "responsive",
        "width": 1394,
        "height": 711,
        "caption": "**Figure 1:** Activation Method - OTAA"
    }
}]$

- Take note of the **Device EUI**, **Application EUI** and the **App Key**

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1563422798\/-1\/gjygq6o6nsxjgs70qijp.jpg",
        "mode": "responsive",
        "width": 1743,
        "height": 889,
        "caption": "**Figure 2:** Device EUI, App EUI and App Key"
    }
}]$

$plugin[{
    "type": "callout",
    "data": {
        "text": "Make sure your LoRa Tracker is still Connected to the RAK Serial Port Tool.",
        "type": "info",
        "title": "Note"
    }
}]$

Now, let's join in OTAA Mode and set your device to AU915 Frequency for example. The default LoRa work mode is LoRaWAN 1.0.2, the default LoRa join mode is OTAA, and the default LoRa class is Class A. For the full list of AT Commands, head on to [auto$](/rak7200-lora-tracker/configuring-the-rak7200-lora-tracker-using-at-commands).

- `at+set_config=lora:join_mode:0` - set the join mode in OTAA.
- `at+set_config=lora:class:0 -`set the LoRa Class to Class A.
- `at+set_config=lora:region:AU915 -`this will set the frequency band to the 915Mhz for the AU region, you need to enter the corresponding frequency band for your location ( Check the corresponding frequency plan by country [here](https://www.thethingsnetwork.org/docs/lorawan/frequencies-by-country.html))

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1563424112\/17850\/qvthvz3yglsjlx79rrez.jpg",
        "mode": "300",
        "width": 541,
        "height": 662,
        "caption": "**Figure 3:** Set the Join mode in OTAA, set LoRa Class to Class A and set the frequency to 915Mhz"
    }
}]$

After , we need to set the Device EUI, Application EUI and the Application to our RAK7200. To do this, enter the following commands:

- `at+set_config=lora:dev_eui:XXX`- where XXX is your Device EUI copied from TTN.
- `at+set_config=lora:app_eui:XXX`- where XXX is your Application EUI copied from TTN.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1563424795\/17850\/lba0x94g2jwecfng49hi.jpg",
        "mode": "300",
        "width": 537,
        "height": 662,
        "caption": "**Figure 4:** Set the Dev and App EUI"
    }
}]$

- `at+set_config=lora:app_key:XXX` - where XXX is your Application Key copied from TTN.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1563424820\/17850\/xeewghj5i6pefrv96is2.jpg",
        "mode": "300",
        "width": 542,
        "height": 668,
        "caption": "**Figure 5:** Set the Application Key"
    }
}]$

This will perform OTAA (Over the air activation) and authenticate the node with TTN. It should now be registered and you can send and receive data. Finally reset the node via the Reset button. If there are no issues you should see a the following information in the Receiving window:

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1563424905\/17850\/t7qelh47t84zbiwjbnud.jpg",
        "mode": "300",
        "width": 538,
        "height": 662,
        "caption": "**Figure 6:**Successful node OTAA Join Procedure"
    }
}]$

Go to the Device Overview in the TTN and you can see that the status is now Green (Online). Now your RAK7200 is transmitting sensor data to TTN. You can see it in its raw form in TTN, by going to the Data tab:

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1564048312\/17850\/oabpufurshfpmqhyxzgu.jpg",
        "mode": "responsive",
        "width": 1809,
        "height": 747,
        "caption": "**Figure 7:** Device Application Data"
    }
}]$

