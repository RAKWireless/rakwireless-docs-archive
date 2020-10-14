---
type: page
title: Access the Gateway
listed: true
slug: access-the-gateway
---published

### Wi-Fi AP Mode

By default, the firmware is configured to operate the Raspberry Pi in Wi-Fi AP mode, which means that you should be able to find an SSID named “Rakwireless_XXXX” on the Wi-Fi network list, for example:

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1593056814\/31135\/zga7jztdzjbeiyp7ijbc.jpg",
        "mode": "600",
        "width": 1100,
        "height": 230,
        "caption": "**Figure 1**: RAKWireless Access Point"
    }
}]$

- The default password for the AP: **rakwireless**.
- The default IP address of the Raspberry Pi: **192.168.230.1.** This is also the address you will be using to SSH into the OS.
- There is no need to configure the IP address of your PC as it will be assigned automatically via the DHCP server.

## Log into the Raspberry through SSH

### 1. Windows OS

SSH (Secure Shell) is used to login to a remote machine and to execute commands. There are several free and good SSH Clients available such as [**Putty**](https://www.chiark.greenend.org.uk/~sgtatham/putty/latest.html), [**BitVise SSH Client**](https://www.bitvise.com/ssh-client-download), and [**MobaXterm**](https://mobaxterm.mobatek.net/). You are free to choose one that fits your needs, however, in this guide, you will be using Putty.

After installation, open Putty and connect with the OS through Wi-Fi AP mode. The IP address is 192.168.230.1.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1593058595\/31135\/kw8lfjithzwsia2fjajb.png",
        "mode": "600",
        "width": 691,
        "height": 690,
        "caption": "**Figure 2**: Putty Software for SSH in Windows"
    }
}]$

- Click open and it will prompt you to enter the username and password. 
- The default username: **pi**
- The default password: **raspberry**

Upon successful login, you should see the initial screen with the messages notifying you that you should change your password. Refer to figure 3.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1593058968\/31135\/ya8udk8rdpptkk06fmaa.jpg",
        "mode": "600",
        "width": 989,
        "height": 750,
        "caption": "**Figure 3**: Command line after login"
    }
}]$

### 2. Mac OS

Open the terminal of Mac OS. Then, launch the **Terminal** application found in this directory: **/Applications/Utilities/**. You can also launch it from Spotlight by hitting **Command + Spacebar** and typing “Terminal” and then return:

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1593059172\/31135\/s69n8r0jizbksqh3loop.png",
        "mode": "600",
        "width": 1381,
        "height": 876,
        "caption": "**Figure 4:** Mac OS Terminal"
    }
}]$

Open the terminal of Mac OS. Enter **root mode** by typing the following command: `sudo -i`.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1593061254\/31135\/e0zgirgzlovoaoxnr7ao.jpg",
        "mode": "responsive",
        "width": 988,
        "height": 158,
        "caption": "**Figure 5**:  SSH in Mac OS"
    }
}]$

- If you are not in root mode, enter `ssh pi@192.168.230.1` in the terminal to login to your gateway. The default password is **raspberry**.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1593061633\/31135\/ibvqtc0m9kkuxlb7uwor.jpg",
        "mode": "responsive",
        "width": 990,
        "height": 211,
        "caption": "**Figure 6**: Log into the Raspberry"
    }
}]$

### 3. Linux

 If you are using Linux the procedure is the same as the one for Mac OS.

