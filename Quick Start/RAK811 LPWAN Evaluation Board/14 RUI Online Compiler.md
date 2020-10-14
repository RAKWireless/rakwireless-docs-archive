---
type: page
title: RUI Online Compiler
listed: true
slug: rui-online-compiler
---published

This document is a detailed walk through on how to use the RUI Online Compiler recently release by RAKwireless. Such tool is useful to minimize the steps undergone in the [Firmware Customizing](https://doc.rakwireless.com/rak811-lora---evaluation-board/burning-the-bootloader-into-the-device) document.

## Account Creation and Log-in Interface

$plugin[{
    "type": "callout",
    "data": {
        "text": "To avoid errors in the firmware compiling using the RUI Online Compiler, it is best advised to use Google Chrome as your Web Browser as this was the browser our technical team used upon testing. If you have not installed the Google Chrome browser, kindly download and install it from **[here](https:\/\/www.google.com\/chrome\/)**.",
        "type": "info",
        "title": "Note:"
    }
}]$

1.Using your recently installed Google Chrome Web Browser, open the link, [RUI Online Compiler](http://47.112.137.11:12090/#/user/login) and you should see the log-in interface same as in the image below.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1579526898\/23625\/b1osq3zcjjisbeqhbw5v.png",
        "mode": "responsive",
        "width": 825,
        "height": 590,
        "caption": "**Figure 1**: RUI Online Compiler Log-in Window"
    }
}]$

2.If this is your first time doing this, kindly create an account by clicking through "**Create an account**" button. 

3.A new window pops-up same as in the image below. You are asked to input your **e-mail address**,your chosen **password** and your **verification code** by clicking the "**Get Verification Code**" button. 

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1579526941\/23625\/braswhitebuh33oaz3ns.png",
        "mode": "responsive",
        "width": 831,
        "height": 622,
        "caption": "**Figure 2**: RUI Online Compiler Sign-up Window"
    }
}]$

$plugin[{
    "type": "callout",
    "data": {
        "text": "Go to your e-mail and check the verification sent when you clicked the \"**Get Verification Code**\" button. Note that you are only given **120 seconds** to have the verification attached in the **Create Account** window.",
        "type": "info",
        "title": "Note:"
    }
}]$

4.Once the three information, **e-mail address**, **password** and **verification code** are supplied, click the "**Create an account**" button in the bottom. Once creating an account is successful, you are then asked to log-on your credentials in the link attached in **Step 1**.

## Selecting and uploading

After your successful sign-up and log-in done in the previous section, you should see the following page below:

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1579527138\/23625\/sc05a2h4fxqgiuit8ltj.png",
        "mode": "responsive",
        "width": 1933,
        "height": 880,
        "caption": "**Figure 3**: RUI Online Compiler Dashboard"
    }
}]$

### Product Model Selection

1.Select the **Core Module** which you want to do customization based on. 

$plugin[{
    "type": "callout",
    "data": {
        "text": "As of now, we only supply **RAK8212**, **RAK5010**, **RAK4600**, **RAK4400**, **RAK811-L**, **RAK811-H**, and **RAK4200** modules. Our team is still in the processing of having most of our devices be programmable so watch for further updates.",
        "type": "info",
        "title": "Note:"
    }
}]$

### Choosing the Upload File

2.Click "**Select file to upload**” button to choose the **.zip file** which includes all source code of your own customized Application.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1579527192\/23625\/berjqqxwurxifkoikdrb.png",
        "mode": "responsive",
        "width": 1933,
        "height": 883,
        "caption": "**Figure 4**: Choosing your Customized .zip file in the RUI Online Compiler"
    }
}]$

Please note that, this .zip file can be made as the following pictures show as an example:

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1579527238\/23625\/bulgldidt55ohueksrcg.png",
        "mode": "responsive",
        "width": 1118,
        "height": 328,
        "caption": "**Figure 5**: Sample files in the Customized Application .zip File"
    }
}]$

3.After choosing the correct .zip file on your chosen directory, press "**Open**" and proceed to the next section.

### File Uploading

4.After choosing the corresponding .zip file from the previous section, press the "**Upload**" button as shown in the image below to begin the uploading process.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1579527283\/23625\/dmxy8pph3jd6lzwh3l1z.png",
        "mode": "responsive",
        "width": 1933,
        "height": 878,
        "caption": "**Figure 6**: RUI Online Compiler Uploading"
    }
}]$

5.A corresponding "**Upload Success**" notification then pops-up in your window once the uploading of the .zip file is successful same as with the image below:

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1579527410\/23625\/tjkmvecfptby0ilwwqkc.png",
        "mode": "responsive",
        "width": 1933,
        "height": 882,
        "caption": "**Figure 7**: RUI Online Compiler Uploading Success"
    }
}]$

### Compiling

6.Once uploading is done, you can now start compiling your customized application by clicking the "**Compile**" button same as with the image below:

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1579527460\/23625\/hyrhkcj18gz4tgccqwko.png",
        "mode": "responsive",
        "width": 1933,
        "height": 882,
        "caption": "**Figure 8**: RUI Online Compiler Compiling"
    }
}]$

Corresponding logs also can be seen in the "**Compile log output**" monitor same with the image shown below:

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1579527626\/23625\/hxjpzr1sv5nw0a5ipuhi.png",
        "mode": "responsive",
        "width": 1932,
        "height": 882,
        "caption": "**Figure 9**: RUI Online Compiler Compiling Logs"
    }
}]$

7.After compiling successfully, a new **.zip file** which includes two files, one is "**compile log file**", the other is the "**final customized firmware**" same with the image shown below:

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1579527675\/23625\/eckuj9mipbwefieupcpz.png",
        "mode": "responsive",
        "width": 1933,
        "height": 882,
        "caption": "**Figure 10:**  Final Customized Firmware Auto-downloaded"
    }
}]$

$plugin[{
    "type": "callout",
    "data": {
        "text": "For failed compiling instances, the .zip file automatically downloaded shall only contain \"**compile log file**\" which would contain the errors occurred upon compiling.",
        "type": "info",
        "title": "Note:"
    }
}]$

$plugin[{
    "type": "callout",
    "data": {
        "text": "For failed auto-downloading of your Final Customized Firmware instances, kindly **turn-off all third party download managers** (i.e. Internet Download Manager) and redo the Compiling process.",
        "type": "info",
        "title": "Note:"
    }
}]$

8.For the successful compiling, a sample image is shown below with the .zip file containing both "**compile log file**", and the "**final customized firmware**" .bin file.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1579527766\/23625\/aca52o0ukf3kzcoriatp.png",
        "mode": "responsive",
        "width": 463,
        "height": 92,
        "caption": "**Figure 11**: Final Customized Firmware sample File"
    }
}]$

9.The **newly compiled .bin file** will then be burned into your device by following the steps in the [Upgrading the Firmware](https://doc.rakwireless.com/rak811-lora---evaluation-board/upgrading-the-firmware) document.

