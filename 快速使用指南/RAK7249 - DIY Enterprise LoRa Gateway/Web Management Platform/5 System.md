---
type: page
title: System
listed: true
slug: system
---published

## 1. System

This is the place where you configure general device parameters.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1564892756\/18281\/r27s2s2xun4a2qhlxbrk.jpg",
        "mode": "responsive",
        "width": 2116,
        "height": 1180,
        "caption": "**Figure 1.** General system parameters"
    }
}]$

**General Settings**

The system time is displayed here. Additionally you can edit the Host Name and select the Time zone.

Another way to get the correct time is to use Timing Synchronization. You can Enable NTP client mode, enable NTP server and provide server candidate URLs.

Note that the Time Synchronization tab is displayed in all System sub-menus.

**Logging**

In case you want to keep a log of system events you can configure how this is done here:

You can set the Buffer size, provide the IP Address and port of an External log server, and set the Log Level.

**Language**

By default, this is in Auto (English), however you can choose from several options including German, Spanish, Russian, etc.

## 2. Administrator

This is where you change the administration password of the device.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1564892821\/18281\/tomhnk97mudsnxakjuj8.jpg",
        "mode": "responsive",
        "width": 2112,
        "height": 498,
        "caption": "**Figure 2.** Administrator panel"
    }
}]$

## 3. Backup / Flash Firmware

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1564892857\/18281\/wfdlxwssnrzjavwho9l7.jpg",
        "mode": "responsive",
        "width": 2112,
        "height": 948,
        "caption": "**Figure 3.** Backup, reset and firmware update"
    }
}]$

**Generate archive** – downloads an archive of the current configuration

**Perform reset** – resets the Gateway to the default settings

**Restore** – you can upload a previously generated archive to restore the configuration settings at the time of its making

**Flash new firmware** – update the firmware by flashing a _bin_ file. Use the button to select the location of the new firmware file and the blue button to initiate the flashing process. There is a tick box to toggle the option of keeping the current settings of the gateway.

$plugin[{
    "type": "callout",
    "data": {
        "text": "It is selected by default as unchecking it will results in having a gateway with stock settings after the firmware update.",
        "type": "info",
        "title": "Note:"
    }
}]$

## 4. Reboot

Reboots the gateway. All unsaved changes will be discarded. This is not a reset in any way and only power cycles the device. All configuration settings will be left intact.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1564892966\/18281\/wglh87huusifinjp6c2c.jpg",
        "mode": "responsive",
        "width": 2102,
        "height": 384,
        "caption": "**Figure 4.** System reboot"
    }
}]$

