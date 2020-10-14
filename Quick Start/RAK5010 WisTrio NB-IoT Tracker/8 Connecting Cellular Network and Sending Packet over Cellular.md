---
type: page
title: Connecting Cellular Network and Sending Packet over Cellular
listed: true
slug: connecting-cellular-network-and-sending-packet-over-cellular
---published

In this section, you will learn more on how to connect Cellular Network of your device. 

- To start with,  insert a SIM card into your RAK5010. For this document,  i’ll use a China Mobile SIM card as an example.

As described in the previous section, we learned that there are three ways to configure our RAK5010: through UART, BLE and microUSB. For this section,  I’ll use UART to configure RAK5010 as an example, but surely you can use BLE or microUSB to configure it too.

OK! Let’s start configuring our RAK5010 through UART.

There are two ways to
connect Cellular network and send packet over Cellular: Manual and Automatic.

### 1 . Connecting Cellular Network and Sending Packet over Cellular Manually

- To begin with, send the AT command
“`at+scan=cellular`” to scan Cellular networks:

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1569647275\/20387\/ldd1gtipgjw2rdimcm06.jpg",
        "mode": "300",
        "width": 540,
        "height": 659,
        "caption": "**Figure 1**: Scanning for Cellular Networks"
    }
}]$

- Wait for about 30 seconds, then you will see the following output in the serial port tool:

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1569647300\/20387\/o1yixmjvgqaheaczyyvb.jpg",
        "mode": "300",
        "width": 538,
        "height": 658,
        "caption": "**Figure 2**: Scanned Cellular Network  shown in Serial Port"
    }
}]$

- As you see, RAK5010 has scanned around Cellular network and show them in the serial port tool.

Then, use the AT command `"at+set_config=cellular: (AT+COPS=1,0,"CHINA MOBILE",0)"`to configure the operator information:

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1569647337\/20387\/s397ccuztyjg01v9oe57.jpg",
        "mode": "300",
        "width": 536,
        "height": 654,
        "caption": null
    }
}]$

Now, continue to configure by using
the AT command 

`"at+set_config=cellular: (AT+QICSGP=1,1,"CMCC","","",1)"` and `"at+set_config=cellular:(AT+QIACT=1)"` :

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1569647480\/20387\/viol2m3ggyntrqdrju3l.jpg",
        "mode": "300",
        "width": 534,
        "height": 655,
        "caption": "**Figure 3**: Configuring the Cellular Network"
    }
}]$

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1569647566\/20387\/kbfkkzhigynpqvvserph.jpg",
        "mode": "300",
        "width": 544,
        "height": 652,
        "caption": "**Figure 4**: Configuring the Cellular Network"
    }
}]$

- Then, set the IP address of the server which will receive the packet sending from RAK5010:

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1569647599\/20387\/wfgibirfba6br8wfddeo.jpg",
        "mode": "300",
        "width": 536,
        "height": 655,
        "caption": "**Figure 5**: Configuring the IP Address of the Server"
    }
}]$

$plugin[{
    "type": "callout",
    "data": {
        "text": "This IP address is just\nused for example, and it is my testing server actually. For your configuration, use your own server IP address.",
        "type": "info",
        "title": "Note"
    }
}]$

- OK, we’ve configured RAK5010 correctly.

Next, let’s try sending a
packet manually over Cellular.

- You can use the AT command `“at+send=cellular:XXX”`
to send data over Cellular:

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1569647644\/20387\/qliw07b9ag9om2ytbi6k.jpg",
        "mode": "300",
        "width": 537,
        "height": 655,
        "caption": "**Figure 6**: Sending Data over Cellular"
    }
}]$

- As you can see, the data we send is “**123456**”. 

Now, let’s check it on our receiving server:

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1569647747\/20387\/muvnk5vma57gwns6apo9.jpg",
        "mode": "responsive",
        "width": 882,
        "height": 88,
        "caption": "**Figure 7**: Receive Data shown in the terminal"
    }
}]$

Great! As you see in the **Figure 7**, the server has received the packet successfully, and the data sent is “**123456**” which is same with the one we just sent out.

### 2 . Connect Cellular Network and Send Packet Automatically

We have already discussed the manual process, now, we'll learn about the **automatic** way of connecting and sending data with Cellular Network. First, configure the parameters for the Cellular operator information and the receiving server information as follows (I use China Mobile SIM card and network for example):

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1569647841\/20387\/nmsor2nxqikesbzduzdj.jpg",
        "mode": "300",
        "width": 539,
        "height": 651,
        "caption": "**Figure 8**: Configuring the Cellular Network Parameters"
    }
}]$

- Then, set the interval for sending loop as follow:

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1569647863\/20387\/usvaf8prsuthawdgwv2t.jpg",
        "mode": "300",
        "width": 536,
        "height": 650,
        "caption": "**Figure 9:** Setting the Loop Intervals"
    }
}]$

As you see, this setting means that we open the sending loop and the interval time at 180 seconds. To know more details about the command, refer to the **[previous section](https://doc.rakwireless.com/rak5010-wistrio-nb-iot-tracker/device-at-commands)**.

- Now, restart RAK5010 by
sending the AT command `“at+set_config=device:restart”`:

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1569647930\/20387\/b5oewg5p13m9pvimgcr0.jpg",
        "mode": "300",
        "width": 542,
        "height": 659,
        "caption": "**Figure 10**: Restarting your RAK5010"
    }
}]$

After restarting, RAK5010 will connect the Cellular network which you just set and send packet of sensor’s data automatically in a loop. Every time it sends a packet out, RAK5010 will go to sleep for 180 seconds which you just set, then RAK5010 will wake up and searching GPS, building a new packet, and sending it out.

- You will see a continuously loop as the following picture shows:

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1569647991\/20387\/ijh8cftfzy4x9ybyalvr.jpg",
        "mode": "300",
        "width": 546,
        "height": 655,
        "caption": "**Figure 11**: Continuous Loop seen in The Serial Tool"
    }
}]$

- RAK5010 will send sensor’s data automatically in a loop.

Let’s check the data in the receiving server:

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1569648037\/20387\/urwjby1runkjaijb18re.jpg",
        "mode": "responsive",
        "width": 1423,
        "height": 54,
        "caption": "**Figure 12**: Data Receive in the Server"
    }
}]$

Great! As we see, the server has received the packet which RAK5010 sends out successfully, and they are all sensor’s data in the packet.

