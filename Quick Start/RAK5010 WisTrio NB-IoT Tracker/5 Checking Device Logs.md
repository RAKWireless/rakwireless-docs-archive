---
type: page
title: Checking Device Logs
listed: true
slug: checking-device-logs
---published

There are 3 ways that you can check the logs for debugging purposes on your RAK5010 WisTrio NB-IoT Tracker:

1. **Through J-Link RTT Viewer**
2. **Through UART**
3. **Through Micro-USB**

### Through J-Link RTT Viewer

**1.** If you want to check the logs of RAK5010 WisTrio NB-IoT Tracker using this method, make sure you have connected the RAK5010 with your PC through JTAG like the following diagram below

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1578967864\/20384\/rrktg8blr065uoa0irl1.jpg",
        "mode": "responsive",
        "width": 3292,
        "height": 1520,
        "caption": "**Figure 1**: RAK5010 and PC Connection through JTAG"
    }
}]$

$plugin[{
    "type": "callout",
    "data": {
        "text": "You still have to connect the Micro USB Cable to the RAK5010 to power the board.",
        "type": "warning",
        "title": "Warning"
    }
}]$

**2.**Go to the Official Website of **Segger** where you can Download the [J-Flash software](https://www.segger.com/products/debug-probes/j-link/tools/j-flash/about-j-flash/). Open the program “**J-Link RTT Viewer V6.60f**” and choose "**USB**" for the type of connection to J-Link. After which, press "**OK**".

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1580437801\/20384\/xgdllxo7gb3ks0y3tbch.png",
        "mode": "responsive",
        "width": 1934,
        "height": 1055,
        "caption": "**Figure 2**: J-Link RTT Viewer"
    }
}]$

**3.** Choose the device parameters as the following picture shows or in the table provided and press "OK".

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1580490162\/20384\/wmoh5e7i8n6gxxr9h4o9.png",
        "mode": "responsive",
        "width": 1102,
        "height": 447,
        "caption": "**Figure 3**: J-Link Target Device Settings"
    }
}]$

| **Parameter** | **Data** | 
| ---- | ---- | 
| Manufacturer | Nordic Semi | 
| Device | nRF52840_xxAA | 
| Core | Cortex-M4 | 
| NumCores | 1 | 
| Flash Size | 1028 KB | 
| RAM Size | 256 KB | 


**4. Connect** to your RAK5010 by navigating through File>Connect in the Main Menu. Alternatively, you could just press "**F2**" to do the same process.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1569641005\/20384\/jrqm79eoaojwuynzdu1t.jpg",
        "mode": "responsive",
        "width": 1917,
        "height": 1016,
        "caption": "**Figure 4**: Connecting in J-Link RTT Viewer"
    }
}]$

**5.** Once connection is obtained, you should see the same log as shown in the image below:

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1580439153\/20384\/uku52cmdo7ccdzwbwubz.png",
        "mode": "responsive",
        "width": 1147,
        "height": 594,
        "caption": "**Figure 5**:  J-Link RTT Viewer showing RAK5010 Logs"
    }
}]$

$plugin[{
    "type": "callout",
    "data": {
        "text": "If there\nis no log after connecting successfully, you can try to reset RAK5010 or check\nthe connection of JTAG.",
        "type": "info",
        "title": "Note"
    }
}]$

### Through UART

**1.** If you want to check the log of RAK5010 through UART, you should make sure that RAK5010 has been connected with your PC through UART correctly as the following picture shows:

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1580437252\/20384\/vnimzkp0kinl9ri7y3zm.jpg",
        "mode": "responsive",
        "width": 6264,
        "height": 2151,
        "caption": "**Figure 6**: RAK5010 and USB-UART Connection"
    }
}]$

- Then open a serial port tool in your PC. If you haven’t a serial port tool, I recommend using RAK Serial Port Tool which you can download from **[here](https://downloads.rakwireless.com/en/LoRa/Tools/RAK_SERIAL_PORT_TOOL_V1.2.1.zip).**
- After pushing the RST button on RAK5010, you can see the following contents in the serial port tool:

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1569641286\/20384\/qsst0fqcss6tlwofo9ex.jpg",
        "mode": "300",
        "width": 540,
        "height": 661,
        "caption": "**Figure 7**: RAK Serial Port Tool"
    }
}]$

- OK, you can see the log through UART now.

### Through Micro USB

- To start with, connect RAK5010 with your PC through microUSB/USB as shown in the image below:

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1578968092\/20384\/cjkxyja4hkqovtiddklj.jpg",
        "mode": "responsive",
        "width": 3544,
        "height": 2020,
        "caption": "**Figure 8**: MicroUSB Interface for RAK5010"
    }
}]$

- Open the serial port tool in your PC.

$plugin[{
    "type": "callout",
    "data": {
        "text": "For this method, you need a serial port tool which can support DTR function,\nlike Termite. You can download Termite **[here](https:\/\/www.compuphase.com\/software_termite.htm)**.",
        "type": "info",
        "title": "Note:"
    }
}]$

- Alright, after opening the serial tool, configure its setting by following the picture below:

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1580436882\/20384\/gpubckbaii9vocy1h32u.png",
        "mode": "responsive",
        "width": 1035,
        "height": 717,
        "caption": "**Figure 9**: Termite Configuration Enabling DTR"
    }
}]$

Now, the Termite app will connect with RAK5010 automatically. Then
you can send AT commands and check the log in Termite:

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1580436975\/20384\/hqfcunna1swkknili72n.png",
        "mode": "responsive",
        "width": 1268,
        "height": 390,
        "caption": "**Figure 10**: Checked Log in Termite"
    }
}]$

