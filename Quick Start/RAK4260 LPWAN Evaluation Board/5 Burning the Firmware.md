---
type: page
title: Burning the Firmware
listed: true
slug: burning-the-firmware
---published

**RAK4260**  is an LPWAN Module based on Microchip’s SIP and the firmware for the RAK4260 can also use the provided SDK of Microchip.

RAK has already compiled a Demo firmware for RAK4260 based on Microchip's SDK that can be downloaded freely for testing purposes: [https://github.com/RAKWireless/Update-File/blob/master/RAK4260_Demo.hex](https://github.com/RAKWireless/RAK4260-LoRaNode-demo)

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
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1579965415\/20857\/vl2mba456yubtqzka3xr.jpg",
        "mode": "responsive",
        "width": 927,
        "height": 717,
        "caption": "**Figure 4:**  J-flash Interface"
    }
}]$

- You will be then prompt to configure your new Project. Select the Target Device by clicking the box labeled red below: 

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1579965123\/20857\/fbpgwsnb9ejns9oqncde.jpg",
        "mode": "responsive",
        "width": 931,
        "height": 716,
        "caption": "**Figure 5:** Configuring the Project"
    }
}]$

- Select the Manufacturer to **Atmel** and Select the Device **Atmel ATSAML21J18 .**

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1580133461\/20857\/ggc8v1ji5w7kc74183et.png",
        "mode": "responsive",
        "width": 770,
        "height": 512,
        "caption": "**Figure 6:** Selecting the Device"
    }
}]$

- Select the Target Interface to be **SWD** and the Speed (kHz) to be **4000** and Press **OK.**

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1579965133\/20857\/fenpa8t70czirau9hzj5.jpg",
        "mode": "responsive",
        "width": 926,
        "height": 716,
        "caption": "**Figure 7:** Target Interface and Speed (kHz)"
    }
}]$

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1579965138\/20857\/b0bjjzvpvwbflhha42ob.jpg",
        "mode": "responsive",
        "width": 927,
        "height": 717,
        "caption": "**Figure 8:** Created Project Successfully"
    }
}]$

### Connecting the RAK4260 LPWAN Evaluation Board with JTAG

- Connect the RAK4260 LPWAN Evaluation Board with your J-Link in your PC through JTAG (refer to the Figure Below)

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1580131779\/20857\/gjmxb2wpip0g66csjb37.png",
        "mode": "responsive",
        "width": 6170,
        "height": 3114,
        "caption": null
    }
}]$

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1580132130\/20857\/issx8md9eyldu4gu9enl.png",
        "mode": "responsive",
        "width": 4164,
        "height": 1626,
        "caption": "**Figure 9:** JTAG to RAK4260 Connections"
    }
}]$

- In the J-Flash software Menu Bar, Choose Target -> Connect 

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1580133526\/20857\/j9la3zo0fzaqv9kqeh8a.png",
        "mode": "responsive",
        "width": 930,
        "height": 717,
        "caption": "**Figure 10:** Connect to the RAK4260"
    }
}]$

- If everything works properly, it will prompt "**Connected Successfully"** indicating that you have successfully connected the RAK4260 with J-Link.
- Now, choose the demo firmware that you have downloaded 

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1579965160\/20857\/c3f6u10buojlrfdtrrcs.jpg",
        "mode": "responsive",
        "width": 926,
        "height": 717,
        "caption": "**Figure 11:** Choosing the Demo Firmware"
    }
}]$

- After you choose the firmware, select Target -> Production Programming to start the flashing process and wait for a couple of minutes.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1580135067\/20857\/btzjzdldqcoluk9go5zp.png",
        "mode": "responsive",
        "width": 930,
        "height": 717,
        "caption": "**Figure 12:** Burning the Firmware"
    }
}]$

- The following picture below shows the correct log that we have successfully burned the firmware into our device:

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1579965173\/20857\/gx2inmvoh81mmpaxtedv.jpg",
        "mode": "responsive",
        "width": 959,
        "height": 369,
        "caption": "**Figure 13:** Success Burning of Firmware Log"
    }
}]$

