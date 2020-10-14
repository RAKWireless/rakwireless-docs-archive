---
type: page
title: Accessing your Gateway
listed: true
slug: accessing-your-gateway
---published

After burning the image of the firmware, make sure to stack the RAK2245 Stamp Edition on top of your Raspberry Pi. Insert the SD Card and power it on.

$plugin[{
    "type": "callout",
    "data": {
        "text": "Before powering the Raspberry Pi you should install the LoRa and GPS antennas. Not doing so might damage the boards.",
        "type": "info",
        "title": "Note"
    }
}]$

There are two ways on how you can connect your PC with the LoRa Gateway:

1. **Wi-Fi AP Mode**

By default, the LoRa Gateway will work in Wi-Fi AP Mode which means that you can find a SSID named like "Rakwireless_XXXX" on your PC Wi-Fi Network List.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1561006497\/15987\/o191iags2a17glpoocmc.jpg",
        "mode": "responsive",
        "width": 503,
        "height": 80,
        "caption": "Figure 1: RAKWireless Access Point"
    }
}]$

Connect to this Wi-Fi SSID by using "**rakwireless**" as the default password. The default IP address of the LoRa Gateway's Wi-Fi is **192.168.12.1** . Take note of this IP address as this will be needed in connecting via SSH.

1. Via the Ethernet port on the Raspberry Pi 3B+

You can also connect your PC with the LoRa Gateway through an Ethernet Cable. By default, the IP Address of the LoRa Gateway's Ethernet is 192.168.10.10

## Log into the LoRa Gateway via SSH

### For Windows

SSH (Secure Shell) is typically used to log in to a remote machine and execute commands. There are a lot of free and good SSH Clients out there namely [Putty](https://www.chiark.greenend.org.uk/~sgtatham/putty/latest.html), [BitVise SSH Client](https://www.bitvise.com/ssh-client-download), [MobaXterm ](https://mobaxterm.mobatek.net/)and many more. Feel free to choose one that fits your needs, you will be using Putty for this guide.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1561007295\/15987\/nr7n0yd8anyhmd5zm7p5.jpg",
        "mode": "responsive",
        "width": 449,
        "height": 441,
        "caption": "Figure 2: Putty Software for SSH in Windows"
    }
}]$

- If you connect with the LoRa Gateway through **Wi-Fi AP Mode**, the IP Address is **192.168.12.1**
- If you connect with the LoRa Gateway through **Ethernet**, the IP Address is **192.168.10.10**
- It will then prompt you to enter the username and password. The default username is "**pi**" and the default password is "**raspberry**"

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1561007660\/15987\/sfzdrqva0x7wo4gnvcww.jpg",
        "mode": "600",
        "width": 854,
        "height": 543,
        "caption": "Figure 3: Command line after log in"
    }
}]$

### For Mac OS

Open the terminal of Mac OS. Enter **root mode** by typing the following command: "`sudo -i`"

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1561009780\/15987\/vzrhdrrikdy04drbkg7m.jpg",
        "mode": "full",
        "width": 848,
        "height": 141,
        "caption": "Figure 4: SSH in Mac OS"
    }
}]$

- Enter "`ssh pi@192.168.12.1`" in the terminal for you to logged into the LoRa Gateway, the default password is "raspberry".
- If you connect your PC with the LoRa Gateway through Ethernet Cable, you should enter "`ssh pi@192.168.10.10`", the default password is "raspberry".

### For Linux

If the OS of your PC is Linux, you should do the same as the Mac OS, except for the root mode.

