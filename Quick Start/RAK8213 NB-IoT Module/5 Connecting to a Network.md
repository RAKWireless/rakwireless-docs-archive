---
type: page
title: Connecting to a Network
listed: true
slug: connecting-to-a-network
---published

As you now have direct access to the Raspberry and its console you can proceed to configuring it to connect to a network, rather act as an AP for other devices.

Instructions and examples are provided in the following sections.

### Connect through Wi-Fi (Raspberry Pi built-in)

Now that you are logged into the Raspberry, you can proceed to accessing the configuration tool that comes with the RAKwireless firmware. To do so, execute the following steps:

1.Enter the following command and select option **1 Configure WIFI.**

$plugin[{
    "type": "code-block",
    "data": {
        "languageBlocks": [
            {
                "code": "sudo qmi-config",
                "language": "none"
            }
        ]
    }
}]$

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1593063675\/31137\/zmgwfphqedcqu3mgzo5p.png",
        "mode": "full",
        "width": 1348,
        "height": 735,
        "caption": "**Figure 1**: Main configuration menu"
    }
}]$

2.Select Option **2 Enable Client Mode/Disable AP Mode** and click **OK**. This will let you use the device as a Wi-Fi client rather than AP so you can connect to a network.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1593074411\/31137\/t2gpubcids97kswvcpeq.png",
        "mode": "full",
        "width": 1308,
        "height": 647,
        "caption": "**Figure 2**: Wi-Fi Configuration Options"
    }
}]$

As shown in figure 2, there are five (5) different Wi-Fi configuration options you can choose from. 

1. **Enable AP Mode/Disable Client Mode** - the gateway will work in Wi-Fi Access Point Mode after rebooting while the Wi-Fi Client Mode will be disabled (this is the default mode).
2. **Enable Client Mode/Disable AP Mode** - the gateway will work in Wi-Fi Client mode after rebooting, while Wi-FI AP Mode will be disabled.
3. **Modify SSID and pwd for AP Mode** - used to modify the SSID and password of the Wi-Fi AP. Only works if the Wi-Fi AP Mode is enabled.
4. **Add New SSID for Client** - this is used if you want to connect to a new Wi-Fi Network. Only works in Wi-Fi Client mode.
5. **Change Wi-Fi Country** - this is used to modify the Resident Country to match with Wi-Fi standards.

$plugin[{
    "type": "callout",
    "data": {
        "text": "To enable the Wi-Fi Client Mode, you have to disable first the AP Mode.",
        "type": "warning",
        "title": "Warning"
    }
}]$

3.A window will pop-up, and then **click OK**.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1593074402\/31137\/wtrzkkvrohvigqmormj8.png",
        "mode": "full",
        "width": 1319,
        "height": 592,
        "caption": "**Figure 3**: Client mode enabled"
    }
}]$

4.Once Wi-Fi AP Mode is enabled, you will automatically return to the main configuration menu (figure 1). Select option **1 Configure WIFI** then choose option **4 Add New SSID for Client.**

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1593071991\/31137\/fecj5fwmlbhm9xhkidzv.png",
        "mode": "full",
        "width": 1297,
        "height": 649,
        "caption": "**Figure 4**: Wi-Fi Settings"
    }
}]$

5.**Enter the SSID** of the network you want to connect to then click OK.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1593072024\/31137\/redo7btntgqg8knv34hz.png",
        "mode": "full",
        "width": 1164,
        "height": 537,
        "caption": "**Figure 5**: Wi-Fi SSID"
    }
}]$

6.Enter also the password then click **OK**. Just leave it empty if it has none.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1593072032\/31137\/cvxrg6bmkxtll3qsluq9.png",
        "mode": "full",
        "width": 1164,
        "height": 537,
        "caption": "**Figure 6**: Wi-Fi Passphrase"
    }
}]$

7.**Quit the setup**. Click the quit button at the lower right corner.

8.Then, **reboot your device**. Use the following command so the changes take effect.

$plugin[{
    "type": "code-block",
    "data": {
        "languageBlocks": [
            {
                "code": "sudo reboot",
                "language": "none"
            }
        ]
    }
}]$

### Connect through Cellular (RAK8213 + Hologram SIM)

Before connecting to a cellular network, you should have a SIM card first. After that, you need to configure the BG96 to connect it to the provider. This requires connecting to the BG96 via the USB interface and sending over a few AT commands to set the right values for several parameters.

For this example, you are going to use a Hologram SIM and configure the BG96 with **minicom**. 

1.To start with, execute the following command:

$plugin[{
    "type": "code-block",
    "data": {
        "languageBlocks": [
            {
                "code": "sudo minicom -D \/dev\/ttyUSB3",
                "language": "none"
            }
        ]
    }
}]$

