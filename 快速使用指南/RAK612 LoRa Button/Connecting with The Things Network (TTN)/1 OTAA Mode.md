---
type: page
title: OTAA Mode
listed: true
slug: otaa-mode
---published

According to **The Things Network, Over-the-Air Activation** (OTAA) is the preferred and most secure way to connect with The Things Network. Thus it is chosen as the default method when registering a device.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1561816598\/17091\/po1kd0m8xjhpajve7l4q.png",
        "mode": "responsive",
        "width": 1788,
        "height": 879,
        "caption": "**Figure 1:** Activation Method - OTAA"
    }
}]$

- Now let's configure our RAK612 LoRa Button to operate in our desired band (EU868 for example) and join via OTAA, by using AT Commands.

$plugin[{
    "type": "callout",
    "data": {
        "text": "Make sure your LoRa Button is still Connected to the RAK Serial Port Tool.",
        "type": "info",
        "title": "Note"
    }
}]$

- Enter the Following AT Command to **set the frequency** to EU868:
`at+band=EU868

`The full list of AT commands can be found in the previous section: [auto$](/rak612-lora-button/configuring-the-lora-button-using-at-commands).

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1561817090\/17091\/tlnci2khmtz9bm68195n.jpg",
        "mode": "responsive",
        "width": 558,
        "height": 707,
        "caption": "**Figure 2:** Set the Frequency to 868Mhz"
    }
}]$

- Set the **Join mode to OTAA**:
`at+set_config=join_mode:1`

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1561817269\/17091\/e8yn5jyc31aocekiyumg.jpg",
        "mode": "responsive",
        "width": 555,
        "height": 703,
        "caption": "**Figure 3:** Set join mode to OTAA"
    }
}]$

- As we have already set the **Device EUI** in the previous section we continue to the next step.
- We set the **Application EUI**. To do this, copy your Application EUI which can be found here:

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1561818617\/17091\/jjnoxvsddap9t10c3pyz.png",
        "mode": "responsive",
        "width": 1788,
        "height": 879,
        "caption": "**Figure 6:** Application EUI in TTN"
    }
}]$

- Then enter the following AT Command:
`at+set_config=app_eui``"YOUR_``APP_EUI"`

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1561819067\/17091\/jwrchq9msalt5qhzrtqc.jpg",
        "mode": "responsive",
        "width": 546,
        "height": 701,
        "caption": "**Figure 7:** Set the Application EUI of your LoRa Button"
    }
}]$

- Next, we will **set the Application Key** which can be found here:

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1561819394\/17091\/sz3jaqqiedy6nxn1d7cj.png",
        "mode": "responsive",
        "width": 1788,
        "height": 879,
        "caption": "**Figure 8:** Application Key in TTN"
    }
}]$

- Enter the following AT Command in the Serial Port Tool:
`at+set_config=app_``key:"YOUR_``APP_KEY"`

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1561819535\/17091\/ifgxtkj0jr6kxiu84ue4.jpg",
        "mode": "responsive",
        "width": 546,
        "height": 699,
        "caption": "**Figure 9:** Set the Application Key"
    }
}]$

- And lastly, you need to initiate the **OTAA** procedure. To do this, use the following AT Command:
`at+join=otaa`

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1561818924\/17091\/m4czmkkipoejqoqsigsm.jpg",
        "mode": "responsive",
        "width": 549,
        "height": 703,
        "caption": "**Figure 10:** Join in OTAA Mode - AT Command"
    }
}]$

- Go to your Devices section on The Things Network and the Status of your Device will be now active! You have now successfully configured your RAK612 LoRa Button! 

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1561819736\/17091\/itpsp7c4vmcba1jmumgc.png",
        "mode": "responsive",
        "width": 1794,
        "height": 863,
        "caption": "**Figure 11:** Online Status in TTN"
    }
}]$

- Now, let's test our LoRa Button and Send some data to TTN. Go to the Data Tab which can be found here:

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1561820394\/17091\/jlbmgzunmgq57itblqfe.png",
        "mode": "responsive",
        "width": 1788,
        "height": 879,
        "caption": null
    }
}]$

- Now Press the Key 1 on your RAK612 LoRa Button:

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1561820506\/17091\/g9kwd9n79od4v3aqsuls.jpg",
        "mode": "responsive",
        "width": 555,
        "height": 699,
        "caption": "**Figure 12:** Testing the LoRa Button in Serial Port Tool"
    }
}]$

- If you check the TTN window you should see the message has been received:

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1561820307\/17091\/uy7dzexfgdalttpksojm.jpg",
        "mode": "responsive",
        "width": 1804,
        "height": 462,
        "caption": "**Figure 13:** Data Sent by the LoRa Button in TTN"
    }
}]$

