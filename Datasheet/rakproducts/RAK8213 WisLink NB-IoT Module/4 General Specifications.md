---
type: page
title: General Specifications
listed: true
slug: general-specifications-rak8213
---published

| **Features** | **Details** | 
| ---- | ---- | 
| Mini PCIe Interface | Using the PCI Express Mini Card 1.2 standard interface | 
| Power Supply | - **Supply voltage**: 3.3V~3.6V<br>- **Typical supply voltage**: 3.3V | 
| Transmitting Power | - Class 3 (23dBm±2dB) for LTE-FDD bands<br>- Class 3 (23dBm±2dB) for LTE-TDD bands<br>- Class 4 (33dBm±2dB) for GSM850<br>- Class 4 (33dBm±2dB) for EGSM900<br>- Class 1 (30dBm±2dB) for DCS1800<br>- Class 1 (30dBm±2dB) for PCS1900<br>- Class E2 (27dBm±3dB) for GSM850 8-PSK<br>- Class E2 (27dBm±3dB) for EGSM900 8-PSK<br>- Class E2 (26dBm±3dB) for DCS1800 8-PSK<br>- Class E2 (26dBm±3dB) for PCS1900 8-PSK | 
| LTE Features | - Support LTE Cat M1 and LTE Cat NB1<br>- Support 1.4MHz RF bandwidth for LTE Cat M1<br>- Support 200KHz RF bandwidth for LTE Cat NB1<br>- Support SISO in DL direction<br>- Cat M1: Max. 375Kbps (DL)/375Kbps (UL)<br>- Cat NB1: Max. 32Kbps (DL)/70Kbps (UL) | 
| GSM Features | **GPRS:**<br><br>- Support GPRS multi-slot class 33 (33 by default)<br>- Coding scheme: CS-1, CS-2, CS-3 and CS-4<br>- Max. 107Kbps (DL)/85.6Kbps (UL)<br><br>**EDGE:**<br><br>- Support EDGE multi-slot class 33 (33 by default)<br>- Support GMSK and 8-PSK for different MCS (Modulation and Coding Scheme)<br>- Downlink coding schemes: CS 1-4 and MCS 1-9<br>- Uplink coding schemes: CS 1-4 and MCS 1-9<br>- Max. 296Kbps (DL)/236.8Kbps (UL) | 
| Internet Protocol Features | - Support **PPP/TCP/UDP/SSL/TLS/FTP(S)/HTTP(S)/NITZ/PING/MQTT** protocols<br>- Support **Password Authentication Protocol** (PAP) and **Challenge Handshake Authentication Protocol** (CHAP) protocols which are usually used for PPP connections | 
| SMS | - Text and PDU mode<br>- Point to point MO and MT<br>- SMS cell broadcast<br>- SMS storage: ME by default | 
| (U)SIM Card Interface | - Support USIM/SIM card: 1.8V, 3.0V | 
| Audio Feature   ** | - Support one digital audio interface: PCM interface | 
| USB Interface | - Compliant with USB 2.0 specification (slave only) and the data transfer rate can reach up to 480Mbps<br>- Used for AT command communication, data transmission, GNSS NMEA output, software debugging and firmware upgrade<br>- Support USB serial drivers for **Windows** 7/8/8.1/10, **Linux** 3.x(3.4 or later)/4.1~4.15, **Android** 4.x/5.x/6.x/7.x/8.x/9.x | 
| UART Interfaces | **UART1:**<br><br>- Used for data transmission and AT command communication;<br>- 115200bps by default;<br>- The default frame format is 8N1 (8 data bits, no parity, 1 stop bit) ;<br>- Support RTS and CTS hardware flow control;<br><br>**UART2:**<br><br>- Used for module debugging and log output;<br>- 115200bps baud rate;<br><br>**UART3:**<br><br>- Used for outputting GNSS data or NMEA sentences; | 
| AT Commands | - 3GPP TS 27.007 and 3GPP TS 27.005 AT commands, as well as Quectel enhanced AT commands | 
| Network Indication | - One NETLIGHT pin for network connectivity status indication | 
| Antenna Interfaces | - Main antenna (ANT_MAIN) and GNSS antenna (ANT_GNSS) interfaces | 
| Physical Characteristics | - **Size**: (51.0±0.15) mm × (30.0±0.15) mm × (4.9±0.2) mm<br>- **Weight**: approx. 128.6 g | 
| Temperature Range | - **Operation temperature range**: -35°C ~ +75°C _(1)_<br>- **Extended temperature range**: -40°C ~ +85°C _(2)_<br>- **Storage temperature range**: -40°C ~ +90°C | 
| Firmware Upgrade | - USB interface, DFOTA | 
| RoHS | - All hardware components are fully compliant with EU RoHS directive | 


$plugin[{
    "type": "callout",
    "data": {
        "text": "** means under development.\n\n_(1)_ Within operation temperature range, the module is 3GPP compliant.\n\n_(2)_ Within extended temperature range, the module remains the ability to establish and maintain a voice, SMS, data transmission, emergency call, etc. There is no unrecoverable malfunction. There are also no effects on radio spectrum and no harm to radio network. Only one or more parameters like Pout might reduce in their value and exceed the specified tolerances. When the temperature returns to the normal operating temperature levels, the module will meet 3GPP specifications again.",
        "type": "info",
        "title": "Note"
    }
}]$

