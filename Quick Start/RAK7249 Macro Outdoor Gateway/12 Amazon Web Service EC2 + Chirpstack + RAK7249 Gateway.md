---
type: page
title: Amazon Web Service EC2 + Chirpstack + RAK7249 Gateway
listed: true
slug: aws-ec2-chirpstack-rak7249-gateway
---published

This document walks through the details on the steps on how to configure the free cloud services of [Amazon](http://aws.amazon.com/) to work with your **RAK7249 Macro Outdoor Gateway**. Follow each and every step discussed in this document to have a fully functional system. If you encounter errors, kindly contact us through the email provided in the Product Overview.

### Creating an Account

For you to enjoy the free cloud services of Amazon, kindly make an account through their [Amazon Web Service](http://aws.amazon.com/) page.

**Considerations**:

- Limited to 750 hours per month for a period of 12 months
- A debit card must be linked to verify your identity in order to use the service.

### Configuring the Instance

1.After you have logged into your account you need to select what instance you are going to be running.

$plugin[{
    "type": "callout",
    "data": {
        "text": "For the purpose of this tutorial we are going to be using \"**EC2**\". Select it in the **AWS Management Console**.",
        "type": "info",
        "title": "Note:"
    }
}]$

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1592817392\/22529\/aewkzzdfxzibdllqyhk3.png",
        "mode": "responsive",
        "width": 1932,
        "height": 1094,
        "caption": "**Figure 1:** AWS Management Console"
    }
}]$

2.In the following screen you can see your running instances, key pairs, security groups, etc. Press the blue “**Launch instance**” button.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1592817452\/22529\/gaamga2lhz8zzi9cvz4y.png",
        "mode": "responsive",
        "width": 1932,
        "height": 1094,
        "caption": "**Figure 2:** Launching an Instance"
    }
}]$

3.The is a ton of choices for the operating system, however we will be using **Ubuntu**. Scroll down and choose **Ubuntu Server 18.04 LTS** (latest at the time of this document). Click the “**Select**” button.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1592817812\/22529\/x83jwk5znemwrgbdqyct.png",
        "mode": "responsive",
        "width": 1933,
        "height": 1094,
        "caption": "**Figure 3:** Selecting the Operating System"
    }
}]$

4.In the next window, you can configure your Instance. However, we will leave it as it is. Just select the _**t2.Micro**_ for the **instance type** as in **Figure 4** and click “**Review and Launch**”.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1592817816\/22529\/uyp0auuld01pznpwnhzz.png",
        "mode": "responsive",
        "width": 1932,
        "height": 1094,
        "caption": "**Figure 4:** Selecting the Instance Type"
    }
}]$

5.Confirm your choice and Launch. Security groups will be edited in the next section so you can go ahead and confirm your choice by pressing the “**Launch**” button as shown in **Figure 5**.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1592817824\/22529\/r5ym7o5stg0mgguwj8lj.png",
        "mode": "responsive",
        "width": 1934,
        "height": 1094,
        "caption": "**Figure 5:** Launching the Instance"
    }
}]$

### Accessing Instance via SSH

In order to have an SSH session to the Instance, we need to create the appropriate access keys. Thus, after Launching you will see the window in the image below:

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1592817829\/22529\/az22dz70vxl0kbok1rju.png",
        "mode": "600",
        "width": 716,
        "height": 516,
        "caption": "**Figure 6**: Key pair creation"
    }
}]$

1.We will choose to "**Create a new key pair**" from the drop-down menu and give it an appropriate name. Finally click the “**Download Key Pair**” button shown in the image below.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1592817863\/22529\/kbp2k1wcvw8pmwaij05i.png",
        "mode": "600",
        "width": 716,
        "height": 533,
        "caption": "**Figure 7:** Creating a new key pair"
    }
}]$

2.After saving the Keys to your chosen location, you can Launch the instance via the blue button "**Launch Instances**".

3.In the image below, you can see the parameters of your instance. Note the fields in the highlighted with the red rectangle. These are you real **URL** and **IP Address** for accessing this instance.

$plugin[{
    "type": "callout",
    "data": {
        "text": "The URL and IP Address shown in the image below are just examples. You will have a different set of information on your setup.",
        "type": "info",
        "title": "Note:"
    }
}]$

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1592817872\/22529\/zjggim1ruvn5dtgqoafq.png",
        "mode": "responsive",
        "width": 1933,
        "height": 1094,
        "caption": "**Figure 8:** Instance Parameters"
    }
}]$

