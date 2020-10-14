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
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1564888854\/17851\/pa1zmfhkpuu9lfw1okef.jpg",
        "mode": "responsive",
        "width": 1916,
        "height": 883,
        "caption": "**Figure 1**. Switching to ABP mode"
    }
}]$

3.Save the mode change and return to the **Device Overview page**. You can copy the keys by pressing the button after the value fields marked in red in Figure 2.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1564889176\/17851\/wdjt8xi7fwyxlptr27dn.jpg",
        "mode": "responsive",
        "width": 1899,
        "height": 937,
        "caption": "**Figure 2**. ABP parameters screen"
    }
}]$

4.Now we need to update the RAK7200 configuration (mode and parameters). Open the Serial Tool and type the command below to change the region (in case you have not done so already):

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
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1564889347\/17851\/pmnpwgxlylnbdng3spu4.jpg",
        "mode": "responsive",
        "width": 2258,
        "height": 1468,
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
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1564889435\/17851\/fl5dtsjzh4npqpulg8il.jpg",
        "mode": "responsive",
        "width": 2263,
        "height": 1466,
        "caption": "**Figure 4**. Join mode setup"
    }
}]$

6.Now that the mode has been changed, enter the parameters: **Device Address, Network Session Key**, and **Application Session Key**. Use the commands below. Remember to replace the **"X"** with the corresponding parameter value for your particular case (Figure 2 for reference of the parameters):

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
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1564889741\/17851\/y0xc1ihj9d9wmc2qarbt.jpg",
        "mode": "responsive",
        "width": 2248,
        "height": 1466,
        "caption": "**Figure 5.** Setting up the RAK7200 ABP parameters"
    }
}]$

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
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1564889937\/17851\/o5ssq5scpmdzpc6q1qit.jpg",
        "mode": "responsive",
        "width": 2275,
        "height": 1471,
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
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1564890126\/17851\/br95560rtmznrqry9jhc.jpg",
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
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1564890186\/17851\/hc6c7k8vh0eoz0yskds8.jpg",
        "mode": "responsive",
        "width": 1904,
        "height": 914,
        "caption": "**Figure 6.** Sending Data to TTN from RAK7200"
    }
}]$