This will start minicom, a Linux tool that allows serial communication. In this case, the minicom allows the serial communication with the USB interface that the BG96 is connected to.

2.Make sure to turn the local Echo so you can input the command with the **Ctrl+A**, followed by **pressing Z** to get to the **Command summary**.

3.**Press E** to turn local echo on/off.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1593067361\/31137\/xowacppstzvf2houzidj.jpg",
        "mode": "600",
        "width": 838,
        "height": 420,
        "caption": "**Figure 7**: Minicom Command Summary"
    }
}]$

The following code block is a summary of the commands you need to execute in the same order. Each code is discussed and an example output is provided at the end of this section.

$plugin[{
    "type": "code-block",
    "data": {
        "languageBlocks": [
            {
                "code": "AT+CPIN? \/\/ Checks the SIM card status.\nAT+QCFG=\"nwscanmode\",1,1 \/\/ Chooses only GSM (disables LTE).\nAT+COPS=? \/\/ Lists the available network providers.\nAT+COPS=1,2,\"28403\",0 \/\/ Forces the connection to Vivacom BG.\nAT+COPS? \/\/ Queries the connected web server information.\nAT+QICSGP=1,1,\"hologram\",\"\",\"\",1 \/\/ Configures PDP context by adding the APN keys.\nAT+QIACT=1 \/\/ Activates the APN network\nAT+QIOPEN=1,0,\"TCP\",\"cloudsocket.hologram.io\",9999,0,1\nAT+QISEND=0,50 \/\/ Sends data, data length is 50.\n{\"k\":\"YOUR_DEVICE_KEY_HERE\",\"d\":\"RAKwireless!\",\"t\":\"_TOPIC1_\"} \/\/ Sends\nAT+QISEND=0,0 \/\/ Query data is sent successfully.",
                "language": "none"
            }
        ]
    }
}]$

**AT+CPIN?**

Checks if the SIM card has a PIN code. In the case of the Hologram SIM, there shouldn’t be one, however, it is good practice to check. If there is no PIN, the output is as follows:

$plugin[{
    "type": "code-block",
    "data": {
        "languageBlocks": [
            {
                "code": "+CPIN: READY",
                "language": "none"
            }
        ]
    }
}]$

**AT+QCFG="nwscanmode",1,1**

Gives you options on what technology to use when scanning for networks. You can use GSM, LTE, or both as the BG96 has them supported. For this guide, GSM is selected as the local providers have no NB-IoT support anyways, plus selecting only one option dramatically speeds up the next step. The response should be as follows:

$plugin[{
    "type": "code-block",
    "data": {
        "languageBlocks": [
            {
                "code": "OK",
                "language": "none"
            }
        ]
    }
}]$

**AT+COPS=?**

Lists all the available network providers in your area. By default, it automatically picks one network provider, but, you are going to make a manual choice. The response the command returns for the region the tutorial produced is as follows:

$plugin[{
    "type": "code-block",
    "data": {
        "languageBlocks": [
            {
                "code": "+COPS: (1,\"Vivacom BG\",\"Vivacom\",\"28403\",0),(1,\"Telenor BG\",\"Telenor\",\"28405\",0) \nOK",
                "language": "none"
            }
        ]
    }
}]$

As shown above, there are 2 operators available: **Vivacom BG** and **Telenor**. Now that this information is present, it can be used for the next command. 

**AT+COPS=1,2,"28403",0**

Selects the network with the numeric identificatory of 28403 (easier to enter than a name). The parameters are as follows:

- **1** - for Manual selection
- **2** - for numeric GSM area location identification number 
- **28403** - for the identification number of Vivacom BG 
- **0** - for GSM area access technology

If there are no errors, the output is as follows:

$plugin[{
    "type": "code-block",
    "data": {
        "languageBlocks": [
            {
                "code": "OK",
                "language": "none"
            }
        ]
    }
}]$

**AT+COPS?**

Checks the network status. If the changes took effect, it should reflect the information you entered in the previous command.

$plugin[{
    "type": "code-block",
    "data": {
        "languageBlocks": [
            {
                "code": "+COPS: 1,2,\"28403\",0 \nOK",
                "language": "none"
            }
        ]
    }
}]$

**AT+QICSGP=1,1,"hologram","","",1**

Sets the AP (access Point). The parameters are as follows:

- **1** - context ID
- **2** - for IPv4
- **"hologram"** - access point name (particular for this example only)
- **""** - user name, empty as there isn’t one.
- **""** - password, empty as there isn’t one.
- **1** - authentication method PAP.

If there are no errors the output is as follows:

$plugin[{
    "type": "code-block",
    "data": {
        "languageBlocks": [
            {
                "code": "OK",
                "language": "none"
            }
        ]
    }
}]$

**AT+QIACT=1**

