---
type: page
title: Checking Device Logs
listed: true
slug: checking-device-logs
---published

You can check the logs for debugging purposes on your RAK8212 iTracker Pro through **J-link RTT Viewer**

### Through J-link RTT Viewer

1.If you want to check the logs of RAK8212 iTracker Pro using this method, make sure you have connected the RAK8212 with your PC through JTAG like the following diagram below:

$plugin[{
    "type": "callout",
    "data": {
        "text": "You still have to connect the battery to the RAK8212 to power the board.",
        "type": "warning",
        "title": "Warning"
    }
}]$

2.Go to the Official Website of **Segger** where you can Download the [J-Flash software](https://www.segger.com/products/debug-probes/j-link/tools/j-flash/about-j-flash/). Open the program “**J-Link RTT Viewer V6.60f**” and choose "**USB**" for the type of connection to J-Link. After which, press "**OK**".

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1580611242\/25186\/yqqi3jf24gullejjki9f.png",
        "mode": "responsive",
        "width": 1948,
        "height": 1062,
        "caption": "**Figure 2**: J-Link RTT Viewer"
    }
}]$

3.Choose the device parameters as the following picture shows and press "**OK**".

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1580611333\/25186\/d7dgg4r2dc86tjawkqzw.png",
        "mode": "responsive",
        "width": 1174,
        "height": 669,
        "caption": "**Figure 3**: J-Link RTT Viewer Connection Parameters"
    }
}]$

4.**Connect** to your RAK8212 iTracker Pro by navigating through `File>Connect` in the Main Menu. Alternatively, you could just press "**F2**" to do the same process.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1580611939\/25186\/iqb42ghnf0wancwytkfu.png",
        "mode": "responsive",
        "width": 1948,
        "height": 1061,
        "caption": "**Figure 4**: Connecting to J-Link"
    }
}]$

5.Once connection is obtained, you should see the same log as shown in the image below:

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1580612005\/25186\/na9nw4tqriblnxmutxcc.png",
        "mode": "responsive",
        "width": 1076,
        "height": 411,
        "caption": "**Figure 5**: Log Checking through J-Link RTT Viewer"
    }
}]$

