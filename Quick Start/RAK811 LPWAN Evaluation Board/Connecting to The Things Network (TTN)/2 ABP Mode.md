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
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1580627024\/17643\/ghtjt9jvmsfgkbqyrbkz.png",
        "mode": "responsive",
        "width": 1934,
        "height": 1094,
        "caption": "**Figure 1**: Switching to ABP Mode"
    }
}]$

3.Save the mode change and return to the **Device Overview page**. You can copy the keys by pressing the button after the value fields marked in red in **Figure 2**.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1580627044\/17643\/pexuiehqh0dkh1hjpymk.png",
        "mode": "responsive",
        "width": 1934,
        "height": 1094,
        "caption": "**Figure 2**: ABP Parameters Window"
    }
}]$

4.Now, we need to update the RAK811 configuration (mode and parameters). Open the RAK Serial Port Tool and type the command below to change the region (in case you have not done so already):

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
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1579523826\/17643\/gkaye44gsjjuxhtptjmv.png",
        "mode": "responsive",
        "width": 1372,
        "height": 901,
        "caption": "**Figure 3**: Region Setup"
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
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1579523877\/17643\/xxgmfyq9dkgzu7hcfq4g.png",
        "mode": "responsive",
        "width": 1374,
        "height": 898,
        "caption": "**Figure 4**: Join Mode Setup"
    }
}]$

6.Now that the mode has been changed, enter the parameters: **Device Address, Network  Session Key**, and **Application Session Key**. Use the commands below. Remember to replace the **"X"** with the corresponding parameter value for your particular case (**Figure 2** for reference of the parameters):

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
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1579524005\/17643\/yjupd0dh7ytr1rzqe118.png",
        "mode": "responsive",
        "width": 1373,
        "height": 897,
        "caption": "**Figure 5:** Setting up the RAK811 ABP Parameters"
    }
}]$

You should end up with a window as the one in **Figure 5** above (**a series of OK messages**).

7.Finally, execute the join command:

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
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1579524076\/17643\/y81mijqfbzfvhxlvt8qm.png",
        "mode": "responsive",
        "width": 1373,
        "height": 898,
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
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1579524163\/17643\/tfs0ngbmzluoex9gl3kn.png",
        "mode": "responsive",
        "width": 1376,
        "height": 900,
        "caption": "**Figure 7:** Sending an uplink frame"
    }
}]$

- If you get a response in your TTN live data feed as in **Figure 8**, than you are all set!

$plugin[{
    "type": "callout",
    "data": {
        "text": "Be sure to have this window opened prior to sending data through the RAK Serial Port or you will not be able to receive the packet sent. Logging out your The Things Network acccount would also clear all the data sent and not being able to receive packets sent.",
        "type": "info",
        "title": "Note:"
    }
}]$

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1580631337\/17643\/zf2brgmub8kkthb87j8y.png",
        "mode": "responsive",
        "width": 1910,
        "height": 886,
        "caption": "**Figure 8:** Sending Data to TTN from RAK811"
    }
}]$

