---
type: page
title: Configuring your RAK8212 iTracker Pro
listed: true
slug: configuring-your-rak8212
---published

You can configure your RAK8212 iTracker Pro by sending AT Commands through Bluetooth.

$plugin[{
    "type": "callout",
    "data": {
        "text": "For the complete list of AT Commands available for configuring your RAK8212 iTracker Pro, kindly check the [auto$](\/rak8212-itracker-pro\/at-commands-for-rak8212-itracker-pro) document.",
        "type": "info",
        "title": "Info"
    }
}]$

### Through BLE

1.In order to configure the RAK8212 iTracker Pro through BLE, download and install **nRF Connect** which is developed by Nordic Semiconductor and is also available in both App Store and Google Play Store.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1580612635\/21934\/cp0at8rhrvymleq7yuqv.jpg",
        "mode": "responsive",
        "width": 1670,
        "height": 1806,
        "caption": "**Figure 1:** nRF Connect App in Android and IOS"
    }
}]$

2.Make sure the Bluetooth on your mobile is turned on. Open the application and you will see all BLE devices in range in the scan list:

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1580440812\/21934\/nub2thufpqgy6jyuxou1.jpg",
        "mode": "300",
        "width": 1094,
        "height": 2148,
        "caption": "**Figure 2:** nRF Master Control Panel (BLE) device connecting"
    }
}]$

3.Upon connecting, a pop-up window displays and in the third item "**Nordic UART Service**", click the arrow marked in the red box which enables you to write commands through **BLE**. 

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1580442605\/21934\/piminlwoxlxa2lcyzjpx.jpg",
        "mode": "responsive",
        "width": 2188,
        "height": 2148,
        "caption": "**Figure 3**: AT+command sending throught BLE"
    }
}]$

4.Click the arrow which is marked by the red box in the picture below, you will see the following page:

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1580442688\/21934\/xfvjlkpzlwvftkgsoaku.jpg",
        "mode": "300",
        "width": 1094,
        "height": 2151,
        "caption": "**Figure 4**: Nordic UART Service RX Characteristics"
    }
}]$

5.You can now then send AT commands to the RAK8212 iTracker Pro. Meanwhile, you can also see log information in RTT Viewer as discussed in [auto$](/rak8212-itracker-pro/checking-device-logs) document.

- For example, if you want to check the current firmware’s version send the following command:

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1580612892\/21934\/pygfdyws2p5zb5zsrtva.jpg",
        "mode": "responsive",
        "width": 2202,
        "height": 2162,
        "caption": "**Figure 5**: AT+command for RAK8212 Firmware Version"
    }
}]$

6.Then, you can see the version number in RTT Viewer tool:

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1580612939\/21934\/ckpxkecc1jucumdjglfm.png",
        "mode": "responsive",
        "width": 962,
        "height": 459,
        "caption": "**Figure 6**: RAK8212 Firmware Version in RTT Viewer Tool"
    }
}]$

