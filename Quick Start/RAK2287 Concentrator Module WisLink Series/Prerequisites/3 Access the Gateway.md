---
type: page
title: Access the Gateway
listed: true
slug: access-the-gateway
---published

There are two ways to connect to your RAK2287 Concentrator Module WisLink Series setup:

$plugin[{
    "type": "callout",
    "data": {
        "text": "Before powering the Raspberry Pi 3B+ or 4 you should install the LoRa\u00ae and GPS antennas. Not doing\nso might damage the boards.",
        "type": "warning",
        "title": "Warning:"
    }
}]$

### 1. Wi-Fi AP Mode

By default, the Firmware is configured to operate the Raspberry Pi in Wi-Fi AP mode, which means that you should be able to find an SSID named “**Rakwireless_XXXX**” on the Wi-Fi network list, for example:

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1591359339\/16422\/r73mdtnaazssxuhawnbu.jpg",
        "mode": "responsive",
        "width": 1100,
        "height": 230,
        "caption": "**Figure 1:** RAKWireless Access Point"
    }
}]$

$plugin[{
    "type": "callout",
    "data": {
        "text": "Connect to this Wi-Fi SSID by using \"**rakwireless**\" as the default password. The default IP\naddress of the gateway's Wi-Fi is `192.168.230.1` . Take note of this IP address as this will\nbe needed in connecting via SSH.",
        "type": "info",
        "title": "Note"
    }
}]$

There is no need to configure the IP address of your PC as it will be assigned automatically via the DHCP server.

### 2. Via the Ethernet Port on the Raspberry Pi

You can also connect your PC with the  gateway through an Ethernet cable. By default, the IP address of the gateway’s Ethernet interface is `192.168.10.10`, so you need to set the IP address of your PC’s Ethernet to the same network segment, for example, `192.168.10.20`_._

- To do this in Windows, go to Control Panel -> Network and Internet -> Network and Sharing Center and Click **Ethernet**

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1591359377\/16422\/shhuzuexng6hzvnojffx.png",
        "mode": "600",
        "width": 1914,
        "height": 1044,
        "caption": "**Figure 2:** Network and Sharing Center"
    }
}]$

- Click **Properties** then Choose **Internet Protocol Version 4 (TCP/IPv4).**

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1591359402\/16422\/ojc4wt2miahdwhwgr2sw.png",
        "mode": "responsive",
        "width": 1200,
        "height": 714,
        "caption": "**Figure 3:** Ethernet Properties"
    }
}]$

- By default, it will obtain an IP Address automatically. Click the Option "Use the following IP Address" and enter the  IP Address: `192.168.10.20` and press OK.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1591359426\/16422\/vapj6ve4oxzemfi3gbgx.png",
        "mode": "responsive",
        "width": 1240,
        "height": 694,
        "caption": "**Figure 4:** TCP\/IPv4 Properties"
    }
}]$

Now , you should be able to access your gateway from your PC successfully using the IP Address `192.168.10.10`through SSH.

## Log into the Gateway via SSH

### 1. Windows OS

SSH (Secure Shell) is typically used to log in to a remote machine and execute commands. There are a lot of free and good SSH Clients out there namely [**Putty**](https://www.chiark.greenend.org.uk/~sgtatham/putty/latest.html), [**BitVise SSH Client**](https://www.bitvise.com/ssh-client-download), [**MobaXterm**](https://mobaxterm.mobatek.net/) and many more. Feel free to choose one that fits your needs, you will be using Putty for this guide.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1591359441\/16422\/rtay3ukszfnlzyguulwv.png",
        "mode": "600",
        "width": 691,
        "height": 690,
        "caption": "**Figure 5:** Putty Software for SSH in Windows"
    }
}]$

- If you have connected to the gateway through **Wi-Fi AP Mode**, the IP Address is `192.168.230.1.`
- If you have connected to the gateway through **Ethernet**, the IP Address is `192.168.10.10.`
- It will then prompt you to enter the username and password. The default username is "**pi**" and the default password is "**raspberry**".

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1576787948\/23803\/wzhirj41gxy8gnjgm0xy.png",
        "mode": "responsive",
        "width": 899,
        "height": 602,
        "caption": "**Figure 6:** Command line after log in"
    }
}]$

### 2. Mac OS

Open the Terminal of Mac OS. Launch the **Terminal** application, which is found in "/Applications/Utilities/" directory but you can also launch it from Spotlight by hitting **Command + Spacebar** and typing “Terminal” and then return:

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1591359470\/16422\/deobdkikkw2o1ws2itzv.png",
        "mode": "responsive",
        "width": 1381,
        "height": 876,
        "caption": "**Figure 7:** Opening Terminal in Mac OS"
    }
}]$

Open the terminal of Mac OS. Enter **root mode** by typing the following command: "`sudo -i`".

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1575957561\/23719\/nwmfjgjta9pulz2ztcns.jpg",
        "mode": "responsive",
        "width": 848,
        "height": 141,
        "caption": "**Figure 8:** SSH in Mac OS"
    }
}]$

- If you are not in root mode, enter "`ssh pi@192.168.230.1`" in the terminal to login to your gateway, the default password is "**raspberry**".
- If you connect your PC with the gateway through Ethernet Cable, you should enter "`ssh pi@192.168.10.10`", the default password is "**raspberry**".

OK, you have logged into the gateway through SSH successfully same with the image shown below:

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1576383471\/23803\/ke0ouxpmixgalqyu5cgk.jpg",
        "mode": "600",
        "width": 1136,
        "height": 712,
        "caption": "**Figure 9:** Log-in Successful Notification"
    }
}]$

### 3. Linux OS

If the OS of your PC is Linux, you should do the same as the Mac OS, except the root mode.

