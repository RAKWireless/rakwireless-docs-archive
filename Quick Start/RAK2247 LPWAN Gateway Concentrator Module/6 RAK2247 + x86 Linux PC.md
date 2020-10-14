---
type: page
title: RAK2247 + x86 Linux PC
listed: true
slug: rak2247-to-x86-linux-pc-interface
---published

This document explains the basic steps on how to interface the RAK2247 LPWAN Gateway Concentrator Module with a Linux Operating System in a computer.

The following devices are necessary for the interface:

- RAK2247 LPWAN Gateway Concentrator Module
- [mPCIe to USB Board](https://store.rakwireless.com/products/mpcie-to-usb-board)

**1.** Insert the RAK2247 mPCIe board into the USB
carrier board and plugged into a free USB port of your PC. Your Linux PC should recognized it as a USB device.

$plugin[{
    "type": "callout",
    "data": {
        "text": "If you want to connect the **RAK2247 mPCIe board** to the **Linux PC** directly, make sure to have the PERST# signal (Pin 22) pulled down.",
        "type": "info",
        "title": "Note:"
    }
}]$

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1567423814\/19000\/a3tjqlnm7gte2rno9fsp.jpg",
        "mode": "300",
        "width": 480,
        "height": 375,
        "caption": "**Figure 1**: RAK2247 LPWAN Gateway Concentrator Module to a PCIe-to-USB board"
    }
}]$

**2.** Open the command line then enter the command below in order to clone the Github repository that is required for the process to be completed:

$plugin[{
    "type": "code-block",
    "data": {
        "languageBlocks": [
            {
                "code": "git clone https:\/\/github.com\/RAKWireless\/rak_common_for_gateway.git",
                "language": "none"
            }
        ]
    }
}]$

**3.** Get the name of the interface you are using to connect to the internet by typing the command:

$plugin[{
    "type": "code-block",
    "data": {
        "languageBlocks": [
            {
                "code": "ifconfig",
                "language": "none"
            }
        ]
    }
}]$

An example in Figure 2 shows the name of the wireless interface “[**wlx6045bdf0cf64**](**wlx6045bdf0cf64**)”.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1579881728\/19000\/nzthjgmjnu5qwretfoer.jpg",
        "mode": "responsive",
        "width": 750,
        "height": 506,
        "caption": "**Figure 2:** Network Interface Name"
    }
}]$

- Enter the RAK Folder through

$plugin[{
    "type": "code-block",
    "data": {
        "languageBlocks": [
            {
                "code": "cd rak_common_for_gateway\/lora\/rak2247_usb",
                "language": "none"
            }
        ]
    }
}]$

4.Next, you need to insert the name you got in **Step 3** for your interface in the following files:

`rak_common_for_gateway/lora/set_eui.sh`

`rak_common_for_gateway/lora/update_gwid.sh`

- Then, replace the following line:

$plugin[{
    "type": "code-block",
    "data": {
        "languageBlocks": [
            {
                "code": "GATEWAY_EUI_NIC=\u201deth0\u201d",
                "language": "none"
            }
        ]
    }
}]$

- With the line,

$plugin[{
    "type": "code-block",
    "data": {
        "languageBlocks": [
            {
                "code": "GATEWAY_EUI_NIC=\u201dwlx6045bdf0cf64h0\u201d",
                "language": "none"
            }
        ]
    }
}]$

Again, the values are just an example. Remember to do this for all 3 files in step 4.

5.**Add** the following lines of code at the end of “**install.sh**” file: ( In addition to inserting the name of the
interface from the previous step)

$plugin[{
    "type": "code-block",
    "data": {
        "languageBlocks": [
            {
                "code": "cp ..\/set_eui.sh packet_forwarder\/lora_pkt_fwd\/\ncp ..\/update_gwid.sh packet_forwarder\/lora_pkt_fwd\/\ncp ..\/start.sh packet_forwarder\/lora_pkt_fwd\/\nmkdir -p \/opt\/ttn-gateway\/\ncp -rf packet_forwarder \/opt\/ttn-gateway\/",
                "language": "none"
            }
        ]
    }
}]$

$plugin[{
    "type": "callout",
    "data": {
        "text": "If you want packet forwarder to start on boot, you need to\nalso add the lines below:",
        "type": "info",
        "title": "Note:"
    }
}]$

$plugin[{
    "type": "code-block",
    "data": {
        "languageBlocks": [
            {
                "code": "cp ..\/ttn-gateway.service \/lib\/systemd\/system\/\nsystemctl enable ttn-gateway.service",
                "language": "none"
            }
        ]
    }
}]$

6.**Save** “install.sh” file and execute it in order to install:

$plugin[{
    "type": "code-block",
    "data": {
        "languageBlocks": [
            {
                "code": "sudo .\/install.sh",
                "language": "none"
            }
        ]
    }
}]$

7.Wait for the installation to complete. Using the commands below, go and run the newly created process (**lora_pkt_fwd**):

$plugin[{
    "type": "code-block",
    "data": {
        "languageBlocks": [
            {
                "code": "cd \/opt\/ttn-gateway\/packet_forwarder\/lora_pkt_fwd \nsudo .\/lora_pkt_fwd",
                "language": "none"
            }
        ]
    }
}]$

$plugin[{
    "type": "callout",
    "data": {
        "text": "If you added the additional lines in step 5 it will execute every time on boot.",
        "type": "info",
        "title": "Note:"
    }
}]$

8.The regional parameter configurations for all
the supported regions are located in the folder
`</opt/packet_forwarder/lora_pkt_fwd/global_conf>`. In case you need to
adjust the region frequency band for example, do so before running the process
(**EU868 is the default**)

9.Finally, you should now see your Gateway in TTN.

