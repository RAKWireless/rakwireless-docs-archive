---
type: page
title: Pin Definition
listed: true
slug: pin-definition-rak8213
---published

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1590735274\/29543\/gty8ntfcns1bviufyzwv.jpg",
        "mode": "responsive",
        "width": 2078,
        "height": 1884,
        "caption": "**Figure 1**: RAK8213 Pin Definition"
    }
}]$

| **Type** | **Description** | 
| ---- | ---- | 
| **IO** | Bidirectional | 
| **DI** | Digital input | 
| **DO** | Digital output | 
| **PI** | Power input | 
| **PO** | Power output | 
| **AI** | Analog input | 
| **AO** | Analog output | 
| **OC** | Open collector | 
| **OD** | Open drain | 
| **NC** | No Connection | 


| **Pin #** | **Mini PCIe PIN Rev. 2.0** | **RAK8213 PIN** | **Type** | **Description** | **Remarks** | 
| ---- | ---- | ---- | ---- | ---- | ---- | 
| 1 | WAKE# | PI_PWRKEY | DI | Turn the module on/off | - 3.3V power domain.<br>- When RAK8213 is in power off mode, it can be turned on to normal mode by driving the PI_PWRKEY pin to a high level (Pressing the Power Button) for at least 500ms.<br>- When RAK8213 is in normal mode, driving the PI_PWRKEY pin to a high level  (Pressing the Power Button) for at least 650ms, the module will execute power-down procedure after the PI_PWRKEY is released. | 
| 2 | 3.3Vaux | 3V3 | PI | 3.3V DC supply |  | 
| 3 | COEX1 | VBUS_CTRL | DO | USB detection control | - 3.3V power domain.<br>- High level: Enable USB detection<br>- Low level: Disable USB detection | 
| 4 | GND | GND | - | Ground |  | 
| 5 | COEX2 | GNSS_PWR_CTRL | DO | Active GNSS antenna power supply control | - 3.3V power domain.<br>- High level: Enable power supply(3.3V)<br>- Low level: Disable power supply | 
| 6 | 1.5V | NC |  | No Connection |  | 
| 7 | CLKREQ# | PI_AP_READY | DI | Application processor sleep state detection | - 3.3V power domain. If unused, keep this pin open. | 
| 8 | UIM_PWR | SIM_VDD_PCIE | PO | Power supply for (U)SIM card | - Either 1.8V or 3.0V is supported by the module automatically.<br>- No Connection by default. Using (U)SIM card connector on board. | 
| 9 | GND | GND |  | Ground |  | 
| 10 | UIM_DATA | SIM_DATA_PCIE | IO | Data signal of (U)SIM card | - No Connection by default. Using (U)SIM card connector on board. | 
| 11 | REFCLK- | PI_UART_TX | DI | UART receive data of RAK8213 | - 3.3V power domain. Connect to BG96’s UART_RX internally. | 
| 12 | UIM_CLK | SIM_CLK_PCIE | DO | Clock signal of (U)SIM card | - No Connection by default. Using (U)SIM card connector on board. | 
| 13 | REFCLK+ | PI_UART_RX | DO | UART transmit data of RAK8213 | - 3.3V power domain. Connect to BG96’s UART_TX internally. | 
| 14 | UIM_RESET | SIM_RST_PCIE | DO | Reset signal of (U)SIM card | - No Connection by default. Using (U)SIM card connector on board. | 
| 15 | GND | GND |  | Ground |  | 
| 16 | UIM_VPP | SIM_PRESENCE_PCIE | DI | (U)SIM card insertion detection | - No Connection by default. Using (U)SIM card connector on board. | 
| 17 | RESERVED | PI_RI | DO | DO | - 3.3V power domain. If unused, keep this pin open. | 
| 18 | GND | GND |  | Ground |  | 
| 19 | RESERVED | NC |  | No Connection |  | 
| 20 | W_DISABLE# | PI_W_DISABLE | DI | Airplane mode control | - 3.3V power domain.<br>- Pull-up by default.<br>- In low voltage level, the module can enter into airplane mode.<br>- If unused, keep this pin open. | 
| 21 | GND | GND |  | Ground |  | 
| 22 | PERST# | PI_RESET | DI | Reset the module | - 3.3V power domain. If unused, keep this pin open. If the Reset Button is pressed the module will reboot. | 
| 23 | PERn0 | PI_CTS | DO | Clear to send | - 3.3V power domain. If unused, keep this pin open. | 
| 24 | 3.3Vaux | 3V3 | PI | 3.3V DC supply |  | 
| 25 | PERp0 | PI_RTS | DI | Request to send | - 3.3V power domain. If unused, keep this pin open. | 
| 26 | GND | GND |  | Ground |  | 
| 27 | GND | GND |  | Ground |  | 
| 28 | 1.5V | PI_PSM | DO | Power saving mode indicator | - 3.3V power domain. If unused, keep this pin open. | 
| 29 | GND | GND |  | Ground |  | 
| 30 | SMB_CLK | BG96_I2C_SCL | OD | I2C serial clock. Used for external codec. | - 1.8V power domain.<br>- Pull-up resistor has been set internally.<br>- No Connection by default. | 
| 31 | PETn0 | PI_DTR | DI | Data terminal ready (sleep mode control) | - 3.3V power domain. If unused, keep this pin open. | 
| 32 | SMB_DATA | BG96_I2C_SDA | OD | I2C serial data. Used for external codec. | - 1.8V power domain.<br>- Pull-up resistor has been set internally.<br>- No Connection by default. | 
| 33 | PETp0 | PI_DCD | DO | Data carrier detection | - 3.3V power domain. If unused, keep this pin open. | 
| 34 | GND | GND |  | Ground |  | 
| 35 | GND | GND |  | Ground |  | 
| 36 | USB_D- | USB- | IO | USB differential data (-) | - Require differential impedance of 90Ω. | 
| 37 | GND | GND |  | Ground |  | 
| 38 | USB_D+ | USB+ | IO | USB differential data (+) | - USB differential data (+) | 
| 39 | 3.3Vaux | 3V3 | PI | 3.3V DC supply |  | 
| 40 | GND | GND |  | Ground |  | 
| 41 | 3.3Vaux | 3V3 | PI | 3.3V DC supply |  | 
| 42 | LED_WWAN# | NETLIGHT_LED | DO | Indicate the module’s network activity status | **Logic Level Changes / _Network Status_**<br><br>- Flicker slowly (200ms Low /1800ms High) / _Network searching_<br>- Flicker slowly (1800ms Low /200ms High) /_Idle_<br>- Flicker quickly (125ms Low /125ms High) / _Data transfer is ongoing_<br>- Always low / _Voice Calling_<br>- 3.3 V power domain. If unused, keep this pin open. | 
| 43 | GND | GND |  | Ground |  | 
| 44 | LED_WLAN# | NC |  | No Connection |  | 
| 45 | RESERVED | BG96_PCM_CLK | DO | PCM clock output | - 1.8V power domain. No Connection by default. | 
| 46 | LED_WPAN# | STATUS_LED | DO | Indicate the module’s operation status. | - 3.3V power domain. <br>- It will output low level when the module is powered on. <br>- If unused, keep this pin open. | 
| 47 | RESERVED | BG96_PCM_OUT | DO | PCM frame synchronization output | - 1.8V power domain. No Connection by default. | 
| 48 | 1.5V | VDD_EXT_1V8 | PO | Provide 1.8V for external circuit<br><br>IOmax=10mA | - Power supply for external GPIO’s pull-up circuits. No Connection by default. | 
| 49 | RESERVED | BG96_PCM_IN | DI | PCM data input | - 1.8V power domain. No Connection by default. | 
| 50 | GND | GND |  | Ground |  | 
| 51 | RESERVED | BG96_PCM_SYNC | DO | PCM data output | - 1.8V power domain. No Connection by default. | 
| 52 | 3.3Vaux | 3V3 | PI | 3.3V DC supply |  | 


