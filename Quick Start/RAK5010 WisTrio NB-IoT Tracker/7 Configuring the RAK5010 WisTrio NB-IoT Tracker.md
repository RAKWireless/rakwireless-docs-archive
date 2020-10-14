---
type: page
title: Configuring the RAK5010 WisTrio NB-IoT Tracker
listed: true
slug: configuring-the-device
---published

You can configure your RAK5010 WisTrio NB-IoT Tracker by sending AT Commands either through UART, through BLE or through Micro USB.

$plugin[{
    "type": "callout",
    "data": {
        "text": "For the full list of AT Commands available for configuring your RAK5010, kindly check [auto$](\/rak5010-wistrio-nb-iot-tracker\/at-commands-for-rak5010).",
        "type": "info",
        "title": "Note"
    }
}]$

### Through UART

**1.**As mentioned in [auto$](/rak5010-wistrio-nb-iot-tracker/checking-device-logs), if you want to use RAK5010 WisTrio NB-IoT Tracker through UART, you should connect the RAK5010 in your machine through UART as shown in the image below:

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1580438878\/20385\/g1rz6rigcuznvqtlfcb5.jpg",
        "mode": "responsive",
        "width": 6264,
        "height": 2151,
        "caption": null
    }
}]$

**2.**Try to send a simple AT command to RAK5010 to get the current firmware’s version by sending the command below using the RAK Serial Port Tool. Similarly, you can send other AT commands of RAK5010 in the same way.

$plugin[{
    "type": "code-block",
    "data": {
        "languageBlocks": [
            {
                "code": "at+version",
                "language": "none"
            }
        ]
    }
}]$

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1569641409\/20385\/viskdhazv9uu3yxhotid.jpg",
        "mode": "300",
        "width": 538,
        "height": 654,
        "caption": "**Figure 1**: AT command for Firmware Version"
    }
}]$

### Through BLE

**1.** In order to configure the RAK5010 WisTrio NB-IoT Tracker through BLE, download and install **nRF Connect** which is developed by Nordic Semiconductor and is also available in both App Store and Google Play Store.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1580375425\/20385\/eponlb3piu1p6noof1np.png",
        "mode": "responsive",
        "width": 1670,
        "height": 1806,
        "caption": "**Figure 2:** nRF Connect App in Android and IOS"
    }
}]$

**2.** Make sure the Bluetooth on your mobile is turned on. Open the application and you will see all BLE devices in range in the scan list:

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1580375724\/20385\/rwpeihuyflhu65gopfml.jpg",
        "mode": "300",
        "width": 1093,
        "height": 2150,
        "caption": "**Figure 3**: Available Bluetooth Devices in the Nordic App"
    }
}]$

**3.** Press the reset button on the RAK5010 and wait for a couple of seconds. Look for a BLE Device named "RUI-..." in the scan list of the app. Connect to this device and click "**Nordic UART Service**"

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1580375890\/20385\/mg6xtfoepu06s33iedyu.jpg",
        "mode": "responsive",
        "width": 2188,
        "height": 2148,
        "caption": "**Figure 4:** Nordic UART Service in the Nordic App"
    }
}]$

$plugin[{
    "type": "callout",
    "data": {
        "text": "By the default, the BLE signal of the RAK5010 is turned off automatically if no connection is established after 60 seconds. Connect to the BLE signal of the RAK5010 immediately after pressing the reset button.",
        "type": "warning",
        "title": "Warning"
    }
}]$

**4.** Click the arrow which is marked by the red box in the picture below, you will see the following page:

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1580376078\/20385\/r7j95cqwrevod7qtvcsv.jpg",
        "mode": "300",
        "width": 1094,
        "height": 2151,
        "caption": "**Figure 5:** RX Characteristic in the Nordic UART Service"
    }
}]$

**5.** You can now then send AT commands to the RAK5010. Meanwhile you can also see log information in RTT Viewer as discussed in [auto$](/rak5010-wistrio-nb-iot-tracker/checking-device-logs).

- For example, if you want to check the current firmware’s version send the following command:

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1580376318\/20385\/jficmu58afzs3r1hkw5h.jpg",
        "mode": "responsive",
        "width": 2188,
        "height": 2148,
        "caption": "**Figure 6**: Sending AT Command via Nordic App"
    }
}]$

**6.** Then, you can see the version number in RTT Viewer tool:

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1580438455\/20385\/nqqegmebbppnrcguzshh.png",
        "mode": "responsive",
        "width": 1159,
        "height": 670,
        "caption": "**Figure 7**: Log Info in J-Link RTT Viewer"
    }
}]$

### Through Micro USB

- To begin with, connect your RAK5010 with your PC through microUSB/USB as shown in the image below:

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1580439043\/20385\/ehzpnpgveqdplcndqwc7.jpg",
        "mode": "responsive",
        "width": 3544,
        "height": 2020,
        "caption": "**Figure 8**: MicroUSB Interface for RAK5010"
    }
}]$

- Open the serial port tool in your PC.

$plugin[{
    "type": "callout",
    "data": {
        "text": "For this method, you need a serial port tool which can support DTR function, like Termite. You can download\nTermite [**here**](https:\/\/downloads.rakwireless.com\/en\/Cellular\/Tools\/).",
        "type": "info",
        "title": "Note:"
    }
}]$

Alright, after opening the serial tool, configure its setting by following the picture below:

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1580439060\/20385\/ginpaktnnszkf65cnlgo.png",
        "mode": "responsive",
        "width": 1035,
        "height": 717,
        "caption": "**Figure 9**: Termite Configuration Enabling DTR"
    }
}]$

Termite will connect with RAK5010 automatically, if not, just click the blue button to connect again:

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1572798488\/20385\/fjdgvai3o7c0fkworis5.jpg",
        "mode": "responsive",
        "width": 1005,
        "height": 721,
        "caption": "**Figure 10**: Termite Initial Log"
    }
}]$

- Now, you can send AT commands into RAK5010.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1580439072\/20385\/ytdlpxiq25p7o1o3ylkr.png",
        "mode": "responsive",
        "width": 1268,
        "height": 390,
        "caption": "**Figure 11**: Checked Log in Termite"
    }
}]$

