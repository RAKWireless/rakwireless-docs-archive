---
type: page
title: Gateway Configuration
listed: true
slug: gateway-configuration
---published

### Set-up the Built-in Network Server

1.Sign in to the gateway by following the [Accessing the Web Management](https://doc.rakwireless.com/rak7249-macro-outdoor-gateway/web-management-platform#accessing-the-web-management-platform) section of the RAK7249 Macro Outdoor Gateway documentation.

2.Setup the RAK7249 Macro Outdoor Gateway using its Built-in Network Server by following this [guide](https://doc.rakwireless.com/rak7249-macro-outdoor-gateway/rak7249-build-in-lora-network-server-rak811).

### Adding Application

1.To enter the application
configuration interface click: **LoRa
Network > Application**. Enter a name for the application and click the **Add** button.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1597128554\/41162\/egnvgmin1fsugph15wmz.jpg",
        "mode": "responsive",
        "width": 1919,
        "height": 729,
        "caption": "**Figure 1**: Create Application in the Buil-In Network Server"
    }
}]$

2.Turn
on the **Auto Add LoRa Device** slider. 

3.Generate
**Application EUI** and **Application Key** by pressing the generate icon marked in the image below. 

$plugin[{
    "type": "callout",
    "data": {
        "text": "The description\nis optional.",
        "type": "info",
        "title": "Note:"
    }
}]$

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1597129027\/41162\/jwq0uq2nb2a2ottj9fwa.jpg",
        "mode": "responsive",
        "width": 1910,
        "height": 900,
        "caption": "**Figure 2**: Registering an application"
    }
}]$

4.After which, press **Save & Apply**.

5.You will be returned to the Application page. Select **Edit** on the created application. 

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1597129239\/41162\/wnhqudrv97xkcnfk8bjn.jpg",
        "mode": "responsive",
        "width": 1912,
        "height": 713,
        "caption": "**Figure 3**: Application list"
    }
}]$

6.Enter the **Device EUI** and press **Add**.

$plugin[{
    "type": "callout",
    "data": {
        "text": "The RAK7431 Device EUI can be seen at the label on the back",
        "type": "info",
        "title": "Note:"
    }
}]$

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1597129351\/41162\/dfkduwpxc6va3819pymi.jpg",
        "mode": "responsive",
        "width": 1919,
        "height": 716,
        "caption": "**Figure 4**: Adding the RAK7431"
    }
}]$

7.On the next page, select the settings provided below:

- **LoRaWAN Class**: C
- **Join Mode**: OTAA
- **Description**: Optional

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1597130313\/41162\/qlo7rowq8qzmqwoguafu.jpg",
        "mode": "responsive",
        "width": 2076,
        "height": 873,
        "caption": "**Figure 5**: Adding the RAK7431 to the Built-In Server"
    }
}]$

