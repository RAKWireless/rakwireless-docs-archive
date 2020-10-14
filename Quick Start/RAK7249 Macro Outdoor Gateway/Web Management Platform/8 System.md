---
type: page
title: System
listed: true
slug: system
---published

### 1. System

General system settings can be monitored and adjusted here.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1592554235\/18281\/mzxcit3l2603xsnexwp2.jpg",
        "mode": "responsive",
        "width": 1916,
        "height": 1267,
        "caption": "**Figure 1:** System Tab"
    }
}]$

- **General Settings**: The system time is displayed here. Additionally, you can edit the Host Name and select the Time zone. Another way to get the correct time is to use Timing Synchronization. You can Enable NTP client mode, enable NTP server and provide server candidate URLs.

$plugin[{
    "type": "callout",
    "data": {
        "text": "Time Synchronization tab is displayed in all System sub-menus.",
        "type": "info",
        "title": "Note:"
    }
}]$

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1592554454\/18281\/wm8uw2dyobfi5vgrvcmo.jpg",
        "mode": "responsive",
        "width": 1935,
        "height": 637,
        "caption": "**Figure 2**: System \u2013 General Settings"
    }
}]$

- **Logging**: In case you want to keep a log of system events you can configure how this is done here. You can set the Buffer size, provide the IP Address and port of an External log server, and set the Log Level.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1592554611\/18281\/rpljbt6zwy3bl9kmnnjg.jpg",
        "mode": "responsive",
        "width": 1934,
        "height": 787,
        "caption": "**Figure 3**: System \u2013 Logging"
    }
}]$

- **Language**: By default, this is in Auto (English), however you can choose from several options including German, Spanish, Russian, etc.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1592554681\/18281\/wgujcrf9jmmsbnymab37.jpg",
        "mode": "responsive",
        "width": 1934,
        "height": 521,
        "caption": "**Figure 4**: System \u2013 Language"
    }
}]$

### 2. Administration

This is where you change the administration password of the device.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1592554738\/18281\/qgy3rt5htkk2ehwykzbk.jpg",
        "mode": "responsive",
        "width": 1934,
        "height": 579,
        "caption": "**Figure 5:** Administration Tab"
    }
}]$

### 3. License

This is the status of your license. You can see the Type, Expiration date, Number of Supported Nodes, and the Number of External Gateways Supported. There is a field to ender the License data in case you are upgrading. All Gateways include a free with the parameters as in Figure 24 in the [LoRa Network](/quick-start/rak7249-macro-outdoor-gateway/lora-network#overview) section.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1592555042\/18281\/e6xfymowlnkowexevzqa.jpg",
        "mode": "responsive",
        "width": 1934,
        "height": 935,
        "caption": "**Figure 6**: License Tab"
    }
}]$

### 4. Backup / Flash Firmware

There are a number of actions that this portion of the Firmware allows the user to perform. It is recommended you make regular backups and refresh the firmware when there is a new release in order to assure optimal performance.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1592555125\/18281\/suh3viguoqraa4wy0qav.jpg",
        "mode": "responsive",
        "width": 1934,
        "height": 1013,
        "caption": "**Figure 4:** Backup, reset and firmware update"
    }
}]$

- **Generate archive**: Downloads an archive of the current configuration
- **Perform reset**: Resets the Gateway to the default settings
- **Restore**: You can upload a previously generated archive to restore the configuration settings at the time of its making
- **Flash new firmware**: Update the firmware by flashing a bin file. Use the button to select the location of the new firmware file and the blue button to initiate the flashing process. There is a tick box to toggle the option of keeping the current settings of the gateway

$plugin[{
    "type": "callout",
    "data": {
        "text": "The **Keep Settings** check box is selected by default, as unchecking it will results in having a Gateway with stock settings after the firmware update.",
        "type": "info",
        "title": "Note:"
    }
}]$

### 5. Reboot

Reboots the gateway. All unsaved changes will be discarded. This is not a reset in any way and only power cycles the device. All configuration settings will be left intact.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1592555198\/18281\/ke0fx5q3cms4nirnivs7.jpg",
        "mode": "responsive",
        "width": 1931,
        "height": 760,
        "caption": "**Figure 5:** System reboot"
    }
}]$

### 6. File Browser

 This gives you access to the files in the **root** partition.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1592555224\/18281\/fyru3ur4e78fvmwtxy7m.jpg",
        "mode": "responsive",
        "width": 1936,
        "height": 777,
        "caption": "**Figure 6**: File Browser"
    }
}]$

