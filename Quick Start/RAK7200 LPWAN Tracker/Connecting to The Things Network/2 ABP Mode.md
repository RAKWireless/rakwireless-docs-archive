---
type: page
title: ABP Mode
listed: true
slug: ttn-abp-mode
---published

1.To join the ABP mode, go to device settings and switch the activation method to **ABP**.

2.The **Device Address**, **Network Session Key** and **App Session Key** will be generated automatically by default.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1580631622\/17851\/ccjbidnd8e8hqvnjvc9g.png",
        "mode": "responsive",
        "width": 1934,
        "height": 1094,
        "caption": "**Figure 1:** Switching to ABP mode"
    }
}]$

3.Save the mode change and return to the **Device Overview page**. You can copy the keys by pressing the button after the value fields marked in red in Figure 2.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1580631633\/17851\/dann1wr9tchabmot7dqe.png",
        "mode": "responsive",
        "width": 1934,
        "height": 1094,
        "caption": "**Figure 2:** ABP Parameters Screen"
    }
}]$

4.Now we need to update the RAK7200 configuration (mode and parameters). Open the Serial Tool and type the command below to change the region (in case you have not done so already):

$plugin[{
    "type": "code-block",
    "data": {
        "languageBlocks": [
            {
                "code": "at+set_config=lora:region:EU868",
                "language": "none"
            }
        ]
    }
}]$

As you can see in **Figure 3**, as we were in the same region (EU868), there was no change.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1579612367\/17851\/zarmjkdjh4o6fisc0rfq.jpg",
        "mode": "responsive",
        "width": 2272,
        "height": 1482,
        "caption": "**Figure 3:** Region Setup"
    }
}]$

5.Change the mode to **ABP** with the command:

$plugin[{
    "type": "code-block",
    "data": {
        "languageBlocks": [
            {
                "code": "at+set_config=lora:join_mode:1",
                "language": "none"
            }
        ]
    }
}]$

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1579612378\/17851\/t5mjuy5rxxolrtiin8tt.jpg",
        "mode": "responsive",
        "width": 2277,
        "height": 1480,
        "caption": "**Figure 4:** Join Mode Setup"
    }
}]$

6.Now that the mode has been changed, enter the parameters: **Device Address, Network Session Key**, and **Application Session Key**. Use the commands below. Remember to replace the **"X"** with the corresponding parameter value for your particular case (Figure 2 for reference of the parameters):

$plugin[{
    "type": "code-block",
    "data": {
        "languageBlocks": [
            {
                "code": "at+set_config=lora:dev_addr:X",
                "language": "none"
            }
        ]
    }
}]$

$plugin[{
    "type": "code-block",
    "data": {
        "languageBlocks": [
            {
                "code": "at+set_config=lora:nwks_key:X",
                "language": "none"
            }
        ]
    }
}]$

$plugin[{
    "type": "code-block",
    "data": {
        "languageBlocks": [
            {
                "code": "at+set_config=lora:apps_key:X",
                "language": "none"
            }
        ]
    }
}]$

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1579612387\/17851\/tacqtzuayki77cruuwqc.jpg",
        "mode": "responsive",
        "width": 2262,
        "height": 1480,
        "caption": "**Figure 5:** Setting up the RAK7200 ABP Parameters"
    }
}]$

7.Finally execute the join command:

$plugin[{
    "type": "code-block",
    "data": {
        "languageBlocks": [
            {
                "code": "at+join",
                "language": "none"
            }
        ]
    }
}]$

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1579612396\/17851\/gc45ctfnhpmyurhjw7uj.jpg",
        "mode": "responsive",
        "width": 2289,
        "height": 1485,
        "caption": "**Figure 6:** Join Command"
    }
}]$

8.You can test the connection by sending an uplink frame. Use the following for example:

$plugin[{
    "type": "code-block",
    "data": {
        "languageBlocks": [
            {
                "code": "at+send=lora:1:12345678",
                "language": "none"
            }
        ]
    }
}]$

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1579612408\/17851\/yzu8x3arcigsctbjjvws.jpg",
        "mode": "responsive",
        "width": 920,
        "height": 600,
        "caption": "**Figure 7:** Sending an Uplink Frame"
    }
}]$

If you get a response in your TTN live data feed as in **Figure 8**, than you are all set!

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1580631670\/17851\/sxccujhjtfgxjkthyvy6.png",
        "mode": "responsive",
        "width": 1910,
        "height": 886,
        "caption": "**Figure 8:** Sending Data to TTN from RAK7200"
    }
}]$

