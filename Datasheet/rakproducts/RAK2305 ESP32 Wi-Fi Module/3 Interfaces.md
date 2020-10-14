---
type: page
title: Interfaces
listed: false
slug: rak2305-interfaces
---draft

### UART Interface

The RAK2305 module provides two UART interfaces: UART0 and UART1.  The UART0 can be used update firmware or to access logs output through WisBlock baseboard USB interface. The UART1 is the main communication interface with WisCPU module.

### SPI Interface

The RAK2305 supports one single SPI Interface. It can be operated either in the master or slave mode, both can be implemented in full duplex or half-duplex communication modes. The SPI interface supports the following features:

- Four SPI transfer modes, which is defined by the polarity (CPOL) and the phase (CPHA) of the SPI clock.
- An internal FIFO buffer of 64-byte.

### I2C Interface

The RAK235 module provides a I2C bus interface. Depending on the user’s configuration, it can serve as I2C master or slave. The I2C interface supports:

- Standard mode (100 Kbit/s) and Fast mode (400 Kbit/s).
- Up to 5MHz, constrained by the SDA pull-up strength.

- 7-bit/10-bit addressing mode

The RAK2305 module allow users to access directly to the  registers to control I2C interfaces, which add more flexibility in the design of the final solution.

### Download Interface

The RAK2305 module uses the UART0 interface to download customized application code into the ESP32’s flash memory. The users can use an USB to UART cable for this purpose. Alternatively, once the RAK2305 is mounted on top of WisBase base board, such as the RAK5005, then users can access to the UART0 interface through the RAK5005’s USB interface instead. The pinout if the USB port of the RAK2305 is shown in the Figure 1.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1595395214\/32332\/zvwcfs66u42vbtcaztkc.jpg",
        "mode": "300",
        "width": 170,
        "height": 150,
        "caption": "**Figure 1:** USB\/UART0 Interface"
    }
}]$

$plugin[{
    "type": "callout",
    "data": {
        "text": "Before Download, you need to pull down IO0.",
        "type": "warning",
        "title": "Warning"
    }
}]$