4.In order to have SSH access to the Instance we will use [**PuTTY**](https://www.putty.org/). Download and install it.

5.In the **AWS Instance** page, mark your instance and click “**Connect**”. This will bring the instructions page out. We will follow the procedure as well.

$plugin[{
    "type": "callout",
    "data": {
        "text": "We first need to convert the keys from _.pem_ format to _.ppk_ format as this is what PuTTY is used for. This is done with PuTTYgen, which comes standard with the PuTTY package.",
        "type": "info",
        "title": "Note:"
    }
}]$

6.Run **PuTTYgen** (if you are suing Windows just type it in the start menu after installing PuTTY and you will find it).

7.In the main windows, select the **Type of key to generate** as **RSA** (should be the default choice). In older versions it is named **SSH-2 RSA**.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1592817880\/22529\/lpurczzz9k7xi401p34y.png",
        "mode": "600",
        "width": 650,
        "height": 591,
        "caption": "**Figure 9**: PuTTYgen main window"
    }
}]$

8.Press “**Load**” in order to select the key files generated by AWS (make sure to select **All Files (_._)** from the drop down menu as by default only **.ppk** files are shown

9.After successfully loading the keys, you can save them in **.ppk** with the “**Save private key**” button. Use the same name as the original **.pem** file. The **ppk** extension will be added automatically. PuTTYgen displays a warning about saving the keys without a passphrase. Ignore it an choose **Yes.**

$plugin[{
    "type": "callout",
    "data": {
        "text": "A passphrase on a private key is an extra layer of protection. Even if your private key is discovered, it cannot be used without the passphrase. The downside to using a passphrase is that it makes automation harder because human intervention is needed to log on to an instance, or to copy files to an instance.",
        "type": "info",
        "title": "Note:"
    }
}]$

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1592817888\/22529\/jzmj397yg6hqjfhf3txt.png",
        "mode": "600",
        "width": 650,
        "height": 591,
        "caption": "**Figure10**: PuTTYgen Saving the public key"
    }
}]$

10.As your Private Key is now in the correct format, now you can create an SSH session with PuTTY. Open the client and select SSH

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1592817896\/22529\/huv72usq8aayvrqetute.png",
        "mode": "600",
        "width": 614,
        "height": 555,
        "caption": "**Figure 11**: PuTTY main window"
    }
}]$

11.You need the correct **Host Name**. Take note of the Host  Name syntax provided below together with an example for a better understanding:

$plugin[{
    "type": "code-block",
    "data": {
        "languageBlocks": [
            {
                "code": "user_name@public_dns_name",
                "language": "none"
            }
        ]
    }
}]$

**Example**: 

- **user_name**: ubuntu
- **public_dns_name**: ec2-3-120-237-38.eu-central-1.compute.amazonaws.com
- **Host name**: [ubuntu@ec2-3-120-237-38.eu-central-1.compute.amazonaws.com](mailto:ubuntu@ec2-3-120-237-38.eu-central-1.compute.amazonaws.com)
- To know  more about "**public_dns___name**" , follow the instructions shown in **Figure 12**.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1592820141\/22529\/xup6rpkdxlylk3eqpiza.jpg",
        "mode": "600",
        "width": 751,
        "height": 667,
        "caption": "**Figure 12**: Knowing your Public DNS Name"
    }
}]$

- Afterwhich, fill-in the corresponding Host Name as shown in **Figure 13**.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1592817905\/22529\/xbg70imnc7iukwmorrto.png",
        "mode": "600",
        "width": 614,
        "height": 555,
        "caption": "**Figure 13:** PuTTY main window with Host Name"
    }
}]$

12.Now we need to tell PuTTY to use our keys. In the **Category panel** expand **Connections>SSH>Auth**. Click the “**Browse**” button and look for you **.ppk** file

$plugin[{
    "type": "callout",
    "data": {
        "text": "If you want to save this configuration for future use go back to the **Session** tab and enter a name in the **Saved Session** text box and click **Save**_._",
        "type": "info",
        "title": "Note:"
    }
}]$

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1592817916\/22529\/fgm7fyurf9an1xnpkril.png",
        "mode": "600",
        "width": 614,
        "height": 555,
        "caption": "**Figure 14**: PuTTY SSH Authentication"
    }
}]$

13.Click the “**Open**” button to initiate the session. If this is your first time connecting, PuTTY will ask for confirmation (click **Yes**). You should see the command line window to your instance now.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1592817924\/22529\/tynwviq4y2z3i6cqzh6z.png",
        "mode": "responsive",
        "width": 837,
        "height": 593,
        "caption": "**Figure 15:** PuTTY SSH Command line"
    }
}]$

