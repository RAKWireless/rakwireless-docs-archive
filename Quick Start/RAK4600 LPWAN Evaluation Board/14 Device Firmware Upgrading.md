---
type: page
title: Device Firmware Upgrading
listed: true
slug: device-firmware-upgrading
---published

**1.**Download the DFU package of the RAK4600 LPWAN Evaluation Board [**here**](https://downloads.rakwireless.com/en/LoRa/RAK4600/Firmware/DFU-Package/RAK4600_V3.0.0.7_dfu.zip) and save it on your mobile phone.

**2.**Make sure the Bluetooth on your mobile is turned on. Open the **nRF Connect** Mobile application and you will see all BLE devices in range in the scan list:

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1580377099\/22596\/mnzoayqdsaquxxdimpnw.jpg",
        "mode": "300",
        "width": 1093,
        "height": 2150,
        "caption": "**Figure 1**: Available Bluetooth Devices in the Nordic App"
    }
}]$

**3.**Press the reset button on the RAK4600 LPWAN Evaluation Board and wait for a couple of seconds. Look for a BLE Device named "RUI-..." in the scan list of the app. Connect to this device and click "**Nordic UART Service**" 

$plugin[{
    "type": "callout",
    "data": {
        "text": "This will be only visible for 60 seconds. More information about Bluetooth Connection Guide can be found here in [auto$](\/rak4600-lora-evaluation-board\/bluetooth-connection-modes).",
        "type": "info",
        "title": "Note"
    }
}]$

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1580377952\/22596\/wwbnonxp1ugf6jtckbm6.jpg",
        "mode": "responsive",
        "width": 2188,
        "height": 2148,
        "caption": "**Figure 2**: Secure DFU Service in the Nordic App"
    }
}]$

**4.**Choose “**Secure DFU Service**” and click the button highlighted in red.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1580378131\/22596\/qxw4hh00xqmcv85df1f7.jpg",
        "mode": "responsive",
        "width": 2188,
        "height": 2148,
        "caption": "**Figure 3**: Buttonless DFU"
    }
}]$

**5.**Now, click the **red box button** in the image shown below and press "**Send**" in the **Write Value** pop-up window.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1580378373\/22596\/xb1hntew7qrbct9et5hz.jpg",
        "mode": "responsive",
        "width": 2188,
        "height": 2148,
        "caption": "**Figure 4:** Resetting the Bootloader via Bluetooth"
    }
}]$

**6.**Great! Now the RAK4600 is now working in DFU Mode. In the application, you will see the following: 

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1580378487\/22596\/qmi89z3vqxvukvbiodnc.jpg",
        "mode": "300",
        "width": 1094,
        "height": 2151,
        "caption": "**Figure 5**: RAK4600 Default Status Overview after Resetting"
    }
}]$

**7.**In the list of devices, find a BLE signal named "**DfuTarg**" and Connect. 

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1580378616\/22596\/g2v0fkj63cbuwtt24mht.jpg",
        "mode": "300",
        "width": 1080,
        "height": 2137,
        "caption": "**Figure 6**: RAK4600 Default Bluetooth ID after Resetting"
    }
}]$

**8.**After connecting, select the DFU Icon. Select the **Distribution packet (ZIP)** and press OK. This will then prompt you to select the zip file of the firmware that you have downloaded. 

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1580378775\/22596\/pqnewr61x87nv5nrxovs.jpg",
        "mode": "responsive",
        "width": 2188,
        "height": 2148,
        "caption": "**Figure 7**: Distribution Packet File Type under DFU"
    }
}]$

**9.** It will then automatically start to upgrade the firmware of your RAK4600 through DFU over BLE. After upgrading, it will restart and the DFU Connection will be disconnected. Now you can use your RAK4600 with the latest firmware!

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1580378838\/22596\/nzilnqodbz6x33uvnpp4.jpg",
        "mode": "300",
        "width": 1094,
        "height": 2147,
        "caption": "**Figure 8**: DFU Upgrading of RAK4600 Firmwave via BLE"
    }
}]$

