---
type: page
title: OTAA Mode
listed: true
slug: chirpstack-otaa-mode
---published

1.To join ChirpStack in OTAA mode, select “**DeviceProfile_OTAA**”.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1580632727\/24877\/kawrl7csak1rbgnaiz1z.png",
        "mode": "responsive",
        "width": 1912,
        "height": 1093,
        "caption": "**Figure 1:** Selecting OTAA Activation Mode in ChirpStack"
    }
}]$

2.Press “**CREATE DEVICE**” button. You may write the application key by yourself or generate it automatically by clicking the icon highlighted in the image.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1580632744\/24877\/phw8fn5ram1ubek2lvy8.png",
        "mode": "responsive",
        "width": 1934,
        "height": 1094,
        "caption": "**Figure 2:** Application Key Generation"
    }
}]$

3.Click "**SET DEVICE KEYS**” button. Now, you’ve completed the configuration on ChirpStack.

- The Device EUI which was set in the previous section to your RAK7200 LPWAN Tracker as "dev_eui" is the same in the image highlighted below

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1580632782\/24877\/alsltdv3wmn3p36miqza.png",
        "mode": "responsive",
        "width": 1934,
        "height": 1094,
        "caption": "**Figure 3:** Device EUI Code"
    }
}]$

- Same with the Application Key, which was set in the previous section as "app_key" is the same with the image highlighted

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1580632822\/24877\/co3zrd6p0w04agsyl5jw.png",
        "mode": "responsive",
        "width": 1934,
        "height": 1094,
        "caption": "**Figure 4:** Application Key LoRaWAN\u00ae"
    }
}]$

$plugin[{
    "type": "callout",
    "data": {
        "text": "The Application EUI which will be set into RAK7200 LPWAN Tracker as \u201c**app_eui**\u201d is not needed for ChirpStack.",
        "type": "info",
        "title": "Note"
    }
}]$

1. Next, let’s **configure** RAK7200 by using **AT commands**. To do this, connect your RAK7200 to a PC, power it on and open **RAK Serial Port Tool** on your computer.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1579614192\/24877\/ah9sepdjjxtslo8od3ia.jpg",
        "mode": "responsive",
        "width": 690,
        "height": 838,
        "caption": "**Figure 5:** RAK Serial Port Tool"
    }
}]$

- Now, let us join our RAK811 using the OTAA activation mode.

5.If the join mode is not in OTAA, just set the LoRa® join mode to **OTAA** and LoRa® class to **Class A** by typing the AT commands shown in the picture below.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1579614208\/24877\/ivwhtrkjbeohwhwjykhl.jpg",
        "mode": "responsive",
        "width": 1356,
        "height": 840,
        "caption": "**Figure 6:** Setting of LoRaWAN\u00ae mode and class"
    }
}]$

6.Type the following AT command to set your respective:**Frequency/Region , Device EUI, Application EUI and Application Key**:

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1579614245\/24877\/p01bw0hgxxgk4rpm5g1z.jpg",
        "mode": "responsive",
        "width": 1356,
        "height": 840,
        "caption": "**Figure 7:** Setting of Frequency and Device EUI"
    }
}]$

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1579614263\/24877\/pphvpa2fnsvazlrsryiz.jpg",
        "mode": "responsive",
        "width": 1356,
        "height": 840,
        "caption": "**Figure 8:** Setting of Application EUI and Key"
    }
}]$

7.Then, **join** in OTAA mode.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1579614277\/24877\/wmzhsi9rjkdkpykwdfyx.jpg",
        "mode": "responsive",
        "width": 692,
        "height": 834,
        "caption": "**Figure 9:** Joining in OTAA"
    }
}]$

- **Joined Successfully!**

8.You can view the "**JoinRequest**" and "**JoinAccept**" on ChirpStack page:

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1580632887\/24877\/ee75imnp4eeilgyx15ju.png",
        "mode": "responsive",
        "width": 1934,
        "height": 1094,
        "caption": "**Figure 10:** Join Request of the Device in the ChirpStack"
    }
}]$

