---
type: page
title: Firmware Customizing
listed: false
slug: firmware-customizing
---published

$plugin[{
    "type": "callout",
    "data": {
        "text": "This document is not an in depth tutorial on how to make your own firmware for your device. Instead, this is\njust a guide on how to use the RAK Online Compiler Tool. As of now, you can only access the RAK Online\nCompiler online Through SSH but rest assured we are currently working on a Web Interface for ease of use.",
        "type": "info",
        "title": "Note:"
    }
}]$

### Accessing Online Compiler

In order for you to access the online compiler, follow these steps:

1.Access the forum through this **[link](https://forum.rakwireless.com/t/rak-online-compiler-for-you-to-compile-your-customized-firmware-based-on-rui/662)**. In the comment section, supply the details needed below:

- Name
- E-mail Address
- A picture of **RAK Product / RAK Module** on hand that you want to test.

2.Wait until one of our Customer Support Team contacts you and if your request is approved, all the necessary credentials shall be sent to your attached e-mail address in the request.

3.Once the necessary credentials are received, download and install an **SSH Client** for your specific OS. There are a lot of Free SSH Clients out there for windows and some of them are provided below together with its download links.

- Bitvise - [https://www.bitvise.com/ssh-server](https://www.bitvise.com/ssh-server)
- WinSCP Tool - [https://winscp.net/eng/downloads.php](https://winscp.net/eng/downloads.php)

$plugin[{
    "type": "callout",
    "data": {
        "text": "For this tutorial, we will be using the **WinSCP Tool**.",
        "type": "info",
        "title": "Note:"
    }
}]$

4.Download and open the WinSCP Tool through the link provided in the previous step. You should be welcomed with the same window as shown in the image below.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1580615743\/22171\/oretjbhmoh1cjbf56b3g.jpg",
        "mode": "responsive",
        "width": 1090,
        "height": 678,
        "caption": "**Figure 1**: WinSCP Tool Welcome Window"
    }
}]$

5.Fill in the necessary credentials provided through the email sent by the Customer Support Team as shown in the image below.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1580615805\/22171\/e7a7auwzwm5a6g2hauue.jpg",
        "mode": "responsive",
        "width": 639,
        "height": 436,
        "caption": "**Figure 2**: WinSCP Tool Log-in Window"
    }
}]$

There are three (3) things you need to fill up:

- **Host Name**: the RAK Online Compiler IP Address is **47.112.137.11**
- **User Name**: this is the username that you received from our support team
- **Password**: this is the password that you received from our support team

6.Click “**Login**” and a pop-up window will appear same as in the image below. Just press **Yes** to proceed.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1580615892\/22171\/nxhdvk4ayqdu6dehmsi1.jpg",
        "mode": "responsive",
        "width": 494,
        "height": 364,
        "caption": "**Figure 3**: WinSCP Log-on Confirmation Prompt"
    }
}]$

You will then see the following window:

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1580615950\/22171\/dockyv9wcccaj4nywnig.jpg",
        "mode": "responsive",
        "width": 1092,
        "height": 680,
        "caption": "**Figure 4**: Computer Local Files and WinSCP Online Compiler Files Comparison"
    }
}]$

$plugin[{
    "type": "callout",
    "data": {
        "text": "The Left Hand Side (1) is the local files on your Computer while the Right hand side (2) is the\nRAK Online Compiler where you will upload all of your files.",
        "type": "info",
        "title": "Note:"
    }
}]$

### Uploading your Customized Firmware

By default, you can use our free and open source application codes **[here](https://github.com/RAKWireless/Products_practice_based_on_RUI)**. But if you want to write your own customized application based RUI by calling RUI APIs, you can follow the guide provided [**here**](https://doc.rakwireless.com/developer-tools/developer-tools/-).

1.Download the zip from our Github repository for testing and extract it on your preferred directory in your PC.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1580229525\/22171\/pdvmjpqotke3ptlxpiuh.jpg",
        "mode": "responsive",
        "width": 932,
        "height": 576,
        "caption": "**Figure 5**: Free Firmware Github Repository"
    }
}]$

2.Open the Application folder on the RAK Online Compiler Directory and navigate to the folder of your corresponding device which you chose in the previous step. Select and right click the files of your application source code and Choose **Upload**. Alternatively, you can **Press F5** for Windows OS.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1580616077\/22171\/umgmdjyouq37wcz5nnbu.jpg",
        "mode": "responsive",
        "width": 1086,
        "height": 674,
        "caption": "**Figure 6**: WinSCP Source Code Uploading"
    }
}]$

3.A prompt will appear once you have done the previous step. Make sure to have the uploading path double checked then **Press OK**.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1580229550\/22171\/zdi1esxuxqw3m18za11j.jpg",
        "mode": "responsive",
        "width": 1090,
        "height": 677,
        "caption": "**Figure 7**: WinSCP Source Code Upload Path Confirmation"
    }
}]$