Confirms and activates the APN network. Expected output is as follows:

$plugin[{
    "type": "code-block",
    "data": {
        "languageBlocks": [
            {
                "code": "OK",
                "language": "none"
            }
        ]
    }
}]$

**AT+QIOPEN=1,0,"TCP","cloudsocket.hologram.io",9999,0,1**

Opens a TCP session to the hologram servers so you can send your data. The most relevant parameters are the three (3) listed below, which you need to change if you use a provider other than Hologram:

- **"TCP"** - type of protocol 
- **"cloudsocket.hologram.io"** host
- **"9999"** port

If there are no errors, the output should be as follows:

$plugin[{
    "type": "code-block",
    "data": {
        "languageBlocks": [
            {
                "code": "OK \n+QIOPEN: 0,0",
                "language": "none"
            }
        ]
    }
}]$

**AT+QISEND=0,50**

In this command, the message is to be sent. In this example, the message has a length of 50 bytes. After the command is executed, you are left with a prompt to enter your message:

$plugin[{
    "type": "code-block",
    "data": {
        "languageBlocks": [
            {
                "code": ">",
                "language": "none"
            }
        ]
    }
}]$

 You need to adhere to a [Hologram specific format](https://www.hologram.io/references/embedded-apis#send-a-message-to-the-hologram-cloud), in short it is as follows:

$plugin[{
    "type": "code-block",
    "data": {
        "languageBlocks": [
            {
                "code": "{\"k\":\"YOUR_DEVICE_KEY_HERE\",\"d\":\"RAKwireless!\",\"t\":\"_TOPIC1_\"}",
                "language": "none"
            }
        ]
    }
}]$

- **" k"** - a string of 8 character is used as **Device Key** for authentication.
- **"d"** - a string of data that is the **Message Payload.**
- **"t"** - a string or an array of strings with message tags to be used as **Message Topics**.

You will need a **Device Key** that ties to your **Hologram SIM**_(this tutorial assumes you have already registered and activated your Hologram SIM)_. To create one, execute the following steps:

1.Open the Hologram Dashboard.

2.Go to the **Webhooks** section.

3.Under **Data Engine**, press the **Show Device Key** button.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1593144274\/31137\/lo8vefxxzwjpckjcwk2h.png",
        "mode": "responsive",
        "width": 1222,
        "height": 598,
        "caption": "**Figure 8**: Hologram Dashboard Webhooks"
    }
}]$

4.In the **Router credentials** window, click the **Generate New Device Key** button to generate a key. Then, click the **Copy Key** button.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1593144294\/31137\/vobw6iohmgbafxkz2txk.png",
        "mode": "600",
        "width": 1212,
        "height": 310,
        "caption": "**Figure 9**: Hologram Dashboard Device Key"
    }
}]$

Now that you have your key, you can replace it for the **k** parameter. You can leave the message and the topic as per the example, which leads to the code line to follow if you use the copied key in figure 8.

The end message for this example is as follows:

$plugin[{
    "type": "code-block",
    "data": {
        "languageBlocks": [
            {
                "code": "{\"k\":\"$pU1Yg}.\",\"d\":\"RAKwireless!\",\"t\":\"_TOPIC1_\"}",
                "language": "none"
            }
        ]
    }
}]$

If the message is sent successfully, the response is as follows:

$plugin[{
    "type": "code-block",
    "data": {
        "languageBlocks": [
            {
                "code": "SEND OK",
                "language": "none"
            }
        ]
    }
}]$

### Command Summary

Listed below are the summary of commands with their corresponding outputs:

$plugin[{
    "type": "code-block",
    "data": {
        "languageBlocks": [
            {
                "code": "AT+CPIN? \n+CPIN: READY \nOK \n\nAT+QCFG=\"nwscanmode\",1,1\nOK\n\nAT+COPS=? \n+COPS: (1,\"Vivacom BG\",\"Vivacom\",\"28403\",0),(1,\"Telenor BG\",\"Telenor\",\"28405\",0) \nOK \n\nAT+COPS=1,2,\"28403\",0 \nOK \n\nAT+COPS? \n+COPS: 1,2,\"28403\",0 \nOK \n\nAT+QICSGP=1,1,\"hologram\",\"\",\"\",1 \nOK \n\nAT+QIACT=1 \nOK \n\nAT+QIOPEN=1,0,\"TCP\",\"cloudsocket.hologram.io\",9999,0,1 \nOK \n+QIOPEN: 0,0\n\nAT+QISEND=0,50\n> {\"k\":\"YOUR_DEVICE_KEY_HERE\",\"d\":\"RAKwireless!\",\"t\":\"_TOPIC1_\u201d}\n\nAT+QISEND=0,0",
                "language": "none"
            }
        ]
    }
}]$

