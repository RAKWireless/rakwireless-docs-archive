---
type: page
title: Schematic Diagram
listed: false
slug: rak5860-schematic-diagram
---draft

The following sections will describe the schematic of the RAK5860 module, which include: 

- Turn on/off module
- WisIO Connector
- Voltage-level translator
- SIM card circuit
- USB Connector
- Status Indication LEDs
- Main Antenna
- GNSS Antenna

### Turn on/off mechanism

Figure 1 shows a circuit to allow turn on or to turn off the module. By default, the internal Quectel BG77 module is in power off mode, it can be turned on by driving WIS_PWRKEY to high state (positive digital pulse) for a period of 500-1000ms. 

Driving WIS_PWRKEY high for 650-1500ms, the module will execute power-down procedure after WIS_PWRKEY is released, then enter off mode.  

Alternatively, the user can send a command **AT+QPOWD** command turn off the internal Quectel BG77 module.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1595477710\/32355\/hhcbjb76nwc1flgmqxog.jpg",
        "mode": "responsive",
        "width": 509,
        "height": 295,
        "caption": "**Figure 1:** Turn On\/Off Module Circuit"
    }
}]$

### WisIO Connector

Figure 2 shows the definition of WisIO connector. 

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1595478713\/32355\/ajnfm4zpvqompwknch8f.jpg",
        "mode": "600",
        "width": 702,
        "height": 764,
        "caption": "**Figure 2:** WisIO Connector Pin Definition"
    }
}]$

The RAK5860 only uses a subset of all the pins available in the WisIO connector. These are shown in the Table below:

| **Name** | **Description** | **Comment** | 
| ---- | ---- | ---- | 
| VBAT | BG77 Power Supply | Max 4.2V | 
| 3v3_S | 3.3V for GNSS Antenna |  | 
| 3V3 | 3.3V For Voltage Level Transistor |  | 
| WIS_PWRKEY | Turn on/off BG77 | Active High | 
| WIS_TX | UART TXD | BG77 MAIN_RX, 1.8V power domain | 
| WIS_RX | UART RXD | BG77 MAIN_TX, 1.8V power domain | 


### WisIO Connector Pin order

Figure
3 shows the WisIO connector’s pin order. The connector is located in the
bottom layer of the RAK5860 module.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1595489725\/32355\/ybqe6nfxcmddcxhq04p8.jpg",
        "mode": "300",
        "width": 859,
        "height": 630,
        "caption": "**Figure 3:** WisIO Connector Pin Order"
    }
}]$

### Voltage-level translator

Within the BG77, all interfaces are designed to work with 1.8V level. RAK5860 features  a voltage-level translator in order to down convert the 3.3V coming from the WisCore module. The Figure 4 shows the design of the internal voltage-level translator.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1595489877\/32355\/iajzywt9xq9yllzhwnns.jpg",
        "mode": "responsive",
        "width": 511,
        "height": 332,
        "caption": "**Figure 4:** 3.3V to 1.8V voltage-level translator"
    }
}]$

When WIS_TX is high (3.3V), the NPN triode is turned off, BG77_RX is pulled high (1.8V)

When WISTX is low (0V), the NPN triode is turned on, BG77 RX is low (0V).

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1595490138\/32355\/sqkb8jzcyawgtpj6nwkw.jpg",
        "mode": "responsive",
        "width": 503,
        "height": 278,
        "caption": "**Figure 5**: 1.8V to 3.3V\nvoltage-level translator"
    }
}]$

When BG77_TX is low (0V), the NPN triode is turned on, WIS_RX is low (0V)

When BG77TX is high (1.8V), the NPN triode is turned off, WIS RX is pulled high (3.3V)

$plugin[{
    "type": "callout",
    "data": {
        "text": "VDD_EXT is 1.8V, from\nBG77 internal regulator, BG77 pin 21",
        "type": "info",
        "title": "Note"
    }
}]$

### SIM card circuit

The RAK5860 module only supports the 1.8V ESIM/SIM card, the following Figure 6 shows SIM interface circuit. by default, we use Nano SIM card, eSIM is no mounting. In order to offer good ESD protection, a TVS diode array is added in the SIM card circuitry

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1595490214\/32355\/al2xtfiv1c9pnyhpcpvz.jpg",
        "mode": "responsive",
        "width": 840,
        "height": 336,
        "caption": "**Figure 6:** SIM Card Circuit"
    }
}]$

### USB Connector

The RAK5860 module provides a Micro-USB connector for connection with a host device. The USB data lines USB+ and USB- are connected directly to the BG77. The VBUS line can be used for USB connection detection. 

In order to offer good ESD protection, a TVS diode array is added in the USB connector circuit.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1595490394\/32355\/e9gbjdetcxega5silqwv.jpg",
        "mode": "responsive",
        "width": 396,
        "height": 311,
        "caption": "**Figure 7:** USB Connector"
    }
}]$

The USB connection detection pin input voltage range is 1.3-1.8V. The Figure 8 shows the USB connection detection pin power supply. 

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1595490517\/32355\/gjqkagfybqm7s3t2as1o.jpg",
        "mode": "responsive",
        "width": 378,
        "height": 241,
        "caption": "**Figure 8:** USB connection detection pin power supply"
    }
}]$

### Power supply for USB PHY circuit

The Figure 9 shows the power supply for USB PHY circuit.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1595490738\/32355\/cbuixbwq2gbavyggu0xb.jpg",
        "mode": "responsive",
        "width": 984,
        "height": 415,
        "caption": "**Figure 9:** Power supply for USB PHY circuit"
    }
}]$

### Status Indication LEDs

Figure 10 shows the operation status and network activity status led circuit, when BG77 is powered on, blue led is lit, different activity network status, the green led is lit or not is different.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1595490860\/32355\/vcmnhvhvv3k2mt9rk1j5.jpg",
        "mode": "responsive",
        "width": 933,
        "height": 534,
        "caption": "**Figure 10:** Status indication LED circuit"
    }
}]$

### Main Antenna

The RAK5860 module’s main antenna has a reserve π-type matching circuit for better RF performance, we use U.FL connector for main antenna.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1595490923\/32355\/nqwbhe0f1mjhgrleldmj.jpg",
        "mode": "responsive",
        "width": 481,
        "height": 291,
        "caption": "**Figure 11:** Main Antenna Circuit"
    }
}]$

### GNNS Antenna

The RAK5860 module is designed with an active antenna, the Figure 12 shows the GNSS antenna circuit. 3V3_S from WisIO connector, we use a U.FL connector for GNSS antenna.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1595490994\/32355\/mmqo6od5g0kztiurpvb3.jpg",
        "mode": "responsive",
        "width": 507,
        "height": 295,
        "caption": "**Figure 12:** GNSS Antenna circuit"
    }
}]$

