---
type: page
title: Accessing your Gateway
listed: true
slug: accessing-your-gateway
---published

After burning the image into the SD Card, make sure you have inserted the SD Card with the Latest Firmware installed to the **RAK7246G LPWAN Developer Gateway** and the LoRa® and  GPS Antenna attached to it.  After which, you can now safely power on the gateway.

$plugin[{
    "type": "callout",
    "data": {
        "text": "Before powering the **RAK7246G LPWAN Developer Gateway**, you must install the LoRa\u00ae and GPS antennas. Not doing\nso might damage the boards.",
        "type": "warning",
        "title": "Warning:"
    }
}]$

### Wi-Fi AP Mode

By default, the Gateway will work in Wi-Fi AP Mode which means that you can find an SSID named like "**Rakwireless_XXXX**" on your PC Wi-Fi Network List.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1591342118\/24743\/yfgz5g5ovpfp7pzjdu3p.jpg",
        "mode": "600",
        "width": 1100,
        "height": 230,
        "caption": "**Figure 1:** RAKWireless Access Point"
    }
}]$

$plugin[{
    "type": "callout",
    "data": {
        "text": "\u201cXXXX\u201d is the last 2 bytes of your RAK7246\u2019s WiFi MAC address. Connect to this Wi-Fi SSID using the password provided below. Take note also  of the default IP address of the Gateway provided below as this will\nbe needed in connecting via SSH.\n\n**Wi-Fi Password**: rakwireless\n\n**Default IP Address**: 192.168.230.1",
        "type": "info",
        "title": "Note"
    }
}]$

## Log into the Gateway via SSH

### 1. Windows OS

SSH (Secure Shell) is typically used to log in to a remote machine and execute commands. There are a lot of free and good SSH Clients out there namely **Putty**, **BitVise SSH Client**, **MobaXterm** and many more. Feel free to choose one that fits your needs. You will be using [Putty](https://doc.rakwireless.com/rak7246---rpi-lora-gateway/downloads#putty---ssh-access-tool) for this guide.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1591343509\/24743\/ceg8e0keefnsx7whdszv.png",
        "mode": "600",
        "width": 691,
        "height": 690,
        "caption": "**Figure 2:** Putty Software for SSH in Windows"
    }
}]$

- If you have connected to the gateway through **Wi-Fi AP Mode**, the IP Address is `192.168.230.1`
- It will then prompt you to enter the username and password. The default username is "**pi**" and the default password is "**raspberry**"

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1579347514\/24743\/tfuxv3h8rzuc8pjdts1i.png",
        "mode": "responsive",
        "width": 1304,
        "height": 845,
        "caption": "**Figure 3:** Command line after log in"
    }
}]$

### 2. Mac OS

Open the Terminal of Mac OS. Launch the **Terminal** application, which is found in "/Applications/Utilities/" directory but you can also launch it from Spotlight by hitting **Command + Spacebar** and typing “Terminal” and then return:

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1576160928\/23803\/ml30pbgwlefwpd72liak.jpg",
        "mode": "600",
        "width": 989,
        "height": 633,
        "caption": "**Figure 4:** Opening Terminal in Mac OS"
    }
}]$

Open the terminal of Mac OS. Enter **root mode** by typing the following command: "`sudo -i`"

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1575957561\/23719\/nwmfjgjta9pulz2ztcns.jpg",
        "mode": "responsive",
        "width": 848,
        "height": 141,
        "caption": "**Figure 5:** SSH in Mac OS"
    }
}]$

- If you are not in root mode, enter "`ssh pi@192.168.230.1`" in the terminal to login to your gateway, the default password is "**raspberry**".

OK, you have logged into the Gateway through SSH successfully same with the image shown below:

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1576383471\/23803\/ke0ouxpmixgalqyu5cgk.jpg",
        "mode": "600",
        "width": 1136,
        "height": 712,
        "caption": "**Figure 6:** Log-in Successful Notification"
    }
}]$

### 3. Linux OS

If the OS of your PC is Linux, you should do the same as the Mac OS, except the root mode.

