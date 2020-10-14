---
type: page
title: ABP Mode
listed: true
slug: ttn-abp-mode
---published

**1.** To join the ABP mode, go to device settings and switch the activation method to **ABP**.

**2.** The **Device Address**, **Network Session Key** and **App Session Key** will be generated automatically by default.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1582559420\/18993\/bs9ladvinybe4v0fqowm.png",
        "mode": "responsive",
        "width": 1934,
        "height": 1094,
        "caption": "**Figure 1**: Switching to ABP mode"
    }
}]$

**3.** Save the mode change and return to the **Device Overview page**. You can copy the keys by pressing the button after the value fields marked in red in Figure 2.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1582559431\/18993\/ytbwh3dd3u6ul6mw174p.png",
        "mode": "responsive",
        "width": 1934,
        "height": 1094,
        "caption": "**Figure 2**: ABP parameters screen"
    }
}]$

**4.** Now we need to update the RAK7204 configuration (mode and parameters). Open the Serial Tool and type the command below to change the region (in case you have not done so already):

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

As you can see in Figure 3, as we were in the same region (EU868), there was no change.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1579523826\/17643\/gkaye44gsjjuxhtptjmv.png",
        "mode": "responsive",
        "width": 1372,
        "height": 901,
        "caption": "**Figure 3**: Region setup"
    }
}]$

**5.** Change the mode to **ABP** with the command:

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
        "caption": "**Figure 4**: Join mode setup"
    }
}]$

**6.** Now that the mode has been changed, enter the parameters: **Device Address, Network  Session Key**, and **Application Session Key**. Use the commands below. Remember to replace the **"XXXX"** with the corresponding parameter value for your particular case (Figure 2 for reference of the parameters):

$plugin[{
    "type": "code-block",
    "data": {
        "languageBlocks": [
            {
                "code": "at+set_config=lora:dev_addr:XXXX",
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
                "code": "at+set_config=lora:nwks_key:XXXX",
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
                "code": "at+set_config=lora:apps_key:XXXX",
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
        "caption": "**Figure 5:** Setting up the RAK7204 ABP parameters"
    }
}]$

You should end up with a window as the one in **Figure 5** above with **a series of OK messages**.

**7.** Finally, execute the join command:

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
        "caption": "**Figure 6:** Join command"
    }
}]$

**8.** You can test the connection by sending an uplink frame. Use the following as an example:

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

If you get a response in your TTN live data feed as in Figure 8, then you are all set!

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1582559445\/18993\/uos1gg9ucwza8nmlt3v6.png",
        "mode": "responsive",
        "width": 1910,
        "height": 886,
        "caption": "**Figure 8:** Sending Data to TTN from RAK7204"
    }
}]$

