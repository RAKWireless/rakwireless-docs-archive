---
type: page
title: ABP Mode
listed: true
slug: abp-mode
---published

Follow these steps, if you want to join with The Things Network in **Activation By Personalisation** (ABP) Mode.

1.First, switch the activation method to ABP as shown in the following image

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1580634741\/17092\/iogtfaiab0eiyzr8a2oi.png",
        "mode": "responsive",
        "width": 1934,
        "height": 1094,
        "caption": "**Figure 1**: APB Activation in The Things Network"
    }
}]$

2.These three parameters will be used on RAK612 LPWAN Button: **Device Address**, **Network Session Key** and **App Session Key**.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1580634760\/17092\/sckqwwwvn1o6nxtxj22d.png",
        "mode": "responsive",
        "width": 1934,
        "height": 1094,
        "caption": "**Figure 2**: ABP Parameters in The Things Network"
    }
}]$

$plugin[{
    "type": "callout",
    "data": {
        "text": "As an example, let's join in ABP mode and EU868 frequency.",
        "type": "info",
        "title": "Note:"
    }
}]$

3.If the join mode is not in ABP Mode, just set the LoRa® join mode to **ABP** as follows:

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1580521597\/17092\/i3u7fbasmosxhnxqkocm.jpg",
        "mode": "responsive",
        "width": 565,
        "height": 717,
        "caption": "**Figure 3**: AT Command for ABP LoRa\u00ae Join Mode via RAK Serial Port Tool"
    }
}]$

4.Set the frequency/region to **EU868**:

$plugin[{
    "type": "code-block",
    "data": {
        "languageBlocks": [
            {
                "code": "at+band=EU868",
                "language": "none"
            }
        ]
    }
}]$

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1580521765\/17092\/gyycegz3irkep0dlp78k.jpg",
        "mode": "responsive",
        "width": 572,
        "height": 721,
        "caption": "**Figure 4**: AT Command for ABP LoRa\u00ae Region\/Frequency via RAK Serial Port Tool"
    }
}]$

5.Set the **Device Address**:

$plugin[{
    "type": "code-block",
    "data": {
        "languageBlocks": [
            {
                "code": "at+set_config=dev_addr:XXXX",
                "language": "none"
            }
        ]
    }
}]$

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1580522037\/17092\/kkejoozziq66h3js71ls.jpg",
        "mode": "responsive",
        "width": 566,
        "height": 718,
        "caption": "**Figure 5**: AT Command for ABP LoRa\u00ae Device Address via RAK Serial Port Tool"
    }
}]$

6.Set the **Network Session Key**:

$plugin[{
    "type": "code-block",
    "data": {
        "languageBlocks": [
            {
                "code": "at+set_config=nwks_key:XXXX",
                "language": "none"
            }
        ]
    }
}]$

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1580522359\/17092\/mxjkc0jdhhfmzyc37aao.jpg",
        "mode": "responsive",
        "width": 566,
        "height": 721,
        "caption": "**Figure 6**: AT Command for ABP LoRa\u00ae Network Session Key via RAK Serial Port Tool"
    }
}]$

7.Set the **Application Session Key**:

$plugin[{
    "type": "code-block",
    "data": {
        "languageBlocks": [
            {
                "code": "at+set_config=apps_key:XXXX",
                "language": "none"
            }
        ]
    }
}]$

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1580522571\/17092\/aa3fabth4hy4df4p4rsp.jpg",
        "mode": "responsive",
        "width": 568,
        "height": 721,
        "caption": "**Figure 7**: AT Command for ABP LoRa\u00ae Application Session Key via RAK Serial Port Tool"
    }
}]$

$plugin[{
    "type": "callout",
    "data": {
        "text": "After configuring all parameters, you need to reset the RAK612 LPWAN Button for saving parameters.",
        "type": "info",
        "title": "Note:"
    }
}]$

8.After resetting your RAK612 LPWAN Button, join in **ABP mode**:

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1580522797\/17092\/fqxrwkmgasamxma6gjbj.jpg",
        "mode": "responsive",
        "width": 565,
        "height": 715,
        "caption": "**Figure 8**: AT Command for ABP LoRa\u00ae Join via RAK Serial Port Tool"
    }
}]$

Joined successfully! Now, let’s try to send a data to TTN. Try pressing any key on your RAK612 LPWAN Button. You should see any data printed in the RAK Serial Port Tool whenever you press any key same as with the image below:

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1580522949\/17092\/r14cjewfmts85rrd6ngw.jpg",
        "mode": "responsive",
        "width": 564,
        "height": 719,
        "caption": "**Figure 9**: Testing the RAK612 LoRa\u00ae Button in RAK Serial Port Tool"
    }
}]$

You can then see the data sent from RAK612 LPWAN BUtton in TTN website as follows:

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1580635061\/17092\/xx559fez2nmalg5wynjq.jpg",
        "mode": "responsive",
        "width": 1806,
        "height": 581,
        "caption": "**Figure 10**: ABP Test Sample Data Sent Viewed in The Things Network"
    }
}]$