4.Wait until the uploading process succeeds.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1580229559\/22171\/jutohgzxpndmwa66chra.jpg",
        "mode": "responsive",
        "width": 1087,
        "height": 677,
        "caption": "**Figure 8**: Ongoing Uploading Process"
    }
}]$

5.In the GitHub repository, there is a folder named ​**common header**​. Open the folder and there should be a file named ​"**rui.h**"**.**

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1580229569\/22171\/s2lyypjtycnez3z1lykr.jpg",
        "mode": "responsive",
        "width": 1087,
        "height": 677,
        "caption": "**Figure 9:** Accessing RUI file"
    }
}]$

6.Upload the "**rui.h**" to the same folder where you saved your own customized firmware:

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1580229580\/22171\/qyrfxw57xtxlfapmhuug.jpg",
        "mode": "responsive",
        "width": 1088,
        "height": 677,
        "caption": "**Figure 10:** Uploading RUI file"
    }
}]$

### Compiling your Firmware

Now that you have successfully uploaded your Firmware into the RAK Online Compiler Directory, it is now time to compile your firmware.

1.Open PuTTy by navigating through **Menu Bar>Commands>Open in PuTTy**. You could also Press **Ctrl + P** on Windows OS.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1580229592\/22171\/nt4gxgaimtzrpdukp1uf.jpg",
        "mode": "responsive",
        "width": 1090,
        "height": 676,
        "caption": "**Figure 11**: Opening PuTTy in WinSCP"
    }
}]$

2.A PuTTy pop-up window shows. Input your **password** in the credentials sent to your email and **press Enter**.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1580229604\/22171\/pn2wgzs43rdr92sk20ki.jpg",
        "mode": "responsive",
        "width": 673,
        "height": 430,
        "caption": "**Figure 12**: WinSCP PuTTy Log-on Requisite"
    }
}]$

3.You can see there are some information including the supported hardware, and the compilation commands same with the image shown below:

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1580229626\/22171\/fynbtk7cf6f1wceatm4n.jpg",
        "mode": "responsive",
        "width": 528,
        "height": 607,
        "caption": "**Figure 13**: Configuration Commands for Supported Hardware through WinSCP PuTTy"
    }
}]$

You can also check them by entering the following command:

$plugin[{
    "type": "code-block",
    "data": {
        "languageBlocks": [
            {
                "code": "rak_rui_help",
                "language": "none"
            }
        ]
    }
}]$

$plugin[{
    "type": "callout",
    "data": {
        "text": "As of now, compile commands are still limited but we are working on adding more commands as well as more\nsupported hardware in the future.",
        "type": "info",
        "title": "Note:"
    }
}]$

4.On the command line, enter your corresponding compile command for your hardware. For Example:

$plugin[{
    "type": "code-block",
    "data": {
        "languageBlocks": [
            {
                "code": "rak_rui_build 8212-M",
                "language": "none"
            }
        ]
    }
}]$

$plugin[{
    "type": "callout",
    "data": {
        "text": "Use rak_rui_build 8212-M if you are using the pro version of rak8212.",
        "type": "info",
        "title": "Note:"
    }
}]$

5.Wait for a couple of seconds and once done, you will see the following message:

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1580229643\/22171\/qwxildahc5yxltdtqoqh.jpg",
        "mode": "responsive",
        "width": 666,
        "height": 126,
        "caption": "**Figure 14**: WinSCP PuTTy Compiling Request"
    }
}]$

6.Congratulations, you have now successfully compiled the firmware for your device. A confirmation message should be the same with the image shown below:

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1580229653\/22171\/byp7seub2qsjr9p6gaa1.jpg",
        "mode": "responsive",
        "width": 716,
        "height": 88,
        "caption": "**Figure 15.** WinSCP PuTTy Compiling Success Prompt"
    }
}]$

7.Next step is to export the firmware binary file. On the same folder press **Ctrl + R** or **Right click** on the directory and click **Refresh**.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1580229663\/22171\/axpmzfaoi4btpusj8ppm.jpg",
        "mode": "responsive",
        "width": 1088,
        "height": 677,
        "caption": "**Figure 16**: WinSCP Online Compiler Files Updating"
    }
}]$

8.Upon doing the previous step, a folder named “build- …..” should now appear. **Open** the folder and **Download** the binary file into your PC.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1580229674\/22171\/voqzvlmyyfig8quufral.jpg",
        "mode": "responsive",
        "width": 548,
        "height": 172,
        "caption": "**Figure 17**: Compiled Build Downloading"
    }
}]$

9.Lastly, **Flash** your customized firmware by following the steps from [auto$](/rak8212-itracker-pro/device-firmware-setup).

