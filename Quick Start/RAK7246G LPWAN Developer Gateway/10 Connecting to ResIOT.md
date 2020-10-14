---
type: page
title: Connecting to ResIOT
listed: true
slug: connecting-to-resiot
---published

ResIOT is a platform for  LoRaWAN®/LPWAN Networks and IoT Projects for Smart City or Industry 4.0. Cost-effective High availability and scalability. Open [ResIOT](https://www.resiot.io/en/sign-up-free/)'s webpage to sign-up using  you e-mail. 

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1579342487\/24750\/bxeu75yr9gy4h0eqthpw.png",
        "mode": "responsive",
        "width": 1547,
        "height": 908,
        "caption": "**Figure 1**: ResIOT Sign-up Page"
    }
}]$

- After clicking the "**Sign up free**" button, a new window shows up in which you will fill in the necessary information to complete your registration. Afterwhich, click the "**SIGN UP FREE**" button at the bottom of the webpage.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1579343011\/24750\/ablbter8wva2akqgvo25.png",
        "mode": "responsive",
        "width": 753,
        "height": 921,
        "caption": "**Figure 2**: ResIOT Registration Credentials"
    }
}]$

- Once registration is done, a new page will be shown in your screen with you username and a link which will be is your ResIOT application site.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1579344610\/24750\/l9ylcgwqugnxbndenayt.png",
        "mode": "responsive",
        "width": 1293,
        "height": 563,
        "caption": "**Figure 3**: ResIOT Application Site Link"
    }
}]$

- Upon clicking the application site link, you will see the login page:

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1579344785\/24750\/ste0f2wtlzhngunfbpf0.png",
        "mode": "responsive",
        "width": 848,
        "height": 685,
        "caption": "**Figure 4:** ResIOT Application Log-in Page"
    }
}]$

- Upon successful log-in, you shall then be asked to choose your LoRaWAN® Frequency Plan. For this example, choose **EU868 Region**.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1579345176\/24750\/be1hyyxjzxxcsm6dxgob.png",
        "mode": "responsive",
        "width": 1551,
        "height": 944,
        "caption": "**Figure 5:** ResIOT LoRaWAN\u00ae Frequency Plan"
    }
}]$

- We will now then setup your RAK7246G LPWAN Developer Gateway by clicking the "**Step 1: Add Gateway Wizard**".

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1579345370\/24750\/laylicf9ubcboe16d3in.png",
        "mode": "responsive",
        "width": 1115,
        "height": 803,
        "caption": "**Figure 6**: Adding your Gateway in ResIOT"
    }
}]$

- A list of LPWAN Gateways are then shown. Choose the item "**IMST iC880a + Raspberry Pi**". 

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1579345552\/24750\/tv0njd77bfa5yggyckwa.png",
        "mode": "responsive",
        "width": 1284,
        "height": 555,
        "caption": "**Figure 7**: Choosing IMST iC880a + Raspberry Pi for your RAK7246G LPWAN Developer Gateway"
    }
}]$

- Afterwhich, a new page will show up asking you to fill in the necessary credentials. 

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1579345915\/24750\/mye9hginw9avxgi4zaam.png",
        "mode": "responsive",
        "width": 1389,
        "height": 915,
        "caption": "**Figure 8**: Adding Credentials in Gateway Setup"
    }
}]$

1. **Name**: You can fill in any content based on your preference
2. **Mac Address**: This is the Wi-Fi MAC Address of your RAK7246G LPWAN Developer Gateway. You can get the Mac Address by typing "**ifconfig**" command in the terminal you accessed through SSH.
3. **Gateway EUI/ID**: This is the Gateway ID which you can get in the Configuring your Gateway document.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1579346500\/24750\/vq1pslh17m57penkcvbd.png",
        "mode": "responsive",
        "width": 731,
        "height": 501,
        "caption": "**Figure 9**: Getting the Wi-Fi MAC Address of the RAK7246G LPWAN Developer Gateway"
    }
}]$

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1579422868\/24750\/e3jrytfdetgnbiru9gxy.png",
        "mode": "responsive",
        "width": 1605,
        "height": 828,
        "caption": "**Figure 10**: Getting the Gateway ID of the RAK7246G LPWAN Developer Gateway"
    }
}]$

- After getting all the necessary credentials, fill in the data ang click "**Save Config**" button.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1579347018\/24750\/gzdrrbwi7jh7gm6pv6he.png",
        "mode": "responsive",
        "width": 1379,
        "height": 921,
        "caption": "**Figure 11**: Saving the Gateway Configuration for the RAK7246G in ResIOT"
    }
}]$

- Next step is to login back to the RAK7246G LPWAN Developer Gateway and choose "**4 Edit packet-forwarder config**" through SSH.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1579347204\/24750\/e3wgp74mg2dhkod5pfyo.png",
        "mode": "responsive",
        "width": 763,
        "height": 345,
        "caption": "**Figure 12**: Editing the packet-forwarder configuration through SSH"
    }
}]$

- It will then open the "**global_conf.json**" file and edit it to update the LoRaWAN® configuration by modifying the content with the data from the ResIOT website same with the image shown below:

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1579347442\/24750\/ftxcb7coskl5n1utxnwu.png",
        "mode": "responsive",
        "width": 1354,
        "height": 691,
        "caption": "**Figure 13**: ResIOT Data to be inserted in the LoRaWAN\u00ae Configuration"
    }
}]$

- Modify the contents of the Json File with the data from the image shown in the previous step.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1579347639\/24750\/sqeb436ha8uqtebwmcfn.png",
        "mode": "responsive",
        "width": 875,
        "height": 432,
        "caption": "**Figure 14**: The Json Configuration File to be Modified"
    }
}]$

- Click the hotkey "**Ctrl + X**" to stop editing the Json File and Press "**Y**" to save the modifications. 
- If you could see a **Green Check Mark** same with the image shown below, that means that you have successfully connected your RAK7246G LPWAN Developer Gateway with ResIOT. Congratulations!

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1579347904\/24750\/x8cb5ggishduukv6xl5t.png",
        "mode": "responsive",
        "width": 1904,
        "height": 926,
        "caption": "**Figure 15**: ResIOT Connection Successful"
    }
}]$

