---
type: page
title: Interfacing your RAK811 LPWAN Evaluation Board with Arduino Boards
listed: true
slug: interfacing-your-rak811-lora-evaluation-board-with-arduino-boa
---published

In this document, a set of instruction is written in detail on how to interface your RAK811 LPWAN Evaluation Board with [Arduino](https://www.arduino.cc/), which is an open-source electronics platform based on easy-to-use hardware and software.

## Requirements:

- **RAK811 LPWAN Evaluation Board** (v1.1 or v1.2)
- Gateway in range for testing
- Arduino Mega 2560
- External USB-UART TTL Converter
- Jumper wires

## Arduino Library Preparation

Make sure to follow all the steps in this section thoroughly or you will not be able to move on to the next sections. Discussed in here is the installation of the Arduino-RAK811 Library as well as the discussion of the included sample Arduino codes within it. 

### GitHub Repository Downloading

Uploaded in the RAKwireless official Github repository is the Arduino Library needed by this document. Kindly download the library through this [link](https://github.com/RAKWireless/WisNode-Arduino-Library). 

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1580042478\/24967\/vexsae4pqn4x4q4xjb3j.png",
        "mode": "600",
        "width": 1493,
        "height": 675,
        "caption": "**Figure 1**: RAK811 LPWAN Evaluation Board Arduino Library Repository"
    }
}]$

### Adding the Arduino RAK811 Library to Arduino IDE

1.Once the Arduino RAK811 Library zip is done downloading, unzip it and you should see these files in the extracted folder:

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1580043274\/24967\/cd0qcew7qxps6intp4mw.png",
        "mode": "600",
        "width": 1093,
        "height": 635,
        "caption": "**Figure 2**: Items in the Extracted Arduino RAK811 Library Folder"
    }
}]$

2.Locate the Arduino Libraries folder in which the downloaded Arduino-RAK811 Library folder shall be pasted by navigating through `Documents>Arduino>libraries` same as in the image shown below:

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1580044251\/24967\/qbursndkl9i49xm851b9.png",
        "mode": "600",
        "width": 1333,
        "height": 902,
        "caption": "**Figure 3**: Arduino Libraries Folder Path"
    }
}]$

3.**Copy and Paste** the Arduino-RAK811 Library folder into the Arduino Libraries folder navigated in the previous step.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1580044395\/24967\/u9ru5d9zwky5pa46sk5n.png",
        "mode": "600",
        "width": 1333,
        "height": 905,
        "caption": "**Figure 4**: Arduino-RAK811-Library merged to the Arduino Local Libraries folder"
    }
}]$

4.To verify if the Arduino-RAK811 Library has been merged successfuly with the local Arduino libraries folder, open the Arduino IDE and navigating through `File>Examples>Arduino-RAK811-Library.`Shown in the examples that a **JoinNetworkOTAA** sample code is provided proving that the library was successfully merged.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1580045711\/24967\/egvenp8w2m3eykmu5xdm.png",
        "mode": "responsive",
        "width": 1199,
        "height": 905,
        "caption": "**Figure 5**: Examples of codes in the Arduino-RAK811-Library"
    }
}]$

### Hex File Updating

On the Arduino-RAK811-Library contains the available functions, the user can refer to the **RAK811.h** file, which has a detailed note on the use of each function. 

1.Using your preferred text editor, open the **RAK811.h hex file** included in the library. Within the codes are the different functionalities and settings used for Arduino boards. For this example, we will be using Sublime Text Editor.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1580047731\/24967\/rnsjyqg91hbkx4hcuzmc.png",
        "mode": "600",
        "width": 1161,
        "height": 861,
        "caption": "**Figure 6**: Contents of RAK811.h Hex File"
    }
}]$

1. Before compiling any Arduino code for RAK811 LPWAN Evaluation Board, user should also consider the **Serial RX and TX buffer size**  by manually navigating through `C:\Program Files (x86)\Arduino\hardware\arduino\avr\cores\arduino` and open the **HardwareSerial.h** hex file. 

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1580048039\/24967\/j3ccynesxgzp7oekcpsv.png",
        "mode": "600",
        "width": 1406,
        "height": 907,
        "caption": "**Figure 7**: Editing the HardwareSerial.h Hex file for RX and TX Buffer Size"
    }
}]$

$plugin[{
    "type": "callout",
    "data": {
        "text": "Depending on the RAM size of the Arduino Board you are using, the RX and TX buffer size are recommended to be bigger.",
        "type": "info",
        "title": "Note:"
    }
}]$

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1580048276\/24967\/buvmu1yh5joquqpp3otc.png",
        "mode": "600",
        "width": 1160,
        "height": 862,
        "caption": "**Figure 8**: Recommended RX and TX Buffer Size"
    }
}]$

