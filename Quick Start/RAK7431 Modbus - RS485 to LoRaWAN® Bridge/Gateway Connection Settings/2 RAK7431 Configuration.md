---
type: page
title: RAK7431 Configuration
listed: true
slug: rak7431-configuration
---published

### Connect the RAK7431 to your Network

1.Connect the RAK7431 to a computer using the Micro USB cable.

2.Open the RAK Serial Tool and select the correct COM port. The default baud rate is **115200**. 

3.After selecting, press **Open**. 

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1597133505\/41166\/rdrljzdn2nzzg6lamsf5.jpg",
        "mode": "600",
        "width": 662,
        "height": 848,
        "caption": "**Figure 1**: RAK Serial Tool"
    }
}]$

- To set up the Device EUI, run the command:

$plugin[{
    "type": "code-block",
    "data": {
        "languageBlocks": [
            {
                "code": "AT+DEVEUI=<Device EUI>",
                "language": "none"
            }
        ]
    }
}]$

- To check the Device EUI run:

$plugin[{
    "type": "code-block",
    "data": {
        "languageBlocks": [
            {
                "code": "AT+DEVEUI",
                "language": "none"
            }
        ]
    }
}]$

- To set up the Application EUI run the command:

$plugin[{
    "type": "code-block",
    "data": {
        "languageBlocks": [
            {
                "code": "AT+APPEUI=<application EUI>",
                "language": "none"
            }
        ]
    }
}]$

- To set up the Application Key run the command:

$plugin[{
    "type": "code-block",
    "data": {
        "languageBlocks": [
            {
                "code": "AT+APPKEY=<application Key>",
                "language": "none"
            }
        ]
    }
}]$

- To check the previously configured Application EUI and Key, run the commands:

$plugin[{
    "type": "code-block",
    "data": {
        "languageBlocks": [
            {
                "code": "AT+APPEUI",
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
                "code": "AT+APPKEY",
                "language": "none"
            }
        ]
    }
}]$

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1597133737\/41166\/mkt6iv87pz3bv4ewxxix.jpg",
        "mode": "600",
        "width": 664,
        "height": 850,
        "caption": "**Figure 2**: Configuring the RAK7431"
    }
}]$

### Set the Frequency Region

The node supports the
following Regional Frequencies: 

- EU433
- CN470
- CN470ALI
- RU864
- IN865
- EU868
- US915
- AU915
- KR920
- AS923

For this demonstration, EU868 shall be used. To set the desired regional frequency band use the command:

$plugin[{
    "type": "code-block",
    "data": {
        "languageBlocks": [
            {
                "code": "AT+REGION=EU868",
                "language": "none"
            }
        ]
    }
}]$

$plugin[{
    "type": "callout",
    "data": {
        "text": "The regional frequency settings need to be\nconsistent with the RAK commercial gateway supported band.",
        "type": "info",
        "title": "Note:"
    }
}]$

### Data Serial Port Rate Setting

$plugin[{
    "type": "callout",
    "data": {
        "text": "The baud rate setting needs to be consistent with the baud rate of the sensor, which is **9600**.",
        "type": "info",
        "title": "Note:"
    }
}]$

The AT command for execution is:

$plugin[{
    "type": "code-block",
    "data": {
        "languageBlocks": [
            {
                "code": "AT+BAUDRATE=9600",
                "language": "none"
            }
        ]
    }
}]$

### Operating and Activation Mode Settings

1.Supported operating modes are two: **Class A** and **Class C**. To set the operating mode (Class C in this case), you need to execute the AT command:

$plugin[{
    "type": "code-block",
    "data": {
        "languageBlocks": [
            {
                "code": "AT+CLASS=C",
                "language": "none"
            }
        ]
    }
}]$

$plugin[{
    "type": "callout",
    "data": {
        "text": "The changes take effect as soon as they are made.",
        "type": "info",
        "title": "Note:"
    }
}]$

2.Activation mode supports the following two modes: **ABP** and **OTAA**. To set the activation mode (OTAA in this case), you need to execute the AT command:

$plugin[{
    "type": "code-block",
    "data": {
        "languageBlocks": [
            {
                "code": "AT+JOINMODE=OTAA",
                "language": "none"
            }
        ]
    }
}]$

3.**Restart** is needed for the modification to take effect. To restart the RAK7431, execute the command:

$plugin[{
    "type": "code-block",
    "data": {
        "languageBlocks": [
            {
                "code": "AT+RESTART",
                "language": "none"
            }
        ]
    }
}]$

4.If everything is configured right, after the execution of the restart command this output pops up in the RAK Serial Tool:

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1597134397\/41166\/apsecikxewxibikunsvn.jpg",
        "mode": "600",
        "width": 664,
        "height": 847,
        "caption": "**Figure 3**: RAK7431 Successful Join"
    }
}]$

