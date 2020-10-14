---
type: page
title: Recommended Circuit
listed: true
slug: recommended-circuit-rak4200-lora-module
---published

### Module Recommended Circuit

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1593677455\/26765\/ldizhxrlo6nadvnd7dbp.jpg",
        "mode": "600",
        "width": 1734,
        "height": 1224,
        "caption": "**Figure 2**: RAK4200 LPWAN Module Recommended Circuit"
    }
}]$

**1. SWD programming Port**

When programming with JLINK tool , it is need to connect 5 pins of 3V3,SWDIO, SWCLK,GND and MCU_NRST. So it is better to leave these 5 pins for SWD
programming.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1593678733\/26765\/dduww145r7d5k5nichcp.jpg",
        "mode": "300",
        "width": 617,
        "height": 601,
        "caption": "**Figure 3**: SWD Programming connection"
    }
}]$

**2. UART port**

There are two UART ports on RAK4200 module. UART2(pin1 and pin2) is used as a
command port and UART1(pin4 and pin5) is used both as a command and an
upgrade port. So it is better to connect UART2 to external MCU and UART1 is used
as a debug or upgrade port.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1593678774\/26765\/fz1itvcxresj5g8jufkc.jpg",
        "mode": "300",
        "width": 659,
        "height": 512,
        "caption": "**Figure 4**: UART Port connection"
    }
}]$

**3. I2C port**

Pin9 and Pin10 are recommended as I2C port. Just pull up with 10K resistance if use
it.

**4. RF port**

There are two types of RF port. One is with Ipex connector and another is PAD type. For Ipex type just connect the antenna to the Ipex connector on the module directly. For PAD type you can design the antenna as Ipex or SMA or Spring type.

**5. SPI port**

The SPI (pin15 ,pin16,pin17) has connected to the SX1276 in the internal of the
module. So it is better not to use these 3 pins and just leave it un-connect on the mainboard.

**6. VDD power in**

It is recommended to add 4 capacitors near the module at the entrance of the power
supply.

- C1 =10uF
- C2=10uF
- C3=100nF
- C4=100nF

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1593678921\/26765\/butfig5xddbojrqikzsf.jpg",
        "mode": "300",
        "width": 644,
        "height": 778,
        "caption": "**Figure 5**: Capacitor filter for the power supply"
    }
}]$

