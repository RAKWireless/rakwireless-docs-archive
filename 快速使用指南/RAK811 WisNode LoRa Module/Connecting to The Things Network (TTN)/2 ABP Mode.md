---
type: page
title: ABP Mode
listed: true
slug: abp-mode
---published

1.To join the ABP mode, go to device settings and switch the activation method to **ABP**.

2.The **Device Address**, **Network Session Key** and **App Session Key** will be generated automatically by default.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1563500613\/17643\/jhlhrcahhyq3cwqetajs.jpg",
        "mode": "responsive",
        "width": 1934,
        "height": 934,
        "caption": "**Figure 1**. Switching to ABP mode"
    }
}]$

3.Save the mode change and return to the **Device Overview page**. You can copy the keys by pressing the button after the value fields marked in red in Figure 2.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1563500937\/17643\/owzqkvcyxiywh7opapjk.jpg",
        "mode": "responsive",
        "width": 1918,
        "height": 928,
        "caption": "**Figure 2**. ABP parameters screen"
    }
}]$

4.Now we need to update the RAK811 configuration (mode and parameters). Open the Serial Tool and type the command below to change the region (in case you have not done so already):

$plugin[{
    "type": "code-block",
    "data": {
        "languageBlocks": [
            {
                "code": "at+set_config=lora:region:EU868",
                "language": "javascript"
            }
        ]
    }
}]$

As you can see in Figure 3, as we were in the same region (EU868), there was no change.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1563501433\/17643\/izmh2qou1crci5thzyqr.jpg",
        "mode": "responsive",
        "width": 898,
        "height": 590,
        "caption": "**Figure 3**. Region setup"
    }
}]$

5.Change the mode to **ABP** with the command:

$plugin[{
    "type": "code-block",
    "data": {
        "languageBlocks": [
            {
                "code": "at+set_config=lora:join_mode:1",
                "language": "javascript"
            }
        ]
    }
}]$

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1563501597\/17643\/unlg9idnik768g4mayef.jpg",
        "mode": "responsive",
        "width": 903,
        "height": 587,
        "caption": "**Figure 4**. Join mode setup"
    }
}]$

6.Now that the mode has been changed, enter the parameters: **Device Address, Network  Session Key**, and **Application Session Key**. Use the commands below. Remember to replace the **"X"** with the corresponding parameter value for your particular case (Figure 2 for reference of the parameters):

$plugin[{
    "type": "code-block",
    "data": {
        "languageBlocks": [
            {
                "code": "at+set_config=lora:dev_addr:X\nat+set_config=lora:nwks_key:X\nat+set_config=lora:apps_key:X",
                "language": "javascript"
            }
        ]
    }
}]$

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1563502259\/17643\/c5knkxlxgbvvstbrro5t.jpg",
        "mode": "responsive",
        "width": 904,
        "height": 592,
        "caption": "**Figure 5.** Setting up the RAK811 ABP parameters"
    }
}]$

You should end up with a window as the one in **Figure 5** above (**a series of OK messages**).

7.Finally execute the join command:

$plugin[{
    "type": "code-block",
    "data": {
        "languageBlocks": [
            {
                "code": "at+join",
                "language": "javascript"
            }
        ]
    }
}]$

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1563502913\/17643\/gvvca32ydr37urofaali.jpg",
        "mode": "responsive",
        "width": 904,
        "height": 588,
        "caption": "**Figure 6.** Join command"
    }
}]$

8.You can test the connection by sending an uplink frame. Use the following for example:

$plugin[{
    "type": "code-block",
    "data": {
        "languageBlocks": [
            {
                "code": "at+send=lora:1:12345678",
                "language": "javascript"
            }
        ]
    }
}]$

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1563503084\/17643\/hpjyhmrocjtps17yhtwj.jpg",
        "mode": "responsive",
        "width": 906,
        "height": 586,
        "caption": "**Figure 7.** Sending an uplink frame"
    }
}]$

If you get a response in your TTN live data feed as in Figure 8, than you are all set!

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1563503174\/17643\/affiz19tyhob1z2uttfm.jpg",
        "mode": "responsive",
        "width": 1904,
        "height": 914,
        "caption": "**Figure 6.** Sending Data to TTN from RAK811"
    }
}]$

