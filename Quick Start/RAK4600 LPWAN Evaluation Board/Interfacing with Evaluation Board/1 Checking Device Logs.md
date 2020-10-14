---
type: page
title: Checking Device Logs
listed: true
slug: checking-device-logs
---published

There are 2 ways that you can check the logs for debugging purposes on your RAK4600 LPWAN Evaluation Board:

1. **Through J-Link RTT Viewer**
2. **Through UART**

### Through J-Link RTT Viewer

1. If you want to check the logs of RAK4600 LPWAN Evaluation Board using this method, make sure you have connected the RAK4600 LPWAN Evaluation Board with your PC through JTAG like the following diagram below:

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1580179235\/22597\/zyvc5cexqy2g04lh5gqm.png",
        "mode": "responsive",
        "width": 6170,
        "height": 3114,
        "caption": null
    }
}]$

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1580137919\/22597\/yrwn46pfwepuhlh1wuof.png",
        "mode": "responsive",
        "width": 4041,
        "height": 1633,
        "caption": "**Figure 1**: RAK4600 LPWAN Evaluation Board to Windows PC connection thru JTAG"
    }
}]$

$plugin[{
    "type": "callout",
    "data": {
        "text": "You still have to connect the Micro-usb Cable to the RAK4600 LPWAN Evaluation Board to power the board.",
        "type": "warning",
        "title": "Note"
    }
}]$

**2.**Go to the Official Website of **Segger** where you can Download the [J-Flash software](https://www.segger.com/products/debug-probes/j-link/tools/j-flash/about-j-flash/). Open the program “**J-Link RTT Viewer V6.60f**” and choose "**USB**" for the type of connection to J-Link. After which, press "**OK**".

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1580544863\/22597\/k40v5ssykcsgrwfvd6ds.png",
        "mode": "responsive",
        "width": 1934,
        "height": 1048,
        "caption": "**Figure 2**: J-Link RTT Viewer Start-up Window"
    }
}]$

**3.** Choose the device parameters as the following picture shows and press "OK".

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1580544879\/22597\/xjnmuyygdpfhmjbko2dn.png",
        "mode": "responsive",
        "width": 1160,
        "height": 655,
        "caption": "**Figure 3**: J-Link RTT Viewer Connection Parameters"
    }
}]$

**4. Connect** to your RAK4600 by navigating through File>Connect in the Main Menu. Alternatively, you could just press "**F2**" to do the same process.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1580544925\/22597\/xhppkxsyq7k0zste4xpx.png",
        "mode": "responsive",
        "width": 1934,
        "height": 1047,
        "caption": "**Figure 4**: J-Link RTT Viewer Connecting Shortcut"
    }
}]$

**5.** Once connection is obtained, you should see the same log as shown in the image below:

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1580277880\/22597\/uvpxna4236xrglaamrcx.jpg",
        "mode": "responsive",
        "width": 944,
        "height": 376,
        "caption": "**Figure 5**: Log Checking through J-Link RTT Viewer"
    }
}]$

$plugin[{
    "type": "callout",
    "data": {
        "text": "If there is no log after connecting successfully, you can try to reset RAK4600 or double check the connection of JTAG.",
        "type": "info",
        "title": "Note:"
    }
}]$

### Through UART

**1.** If you want to check the log of RAK4600 through UART, you should make sure that RAK4600 has been connected with your PC through UART correctly as the following picture shows:

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1580142044\/22597\/munukxglkrz6vw7n9tow.jpg",
        "mode": "responsive",
        "width": 1600,
        "height": 600,
        "caption": "**Figure 6**: UART to RAK4600 LPWAN Evaluation Board Connection"
    }
}]$

$plugin[{
    "type": "callout",
    "data": {
        "text": "You still have to connect the Micro-usb Cable to the RAK4600 LPWAN Evaluation Board to power the board.",
        "type": "warning",
        "title": "Note:"
    }
}]$

**2.** Open the RAK Serial Port Tool as described in [auto$](/rak4600-lora-evaluation-board/interfacing-with-rak4600).

**3.** Press the Reset Button on the RAK4600 LPWAN Evaluation Board then you will see the following contents in the Serial port Tool.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1580277910\/22597\/ebx6auejnil1ob8hvhaf.jpg",
        "mode": "responsive",
        "width": 555,
        "height": 673,
        "caption": "**Figure 7**: Log Checking through UART"
    }
}]$

