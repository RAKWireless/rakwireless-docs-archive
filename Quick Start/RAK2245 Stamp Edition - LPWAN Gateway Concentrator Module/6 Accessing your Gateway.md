---
type: page
title: Accessing your Gateway
listed: true
slug: accessing-your-gateway
---published

After burning the image into the SD Card, make sure you have inserted the SD Card with the Latest Firmware installed to the Raspberry Pi  with the RAK2245 Stamp Edition - LPWAN Gateway Concentrator Module and the LoRa® and GPS Antenna attached to it. After which, you can now safely power on the gateway. In this document, several ways in accessing the gateway are provided to have different alternatives for you to choose depending on the availability of the requirements needed.

$plugin[{
    "type": "callout",
    "data": {
        "text": "Before powering the Raspberry Pi you should install the LoRa\u00ae and GPS antennas. Not doing so might damage the boards.",
        "type": "warning",
        "title": "Warning:"
    }
}]$

### 1. Wi-Fi AP Mode

By default, the gateway will work in Wi-Fi AP Mode which means that you can find a SSID named like "**Rakwireless_XXXX**" on your PC Wi-Fi Network List.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1579871940\/15987\/m3gdql9punccouuquldw.jpg",
        "mode": "300",
        "width": 517,
        "height": 94,
        "caption": "**Figure 1**: RAKWireless Access Point"
    }
}]$

$plugin[{
    "type": "callout",
    "data": {
        "text": "Connect to this Wi-Fi SSID by using \"**rakwireless**\" as the default password. The default IP address of the gateway's Wi-Fi is **`192.168.230.1`**. Take note of this IP address as this will be needed in connecting via SSH.",
        "type": "info",
        "title": "Note:"
    }
}]$

### 2. Via the Ethernet port on the Raspberry Pi 3B+

You can also connect your PC with the gateway through an Ethernet cable. By default, the IP address of the gateway’s Ethernet interface is `192.168.10.10`, so you need to set the IP address of your PC’s Ethernet to the same network segment, for example, `192.168.10.20`_._

- To do this in Windows, go to Control Panel -> Network and Internet -> Network and Sharing Center and Click **Ethernet**

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1591360427\/15987\/imoodsj5ccmum7gmu5gb.png",
        "mode": "responsive",
        "width": 1914,
        "height": 1044,
        "caption": "**Figure 2:** Network and Sharing Center"
    }
}]$

- Click **Properties** then Choose **Internet Protocol Version 4 (TCP/IPv4).**

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1591360437\/15987\/m3k48kcdd6vn6389hu3n.png",
        "mode": "responsive",
        "width": 1200,
        "height": 714,
        "caption": "**Figure 3:** Ethernet Properties"
    }
}]$

- By default, it will obtain an IP Address automatically. Click the Option "Use the following IP Address" and enter the IP Address: `192.168.10.20` and press OK.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1591360447\/15987\/c4lu3uuoogwlyhz8sdwd.png",
        "mode": "responsive",
        "width": 1240,
        "height": 694,
        "caption": "**Figure 4:** TCP\/IPv4 Properties"
    }
}]$

Now , you should be able to access your gateway from your PC successfully using the IP Address `192.168.10.10`through SSH.

## Log into the Gateway via SSH

### 1. Windows OS

SSH (Secure Shell) is typically used to log in to a remote machine and execute commands. There are a lot of free and good SSH Clients out there namely [Putty](https://www.chiark.greenend.org.uk/~sgtatham/putty/latest.html), [BitVise SSH Client](https://www.bitvise.com/ssh-client-download), [MobaXterm ](https://mobaxterm.mobatek.net/)and many more. Feel free to choose one that fits your needs, you will be using Putty for this guide.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1591360458\/15987\/iset3wuuvhwgfq1s1huv.png",
        "mode": "600",
        "width": 691,
        "height": 690,
        "caption": "**Figure 5:** Putty Software for SSH in Windows"
    }
}]$

- If you have connected to the gateway through **Wi-Fi AP Mode**, the IP Address is `192.168.230.1`
- If you have connected to the gateway through **Ethernet**, the IP Address is `192.168.1.10`
- It will then prompt you to enter the username and password. The default username is "**pi**" and the default password is "**raspberry**"

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1579872728\/15987\/xn4iy6bxo6myz6bff6is.jpg",
        "mode": "responsive",
        "width": 868,
        "height": 557,
        "caption": "**Figure 6:** Command Line after Log-in"
    }
}]$

### 2. Mac OS

Open the Terminal of Mac OS. Launch the **Terminal** application, which is found in "/Applications/Utilities/" directory but you can also launch it from Spotlight by hitting **Command + Spacebar** and typing “Terminal” and then return:

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1591360472\/15987\/iez51catkqwhoifhez7d.png",
        "mode": "600",
        "width": 1381,
        "height": 876,
        "caption": "**Figure 7:** Opening Terminal in Mac OS"
    }
}]$

Open the terminal of Mac OS. Enter **root mode** by typing the following command: "`sudo -i`"

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1579872847\/15987\/n23irdfprbarciykopvs.jpg",
        "mode": "responsive",
        "width": 862,
        "height": 155,
        "caption": "**Figure 8:** SSH in Mac OS"
    }
}]$

- If you are not in root mode, enter "`ssh pi@192.168.230.1`" in the terminal to login to your gateway, the default password is "**raspberry**".
- If you connect your PC with the gateway through Ethernet Cable, you should enter "`ssh pi@192.168.10.10`", the default password is "**raspberry**".

OK, you have logged into the gateway through SSH successfully same with the image shown below:

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1579873088\/15987\/ev6njusmdpurynnhahum.jpg",
        "mode": "responsive",
        "width": 1150,
        "height": 726,
        "caption": "**Figure 9:** Log-in Successful Notification"
    }
}]$

### 3. Linux OS

If the OS of your PC is Linux, you should do the same as the Mac OS, except for the root mode.

