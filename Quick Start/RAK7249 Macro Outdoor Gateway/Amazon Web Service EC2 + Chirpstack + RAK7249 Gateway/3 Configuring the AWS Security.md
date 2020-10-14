---
type: page
title: Configuring the AWS Security
listed: true
slug: configuring-the-aws-security
---published

By default, all inbound traffic to an AWS Instance is blocked, only port 22 (SSH) is open. You need to add a set of rules in order for the Gateway and LoRa® Network Server to be able to communicate:

- The Semtech Packet Forwarder needs **UDP port 1700;**
- MQTT Bridge (unsecured) needs **TCP port 1883**;
- MQTT Bridge (secured) needs **TCP port 8883**; 
- Chirpstack Web Ui needs **TCP port 8080**.

**1.**Open the Security Groups tab in the AWS Dashboard:

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1592825212\/22535\/xnld489ed0z1mt3ayww6.png",
        "mode": "responsive",
        "width": 1933,
        "height": 1094,
        "caption": "**Figure 1:** AWS Security Groups"
    }
}]$

2.Select your desired Security Group (Ubuntu Instance). If you have multiple instances you can use the date and time of creation of the group as a guide to which is the one you want. Click the “**Action**” button and from the drop-worn menu select **Edit Inbound Rules**:

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1592825223\/22535\/sucnlrzozw9ojbwhvxe5.png",
        "mode": "responsive",
        "width": 1561,
        "height": 261,
        "caption": "**Figure 2:** Security Group Inbound Rules"
    }
}]$

3.In the opened window, press the “**Add Rule**” button and add all the 4 rules mentioned before.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1592825232\/22535\/tbhqqcgvyayhwn3adoad.png",
        "mode": "responsive",
        "width": 1932,
        "height": 1094,
        "caption": "**Figure 3:** Adding Inbound Rules"
    }
}]$

$plugin[{
    "type": "callout",
    "data": {
        "text": "It is a good practice\nto name them in accordance with what each of them represents.",
        "type": "info",
        "title": "Note:"
    }
}]$

4.Make sure to **Save** with the button in the lower right corner.

5.Finally check if the rules you created are working by entering your instance Public IP address using port 8080 in a browser window. You should see the Login page of the Chirpstack Web UI (for example `3.120.237.38:8080` as in the image below).

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1580136215\/22535\/ql8xb2sfuyeeloxjihf2.jpg",
        "mode": "responsive",
        "width": 1146,
        "height": 575,
        "caption": "**Figure 4:** Chirpstack Login Page"
    }
}]$

$plugin[{
    "type": "callout",
    "data": {
        "text": "The default Username and Password is **admin**. Additionally, there are profiles crated in the RAKwireless Chirpstack installation, so you\ndo not need to make those yourself and you can directly proceed to adding your\nGateway.",
        "type": "info",
        "title": "Note:"
    }
}]$

