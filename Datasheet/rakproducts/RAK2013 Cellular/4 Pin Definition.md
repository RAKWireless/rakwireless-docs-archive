---
type: page
title: Pin Definition
listed: true
slug: pin-definition-rak2013-cellular
---published

RAK2013 board is composed of four connectors: **J3**, **J15**, **J16** and **J17**.

### J3 – Boot Jumper

- Jumper for BG96/EG91/EG95 USB boot
- J3 open: boot normally.
- J3 shorted: Force the module  to boot from USB port.

### J15 – Raspberry Connector

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1578924362\/17667\/gwqr0zvzhqbyc2qyihux.jpg",
        "mode": "responsive",
        "width": 1725,
        "height": 1375,
        "caption": "**Figure 1**: RAK2013 Raspberry Connector"
    }
}]$

**Click [here](https://trello-attachments.s3.amazonaws.com/5d0661984b710a15f2d77e5a/5dfb7e2933086e6c5d412d2b/f90a74b153c710bcfb0a9b732cb627c6/RAK2013_Cellular_Pi_Hat_Pinout_Diagram_upd1-200.png) for a much clearer image especially the Pin Numbers**

The table below shows the pin connections of the raspberry connector.

| **Pin Number** | **RAK2013** | **Raspberry Definition** | 
| ---- | ---- | ---- | 
| 1 | NC | 3V3 | 
| 2 | CONN_5V0 | 5V | 
| 3 | SDA_to_MikroBus | GPIO2 (SDA1) | 
| 4 | CONN_5V0 | 5V | 
| 5 | SCL_to_MikroBus | GPIO3 (SCL1) | 
| 6 | GND | GND | 
| 7 | PA_SHNT | GPIO4 (GCLK) | 
| 8 | BG96_RX | GPIO14 (TXD0) | 
| 9 | GND | GND | 
| 10 | BG96_TX | GPIO15 (RXD0) | 
| 11 | NC | GPIO17 (GPIO_GEN0) | 
| 12 | BG96_PWRKEY | GPIO18 (GPIO_GEN1) | 
| 13 | RST_ MikroBus | GPIO27 (GPIO_GEN2) | 
| 14 | GND | GND | 
| 15 | BG96_DTR | GPIO22 (GPIO_GEN3) | 
| 16 | Reserved for GPS TX | GPIO23 (GPIO_GEN4) | 
| 17 | NC | 3V3 | 
| 18 | Reserved for GPS RX | GPIO24 (GPIO_GEN5) | 
| 19 | MikroBus_MOSI | GPIO10 (SPI_MOSI) | 
| 20 | GND | GND | 
| 21 | MikroBus _MISO | GPIO9 (SPI_MISO) | 
| 22 | MikroBus _INT | GPIO25 (GPIO_GEN6) | 
| 23 | MikroBus _CLK | GPIO11 (SPI_SCLK) | 
| 24 | NC | GPIO8 (SPI_CE0_N) | 
| 25 | GND | GND | 
| 26 | MikroBus _CS | GPIO7 (SPI_CE1_N) | 
| 27 | ID_SDA | ID_SD | 
| 28 | ID_SCL | ID_SC | 
| 29 | BG96_W_DISABLE | GPIO5 | 
| 30 | GND | GND | 
| 31 | BG96_RESET | GPIO6 | 
| 32 | MikroBus_PWM | GPIO12 | 
| 33 | NC | GPIO13 | 
| 34 | GND | GND | 
| 35 | NC | GPIO19 | 
| 36 | BG96_PSM | GPIO16 | 
| 37 | BG96_AP_ READY | GPIO26 | 
| 38 | BG96_RI | GPIO20 | 
| 39 | GND | GND | 
| 40 | BG96_STATUS | GPIO21 | 


### J16 and J17 – MikroBus Interface

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1587101839\/17667\/jspcgxrhtz13ler2vvwm.jpg",
        "mode": "responsive",
        "width": 4912,
        "height": 2081,
        "caption": "**Figure 2:** MikroBus Interface"
    }
}]$

