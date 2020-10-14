---
type: page
title: Accessing your Gateway
listed: false
slug: accessing-your-gateway
---published

This guide assumes you are using a IoT LoRa Gateway HAT (Pi Supply). After burning the image of the firmware, make sure to slot the RAK2247 Concentrator module into the IoT LoRa Gateway HAT. Next Stack the combo on top of the Raspberry Pi. Insert the SD Card and power it on.

$plugin[{
    "type": "callout",
    "data": {
        "text": "Before powering the Raspberry Pi you should install the LoRa uFL Antenna on the Concentrator.  Not doing so might damage the boards.",
        "type": "warning",
        "title": "Warning"
    }
}]$

There are two ways on how you can connect your PC with the LoRa Gateway:

### 1. Wi-Fi AP Mode

By default, the LoRa Gateway will work in Wi-Fi AP Mode, which means that you can find an SSID named like "Rakwireless_XXXX" on your PC Wi-Fi Network List.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1561110050\/16444\/nyiec9wk9b3au0vht7hx.png",
        "mode": "responsive",
        "width": 503,
        "height": 80,
        "caption": "**Figure 1:** RAKWireless Access Point"
    }
}]$

$plugin[{
    "type": "callout",
    "data": {
        "text": "Connect to this Wi-Fi SSID by using \"rakwireless\" as the default password. The default IP address of the LoRa Gateway's Wi-Fi is 192.168.12.1 . Take note of this IP address as this will be needed in connecting via SSH.",
        "type": "info",
        "title": "Note:"
    }
}]$

### 2. Via the Ethernet Port on the Raspberry Pi 3B+

You can also connect your PC with the LoRa Gateway through an Ethernet Cable via the Raspberry Pi port. By default, the IP Address of the LoRa Gateway's Ethernet is **192.168.10.10**.

## Log into the LoRa Gateway via SSH

### 1. Windows OS

SSH (Secure Shell) is typically used to log in to a remote machine and execute commands. There are a lot of free and good SSH Clients out there namely [**Putty**](https://www.chiark.greenend.org.uk/~sgtatham/putty/latest.html), [**BitVise SSH Client**](https://www.bitvise.com/ssh-client-download), **[MobaXterm](https://mobaxterm.mobatek.net/)**and many more. Feel free to choose one that fits your needs, you will be using Putty for this guide.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1561110096\/16444\/jiolozdkpt3q3y51gk4g.png",
        "mode": "responsive",
        "width": 449,
        "height": 441,
        "caption": "**Figure 2:** Putty Software for SSH in Windows"
    }
}]$

- If you have connected to the LoRa Gateway through **Wi-Fi AP Mode**, the IP Address is **192.168.12.1**
- If you have connected to the LoRa Gateway through **Ethernet**, the IP Address is **192.168.10.10**
- It will then prompt you to enter the username and password. The default username is "**pi**" and the default password is "**raspberry**".

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1561110118\/16444\/tbcdihoaguj2ukjvp0jo.png",
        "mode": "600",
        "width": 854,
        "height": 543,
        "caption": "**Figure 3:** Command line after Log in"
    }
}]$

### 2. Mac OS

Open the terminal of Mac OS. Enter `root mode` by typing the following command: "`sudo -i`".

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1561903260\/16444\/gm61vyew0n8vzmfsx0zw.png",
        "mode": "responsive",
        "width": 848,
        "height": 141,
        "caption": "**Figure 4:** SSH in Mac OS"
    }
}]$

- Enter "`ssh pi@192.168.12.1`" in the terminal to login to your LoRa Gateway, the default password is "raspberry".
- If you connect your PC with the LoRa Gateway through Ethernet Cable, you should enter "`ssh pi@192.168.10.10`", the default password is "raspberry".

### 3. Linux OS

If the OS of your PC is Linux, you should do the same as the Mac OS, except the root mode.

