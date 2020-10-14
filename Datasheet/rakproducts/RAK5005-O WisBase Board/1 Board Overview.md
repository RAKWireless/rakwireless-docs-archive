---
type: page
title: Board Overview
listed: false
slug: board-overview-rak5005-o
---draft

### Overview

Figure 1 shows the top view and the interfaces of the RAK5005-O base board and figure 2 shows the bottom of the board.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1594961446\/32152\/jgnyj4soo1xzaesxkk9q.jpg",
        "mode": "600",
        "width": 592,
        "height": 265,
        "caption": "**Figure 1**: Top view of the board with interfaces"
    }
}]$

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1594962459\/32152\/lm6d7pmbpj8t6wiskg0r.jpg",
        "mode": "600",
        "width": 543,
        "height": 325,
        "caption": "**Figure 2**: Bottom view of the board with interfaces"
    }
}]$

As shown in Figure 4 and Figure 5, in the RAK5005-O baseboard, there is 1 slot reserved for WisDuo module，4 slots reserved for WisSensor modules and 1 slot reserved for WisIO module. Additionally, there are also 2.54mm pitch connectors for extension interface, such as I2C, UART, and GPIO pins.

For convenience, there is a USB connector for debugging, it is connected directly to MCU’s USB port (if supported). the customer can access the internal MCU by connecting to a computer’s USB port directly. This USB connector is also used as a battery charging port.

For each module, we design a method to connect and fasten the module easily. These connectors are high-speed board to board connector, they provide signal integrity for each data bus. A set of screws are used for attaching the module under the environment with vibrations.

To avoid electromagnetic interference and heating interference, the sensor connectors on the WisBase are designed to be installed on both sides of the PCB. As shown in Figure 4, and Figure 5, A sensor module can be attached either on the top layer or the bottom layer of the WisBase board.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1594996854\/32152\/vsl8eckzyx4toar2onpz.png",
        "mode": "600",
        "width": 1107,
        "height": 556,
        "caption": "**Figure 3**: Bottom view of the board with interfaces"
    }
}]$

For example, it is recommended to attach a temperature sensor outside of the base board, as shown in the Figure 7. It allows to get more accurate measurements, since temperature sensor located in the top layer of the base board could be interfered by the heating introduced by other modules.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1594996864\/32152\/pwqs7b4bt5hy3l1mc1ps.png",
        "mode": "600",
        "width": 1107,
        "height": 691,
        "caption": "**Figure 4**: Out of the board Temperature Sensor"
    }
}]$

