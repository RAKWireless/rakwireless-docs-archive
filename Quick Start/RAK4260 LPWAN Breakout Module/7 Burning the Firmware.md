---
type: page
title: Burning the Firmware
listed: false
slug: burning-the-firmware
---published

The **RAK4260** LPWAN Breakout Module is based on Microchip’s SIP and the firmware for the RAK4260 can also use the provided SDK of Microchip.

RAK has already compiled a Demo firmware for RAK4260 based on Microchip's SDK that can be downloaded freely for testing purposes: [https://github.com/RAKWireless/RAK4260-LoRaNode-demo](https://github.com/RAKWireless/RAK4260-LoRaNode-demo)

$plugin[{
    "type": "callout",
    "data": {
        "text": "This sample firmware is solely for testing purposes only. If you want to use and deploy your own, you have to make your own customized firmware based on Microchip SDK.",
        "type": "info",
        "title": "Note"
    }
}]$

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1579608539\/20857\/ovzw794dwmoh8axyrezk.png",
        "mode": "responsive",
        "width": 1934,
        "height": 1048,
        "caption": "**FIgure 1:** RAK4260 Github Repository"
    }
}]$

### Installing J-Flash

- Go to the Official Website of **Segger** where you can Download the J-Flash software: [https://www.segger.com/products/debug-probes/j-link/tools/j-flash/about-j-flash/](https://www.segger.com/products/debug-probes/j-link/tools/j-flash/about-j-flash/)

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1580057490\/20857\/za0zjvbmhukxwqkp5j1w.jpg",
        "mode": "responsive",
        "width": 1362,
        "height": 651,
        "caption": "**Figure 2:** Segger Official Website"
    }
}]$

- Download the software that corresponds to your Operating System, in this guide we will be using Windows OS.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1579964193\/20857\/wousuga7p4wzez8fbbsa.jpg",
        "mode": "responsive",
        "width": 1365,
        "height": 648,
        "caption": "**Figure 3:** J-link Software in different platforms"
    }
}]$

- After you have downloaded the corresponding software for your machine, install it and wait for a couple of minutes.

### Creating Project in J-Flash

- Upon opening the software, you will be greeted with the following window.  Choose **Create a new project**. Then Click **Start J-Flash.**

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1588949413\/29209\/hy2w4mi1tv8dbhyqquur.png",
        "mode": "responsive",
        "width": 1381,
        "height": 1062,
        "caption": "**Figure 4:**J-Flash new project window"
    }
}]$

- The next step is to select the right “**Target Device**”, to match the chip at the core of the RAK4260 LPWAN Breakout Module. Press the button with the dots on it in Figure 5, and you will be redirected to the selection screen.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1588949439\/29209\/dqf5mw3k7brx8xmubb4n.png",
        "mode": "responsive",
        "width": 1379,
        "height": 1065,
        "caption": "**Figure 5:** New project settings"
    }
}]$

- Select “**Atmel**” as the manufacturer via the drop-down menu and navigate to the **ATSAMR34J18** list entry. This is the chip at the core of the RAK4260 LPWAN Breakout Module, so we need to instruct the J-Flash tool that we are going to be working with it as shown in Figure 6.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1588949580\/29209\/wv96j8sgmn7laj4jkr8j.png",
        "mode": "responsive",
        "width": 1379,
        "height": 1067,
        "caption": "**Figure 6:** Device selection"
    }
}]$

- You will be redirected to the main project window where the newly selected device will be shown. Leave the rest of the parameters with their default values. If for some reason they diverge from what is shown in Figure 7, adjust them.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1588949662\/29209\/grk30s1drywsbtwp9vii.png",
        "mode": "responsive",
        "width": 1380,
        "height": 1064,
        "caption": "**Figure 7:** Project settings"
    }
}]$

- Now the new project will initialize and you need to instruct the tool to connect to the device. Do this by going to `Target → Connect` in the menu list on the top.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1588949773\/29209\/o5azftqsm0kjuepsx30q.png",
        "mode": "responsive",
        "width": 1379,
        "height": 1063,
        "caption": "**Figure 8:** Device connection"
    }
}]$

- The “**LOG**” window should reflect the connection process log and end up with a “**Connection successful**” message if everything went smoothly (Figure 9).

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1588949853\/29209\/qcd5h4g4xiab1espz93w.png",
        "mode": "responsive",
        "width": 1911,
        "height": 458,
        "caption": "**Figure 9**: Device log (connection successful)"
    }
}]$

- Now, choose the demo firmware that you have downloaded

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1588949980\/29209\/s0kf855zwvrxupm09i4e.png",
        "mode": "responsive",
        "width": 1115,
        "height": 860,
        "caption": "**Figure 10:** Loading the firmware file into the tool"
    }
}]$

- If you have managed to load the correct file the data in it will be visualized in a new window in HEX values. The only thing left to do now is tell the tool to flash it. Navigate to `Target → Production` Programming, or press **F7** to start the process.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1588950037\/29209\/fh7q9dkcvbcdvrjjy6zz.png",
        "mode": "responsive",
        "width": 1380,
        "height": 1063,
        "caption": "**Figure 11**: Flashing the firmware"
    }
}]$

- The firmware flashing process will initiate and there will be a blue bar that starts filling, reflecting the progress of the operation. Once the process completes successfully you will be shown a message window stating this, together with the time it took for the operation to finish (Figure 12).

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1588950182\/29209\/qpglo2lfvj9urcgi7p6q.png",
        "mode": "responsive",
        "width": 1380,
        "height": 1064,
        "caption": "**Figure 12:** Loading the firmware file into the tool"
    }
}]$

