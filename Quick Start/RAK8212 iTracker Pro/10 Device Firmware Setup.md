---
type: page
title: Device Firmware Setup
listed: true
slug: device-firmware-setup
---published

An easy and quick way to have a fully functional **RAK8212 iTracker Pro** is by using a Pre-compiled Firmware Image provided. In this document are the step by step instructions on how to install the Image into your device.

### Burn the latest Firmware

1.If you want to get a pre-compiled firmware instead of compiling the source code by
yourself, you can find the latest firmware on RAK website **[here](https://downloads.rakwireless.com/en/Cellular/RAK8212/Firmware/)**.

2.Download and install **J-Link tool** on your Windows PC. You can download it **[here](https://downloads.rakwireless.com/en/Cellular/RAK8212/Tool/)**.

3.Connect the RAK8212 iTracker Pro with your PC through through your JTAG Emulator Kit as follows:

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1572177267\/21933\/e85ljqeubbgacmtfqm6e.jpg",
        "mode": "responsive",
        "width": 428,
        "height": 572,
        "caption": "**Figure 1**: RAK8212 to Windows PC connection thru JTag Emulator Kit"
    }
}]$

4.Now, **Open** the program “**J-Flash V6.41a**” which you just installed and click “**Start J-Flash**”

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1580196489\/21933\/pfxc6gdoyv8djlndcfgt.jpg",
        "mode": "responsive",
        "width": 878,
        "height": 701,
        "caption": "**Figure 2**: J-Flash Start Connection"
    }
}]$

5.Click the **button** marked with the **red box** in the image below labeled **Figure 3**, then you can see the
following page as shown in **Figure 4** and in the table provided. 

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1580196499\/21933\/ewkidffcazavmmscfdta.jpg",
        "mode": "responsive",
        "width": 867,
        "height": 670,
        "caption": "**Figure 3**: J-Flash Target Device Choosing"
    }
}]$

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1580196507\/21933\/ydqhs7betd9x9vty0bwf.jpg",
        "mode": "responsive",
        "width": 872,
        "height": 669,
        "caption": "**Figure 4**: J-Flash Target Device Parameter"
    }
}]$

| **Parameter** | **Value** | 
| ---- | ---- | 
| Manufacturer | Nordic Semiconductor | 
| Device | nRF52832_xxAA | 
| Core | Cortex-M4 | 
| Flash Size | 512 KB + 4 KB | 
| RAM Size | 64 KB | 


6.Click **OK** and a window pops-up as shown in the image below:

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1580196523\/21933\/rrdddufy1ykhtnoz85fm.jpg",
        "mode": "responsive",
        "width": 892,
        "height": 688,
        "caption": "**Figure 5**: J-Flash Target Device Parameter Selection Window"
    }
}]$

7.Now, connect to the RAK8212 iTracker Pro by navigating through **Target>Connect** in the **Main Menu.**

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1580196534\/21933\/dh4mpqr9z45vcqlpb9xh.jpg",
        "mode": "responsive",
        "width": 885,
        "height": 681,
        "caption": "**Figure 6**: Connecting to the RAK8212 iTracker Pro"
    }
}]$

$plugin[{
    "type": "callout",
    "data": {
        "text": "If connection is unsuccessful, please recheck the connections between the RAK8212 iTracker Pro, JTAG, and the connecting wires.",
        "type": "info",
        "title": "Note:"
    }
}]$

8.Open the download firmware of the RAK8212 iTracker Pro by dragging it into the window as shown in the image below:

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1580196541\/21933\/jrtcho26jvqd43gceelw.jpg",
        "mode": "responsive",
        "width": 818,
        "height": 627,
        "caption": "**Figure 7**: RAK8212 Firmware Opening"
    }
}]$

9.Before going into the firmware process, make sure to have the old firmware erased in the chip by navigating through **Target>Manual Programming>Erase Chip** in the **Main Menu** or by doing the process shown in the image below:

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1580196548\/21933\/nqtp5abjixx7ejfvlu21.jpg",
        "mode": "responsive",
        "width": 823,
        "height": 634,
        "caption": "**Figure 8**: RAK8212 Old Firmware Data Erasing"
    }
}]$

10.After the successful erasing of the old Firmware, you can start to burn the new firmware into RAK8212 iTracker Pro by navigating through **Target>Production Programming** in the **Main Menu** or by Pressing "**F7**".

11.Wait for a couple of seconds and a notification pop-ups showing a successful burning of the updated firmware as shown in the image below:

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1580196557\/21933\/eqagc4qeasa4xvpbypx9.jpg",
        "mode": "responsive",
        "width": 814,
        "height": 626,
        "caption": "**Figure 9**: RAK8212 Firmware Burning Successful"
    }
}]$

### Firmware Logs Checking

1.**Open** the program “**J-Link
RTT Viewer V6.41a**” which you just installed and click **OK**.

2.Choose the parameters as shown in the image and in the table provided below and click **OK**.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1580196608\/21933\/dquesjm84olj0q61vidc.jpg",
        "mode": "responsive",
        "width": 1022,
        "height": 547,
        "caption": "**Figure 10**: Firmware Log Checking Parameters"
    }
}]$

| **Parameter** | **Value** | 
| ---- | ---- | 
| Manufacturer | Nordic Semiconductor | 
| Device | nRF52832_xxAA | 
| Core | Cortex-M4 | 
| Flash Size | 516 KB | 
| RAM Size | 64 KB | 


3.Connect by navigating through **File>Connect** in the **Main Menu** or by pressing "**F2**".

4.A sample log is shown in the image below:

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1580196615\/21933\/n72yss9n4olrt2sqb1tv.jpg",
        "mode": "responsive",
        "width": 1032,
        "height": 550,
        "caption": "**Figure 11**: Firmware Log Sample"
    }
}]$

$plugin[{
    "type": "callout",
    "data": {
        "text": "If no logs are shown upon connecting, try resetting the RAK8212 iTracker Pro and redo the Firmware Logs Checking Section",
        "type": "info",
        "title": "Note:"
    }
}]$

