---
type: page
title: ABP Mode
listed: true
slug: chirpstack-abp-mode
---published

**1.** If you select “**DeviceProfile_ABP**” or “**DeviceProfile_ABP_CN470**”, it means you want to join ChirpStack in **ABP mode**.

$plugin[{
    "type": "callout",
    "data": {
        "text": "Frequency AS923  in ABP Mode is not supported in Chirpstack.",
        "type": "warning",
        "title": "Warning:"
    }
}]$

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1582559159\/24963\/sgmhz031rjwdryeko8cv.png",
        "mode": "responsive",
        "width": 1909,
        "height": 1093,
        "caption": "**Figure 1**: Chirpstack ABP Activation"
    }
}]$

**2.** Then you can see that there are some parameters for ABP in the “**ACTIVATION**” item:

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1582559249\/24963\/anv0xqjuyslnkiue0ltb.png",
        "mode": "responsive",
        "width": 1909,
        "height": 1094,
        "caption": "**Figure 2**: Chirpstack ABP Activation Parameters Needed"
    }
}]$

**3.** Use these parameters to set RAK5205 WisTrio LPWAN Tracker by using AT command. Set **LoRa® join** mode to **ABP**:

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
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1579529636\/24043\/iqptivjfhqaf9rkoxfwb.jpg",
        "mode": "responsive",
        "width": 555,
        "height": 675,
        "caption": "**Figure 3**: Chirpstack ABP Join Mode via RAK Serial Port Tool"
    }
}]$

**4.** Set LoRa® class to **Class A**:

$plugin[{
    "type": "code-block",
    "data": {
        "languageBlocks": [
            {
                "code": "at+set_config=lora:class:0",
                "language": "none"
            }
        ]
    }
}]$

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1579529642\/24043\/kkm5pwzhi44aif78akij.jpg",
        "mode": "responsive",
        "width": 558,
        "height": 673,
        "caption": "**Figure 4**: Chirpstack ABP Set Class via RAK Serial Port Tool"
    }
}]$

**5.** Set the frequency/region to **EU868**:

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

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1579529648\/24043\/hybihb6l6knq8lccnm1h.jpg",
        "mode": "responsive",
        "width": 558,
        "height": 673,
        "caption": "**Figure 5**: Chirpstack ABP Set Region\/Frequency via RAK Serial Port Tool"
    }
}]$

**6.** Set the **Device Address**:

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
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1579529660\/24043\/tpqvwwbxnmlwzqcfgozy.jpg",
        "mode": "responsive",
        "width": 557,
        "height": 666,
        "caption": "**Figure 6**: Chirpstack ABP Set Device Address via RAK Serial Port Tool"
    }
}]$

**7.** Set the **Network Session Key**:

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
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1579529666\/24043\/gzryq4icdnjuxykqgfhz.jpg",
        "mode": "responsive",
        "width": 562,
        "height": 677,
        "caption": "**Figure 7**: Chirpstack ABP Set Network Session Key via RAK Serial Port Tool"
    }
}]$

**8.** Set the **Application Session Key**:

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
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1579529673\/24043\/czhbmtdl7or1c2d6katt.jpg",
        "mode": "responsive",
        "width": 550,
        "height": 670,
        "caption": "**Figure 8**: Chirpstack ABP Set Application Session Key via RAK Serial Port Tool"
    }
}]$

$plugin[{
    "type": "callout",
    "data": {
        "text": "After configuring all parameters, you need to reset RAK5205 WisTrio LPWAN Tracker for saving parameters!",
        "type": "info",
        "title": "Note:"
    }
}]$

**9.** After resetting RAK5205 WisTrio LPWAN Tracker, join in ABP mode:

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
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1579529681\/24043\/b3oaamuv6fom8bydg1mi.jpg",
        "mode": "responsive",
        "width": 556,
        "height": 675,
        "caption": "**Figure 9**: Chirpstack ABP Join via RAK Serial Port Tool"
    }
}]$

$plugin[{
    "type": "callout",
    "data": {
        "text": "Actually,\nit is not needed to join in ABP mode. But you still need to set this AT command to\nvalidate the parameters which you just set for ABP mode.",
        "type": "info",
        "title": "Note:"
    }
}]$

**10.** Now, let’s try to send a data from RAK5205 WisTrio LPWAN Tracker to ChirpStack:

$plugin[{
    "type": "code-block",
    "data": {
        "languageBlocks": [
            {
                "code": "at+send=lora:2:1234567890",
                "language": "none"
            }
        ]
    }
}]$

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1579529685\/24043\/elbbdyduu3bbgnopsvns.jpg",
        "mode": "responsive",
        "width": 557,
        "height": 673,
        "caption": "**Figure 10**: Chirpstack Sample Data Sent via RAK Serial Port Tool"
    }
}]$

- You can then see the data which is just sent from RAK5205 WisTrio LPWAN Tracker on ChirpStack page:

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1582559274\/24963\/wv0gms26hbo1cktpspfe.png",
        "mode": "responsive",
        "width": 1934,
        "height": 1094,
        "caption": "**Figure 11**: Chirpstack Data Received Preview"
    }
}]$

