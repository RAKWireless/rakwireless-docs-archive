---
type: page
title: Configuring the RAK4600 LPWAN Evaluation Board
listed: true
slug: configuring-the-rak4600-lora-evaluation-board
---published

You can configure your RAK4600 LPWAN Evaluation board by sending AT Commands either through UART or through BLE.

$plugin[{
    "type": "callout",
    "data": {
        "text": "For the complete list of AT Commands available for configuring your RAK4600 LPWAN Evaluation Board,  kindly click [here](\/rak4600-lora-evaluation-board\/at-commands-for-rak4600)",
        "type": "info",
        "title": "Note:"
    }
}]$

### Through UART

1. As mentioned in Checking Device Logs , if you want to use RAK4600 LPWAN Evaluation Board through UART, you should connect the RAK4600 in your machine through UART as shown in the image below:

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1580142010\/22598\/evtfrnai2bs2mtpyhusv.jpg",
        "mode": "responsive",
        "width": 1600,
        "height": 600,
        "caption": "**Figure 1**: UART to RAK4600 LoRa\u00ae  Evaluation Board Connection"
    }
}]$

**2.** Try to send a simple AT command to RAK4600 to get the current firmware’s version by sending the command below using the RAK Serial Port Tool. Similarly, you can send other AT commands of RAK4600 in the same way.

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
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1580196484\/22598\/nf6t8ozsqpkucbbr58tf.jpg",
        "mode": "responsive",
        "width": 550,
        "height": 671,
        "caption": "**Figure 2**: RAK4600 Version Checking via RAK Serial Port Tool"
    }
}]$

### Through BLE

1. In order to configure the RAK4600 LPWAN Evaluation Board through BLE, download and install nRF Connect which is developed by Nordic Semiconductor and is also available in both App Store and Google Play Store.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1580194231\/22598\/hduslzxiwfe6kwsj0ksn.png",
        "mode": "600",
        "width": 1670,
        "height": 1806,
        "caption": "**Figure 3:** nRF Connect App in Android and IOS"
    }
}]$

**2.** Make sure the Bluetooth on your mobile is turned on. Open the application and you will see all BLE devices in range in the scan list:

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1580376685\/22598\/p2phiyi0prjpmtdvjwsl.jpg",
        "mode": "300",
        "width": 1094,
        "height": 2148,
        "caption": "**Figure 3**: Available Bluetooth Devices in the Nordic App"
    }
}]$

**3.** Press the reset button on the RAK4600 LPWAN Evaluation Board and wait for a couple of seconds. Look for a BLE Device named "RUI-..." in the scan list of the app. Connect to this device and click "**Nordic UART Service**"

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1580376699\/22598\/um8erg9zw1xozuel61ar.jpg",
        "mode": "responsive",
        "width": 2188,
        "height": 2148,
        "caption": "**Figure 4**: Nordic UART Service in the Nordic App"
    }
}]$

$plugin[{
    "type": "callout",
    "data": {
        "text": "By the default, the BLE signal of the RAK4600 is turned off automatically if no connection is established after 60 seconds. Connect to the BLE signal of the RAK4600 immediately after pressing the reset button.",
        "type": "warning",
        "title": "Warning"
    }
}]$

**4.** Click the arrow which is marked by the red box in the picture below, you will see the following page:

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1580376775\/22598\/xxlsye1tunqfzihlagbt.jpg",
        "mode": "300",
        "width": 1094,
        "height": 2151,
        "caption": "**Figure 5**: RX Characteristic in the Nordic UART Service"
    }
}]$

**5.** You can now then send AT commands to the RAK4600. Meanwhile you can also see log information in RTT Viewer as discussed in [auto$](/rak4600-lora-evaluation-board/checking-device-logs#through-j-link-rtt-viewer).

- For example, if you want to check the current firmware’s version send the following command:

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1580376791\/22598\/n5h2naehgbbzjnlt8l6y.jpg",
        "mode": "responsive",
        "width": 2188,
        "height": 2148,
        "caption": "**Figure 6**: Sending AT Command via Nordic App"
    }
}]$

**6.** Then you can see the version number in RTT Viewer tool:

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1580196818\/22598\/c9x3b3vnnmwsnfaobycq.jpg",
        "mode": "responsive",
        "width": 895,
        "height": 458,
        "caption": "**Figure 7**: Logs displayed in the J-Link RTT Viewer"
    }
}]$

