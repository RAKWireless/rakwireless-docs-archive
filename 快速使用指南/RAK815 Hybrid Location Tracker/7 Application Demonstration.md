---
type: page
title: Application Demonstration
listed: true
slug: application-demonstration
---published

In this section, you will learn the three different open source application demo of the RAK815 Hybrid Location Tracker. 

### Log Information

After you finish downloading the application, you can view the Log Information through the serial port defined by the firmware. But first, you need to connect Pin3 >> Pin5, Pin4 >> Pin6 on the UART switch Interface. Refer to the Datasheet available [**here**](https://downloads.rakwireless.com/en/LoRa/RAK815/Hardware%20Specification/RAK815%28RAK813%20BreakBoard%29%20Datasheet%20V1.1.pdf). 

$plugin[{
    "type": "callout",
    "data": {
        "text": "The serial program used in this demonstration is CommUart Assistant, although you may use other serial terminals.",
        "type": "info",
        "title": "Note!"
    }
}]$

### Install Serial Port Driver

This device uses USB to serial port chip CP2102, so after the device is connected to
the computer, the driver will usually be installed automatically. If you find that your
computer is not automatically installed, please go to this [**link**](https://www.silabs.com/products/development-tools/software/usb-to-uart-bridge-vcp-drivers) to download the driver.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1561972253\/16608\/vz9jlabxzzlhzxgu5fav.jpg",
        "mode": "responsive",
        "width": 656,
        "height": 102,
        "caption": "Figure 1.  Selecting USB-UART CP2102 Connection"
    }
}]$

### See Log Information

After successfully installing the driver, connect the device to the PC via the Micro
USB connector. Then reset (reset Button is defined as SW3) device will see the following
log information in the serial port.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1561974204\/16608\/ykozypirtuxyoycosxzv.jpg",
        "mode": "responsive",
        "width": 649,
        "height": 563,
        "caption": "Figure 2. CommUart Assistant Serial Terminal"
    }
}]$

## LoRaWAN Demonstration

- Turn on your RAK815 and download the LoRaWAN Demonstration. 
- Navigate to the Bluetooth settings of your mobile phone and check for "RAK815 LoRaWAN Demo". 

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1561974339\/16608\/cw7awroysyn0t0nad03o.jpg",
        "mode": "responsive",
        "width": 901,
        "height": 496,
        "caption": "Figure 3. Bluetooth Radio Status in Mobile Phone"
    }
}]$

- Using your mobile devices, search for "nordic" in Apple Store or Google Play Store and install the nRF Connect App.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1561976673\/16608\/jb3f3n9z7wmkjrxrgx8d.jpg",
        "mode": "responsive",
        "width": 1063,
        "height": 956,
        "caption": "Figure 4. nRF Connect App"
    }
}]$

- Open the app and connect to the device's Bluetooth radio "RAK813
LoRaWAN Demo". Then, click RX Characteristic to
send data.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1561976691\/16608\/zao6kttu4rqkmj9dzs2r.jpg",
        "mode": "responsive",
        "width": 971,
        "height": 893,
        "caption": "Figure 5. Connecting to RAK815 Bluetooth through nRF Connect"
    }
}]$

Type the value 123456 as a sample message and click "send".

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1561979458\/16608\/vjzb3dyvk4rfhsphqa30.jpg",
        "mode": "responsive",
        "width": 948,
        "height": 881,
        "caption": "Figure 6. Sending Message through nRF Connect"
    }
}]$

After sending, you can see the message in the serial port's Log information.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1561976779\/16608\/qxydnlgyrxaf1gyhbmrw.jpg",
        "mode": "responsive",
        "width": 975,
        "height": 847,
        "caption": "Figure 7. Message shown in the Serial Port log Information"
    }
}]$

### Configuring the parameters using the LoRaWAN Demo

The LoRaWAN web server provider selected use for this case is The Things Network (TTN). To know more about setting up your LoRa Gateway device, refer to this **[page](https://www.thethingsnetwork.org/labs/story/rak831-lora-gateway-from-package-to-online).**

After getting OTAA or ABP parameters of LoRa device from TTN, you can write data
into the flash of RAK815 by transmitting data
through Bluetooth. The format of the data you are sending must be as shown below:

`lora_cfg:dev_eui=xxxxxxxxxxxxxxxx&app_eui=xxxxxxxxxxxxxxxx&app_key=xxxxxxxxxxx
xxxxxxxxxxxxxxxxxxxxx&dev_addr=xxxxxxxx&nwkskey=xxxxxxxxxxxxxxxxxxxxxxxxxxxxx
xxx&appskey=xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx`

$plugin[{
    "type": "callout",
    "data": {
        "text": "Because the information is too long, the serial port won't show the details of the configuration.",
        "type": "info",
        "title": "Note"
    }
}]$

After successfully configuring your device parameters, a message will be shown in your serial port saying: "**LoRaWAN parameters configured successfully**".

Then, reset the device. If your LoRa gateway device is ready, RAK815 will send a join request to LoRaWAN network server. You can see the successful information in the terminal. 

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1561976817\/16608\/sruh9mqzslsprlziqxgf.jpg",
        "mode": "responsive",
        "width": 1130,
        "height": 979,
        "caption": "Figure 8. LoRaWAN Parameters Configuration Status"
    }
}]$

You can also see the data sent by the device on the TTN:

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1561976867\/16608\/ikjgyqehmew7fmpj7u8j.jpg",
        "mode": "responsive",
        "width": 1246,
        "height": 707,
        "caption": "Figure 9. LoRaWAN Parameter Settings in TTN"
    }
}]$

## Peripherals Demo

- Download the Peripherals Demo into your RAK815.
- Navigate to the Bluetooth settings of your mobile phone and check for **"RAK815 Peripherals Demo"**. 
- The device's log information serial port will print the device's sensor information every five
seconds.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1561976887\/16608\/quseig6dab5xftwudrtg.jpg",
        "mode": "responsive",
        "width": 892,
        "height": 774,
        "caption": "Figure 10. Device Information Status"
    }
}]$

Similarly with the LoRaWAN Demo, you can also send message through the nRF Connect app you installed. The message can be viewed to our serial terminal as shown in the image below.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1561976908\/16608\/wkvurxwr2xspwgjea2ri.jpg",
        "mode": "responsive",
        "width": 874,
        "height": 762,
        "caption": "Figure 11. Message Received shown in Serial Port"
    }
}]$

If you connect the LCD to the LCD's expansion interface, you can also see the data
for each sensor on the LCD display.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1561976916\/16608\/wxrjzjtojnqjjtg6ckti.jpg",
        "mode": "300",
        "width": 812,
        "height": 589,
        "caption": "Figure 12. Message Status shown in LCD"
    }
}]$

## Scan Demo

- Download the Scan Demo into your RAK815.
- Navigate to the Bluetooth settings of your mobile phone and check for **"RAK815 Scan Demo"**. 
- Same with the previous application, open the nRF Connect app and connect to the Bluetooth named "RAK815 Scan Demo"; configure the device by sending the LoRaWAN parameters. The configuration status can be seen in the serial port as shown in the figure below. 

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1561976952\/16608\/x7qzkjwx8be8krdiv7y6.jpg",
        "mode": "responsive",
        "width": 896,
        "height": 779,
        "caption": "Figure 13. LoRaWAN Parameters Configuration Status"
    }
}]$

- After successfully configuring the parameters, check if your LoRaWAN gateway has been set in advance. Reset the device and a message will be sent to your terminal that the device has successfully joined in OTAA. 

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1561976983\/16608\/rpxs5wdvond0xiivhdwb.jpg",
        "mode": "responsive",
        "width": 917,
        "height": 796,
        "caption": "Figure 14. OTAA Activation Message"
    }
}]$

Next, if you press the first button of the device, see the figure below. The device will
scan the surrounding Bluetooth device for 1s. 

$plugin[{
    "type": "callout",
    "data": {
        "text": "This device can only scan Bluetooth BLE devices.)",
        "type": "info",
        "title": "Note"
    }
}]$

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1561976999\/16608\/m6uuduwrnoqnthrm4ply.jpg",
        "mode": "300",
        "width": 542,
        "height": 850,
        "caption": "Figure 15. Pressing the Button to Scan BLE"
    }
}]$

If the device scans a Bluetooth BLE device, the scanned device information is printed
out from the log information serial port.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1561977028\/16608\/ln24jrhvwtfibdrucgab.jpg",
        "mode": "responsive",
        "width": 970,
        "height": 840,
        "caption": "Figure 16. Scanned BLE Information Status"
    }
}]$

If your device is in a LoRaWAN connection state, at this point your device will send
the Bluetooth BLE device information you scanned to the LoRaWAN server.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1561977040\/16608\/pxr1lb1u7qw6clkkosct.jpg",
        "mode": "responsive",
        "width": 1327,
        "height": 532,
        "caption": "Figure 17. Scanned BLE Device Information shown in TTN"
    }
}]$

In addition, if you connect the LCD to the device LCD expansion interface, you can
view the real-time status of the device on the LCD

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1561977051\/16608\/i39ewe9t1sqxkgdlgcmb.jpg",
        "mode": "300",
        "width": 860,
        "height": 643,
        "caption": "Figure 18. Status Update shown in LCD"
    }
}]$

