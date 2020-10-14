---
type: page
title: System on a Chip (SoCs) and Sensors
listed: true
slug: socs-and-sensors
---published

This section provides detail specifications about the different module present in the RAK5010 device. 

## 1. BG96

### 1.1 Frequency Bands

| **LTE Bands** | **GSM** | **Rx-Diversity** | **GNSS** | 
| ---- | ---- | ---- | ---- | 
| **Cat M1 & NB1:** |  |  |  | 
| LTE-FDD:<br>B1/B2/B3/B4/<br>B5/B8/B12/B13/B18/<br>B19/B20/B26/B28 | GSM850/GSM900 | Not<br> Supported | GPS, GLONASS,<br>BeiDou/<br>Compass, Galileo, QZSS | 


### 1.2 Key Feature of BG96 Module

| **Feature** | **Details** | 
| ---- | ---- | 
| **Power Supply** | Supply Voltage: 3.3V – 4.3V<br>Typical supply<br>voltage: 3.8V | 
| **Transmitting Power** | Class: 3 (23dBm±2dB) for LTE-FDD bands<br>Class: 3 (23dBm±2dB) for LTE-TDD bands<br>Class: 4 (33dBm±2dB) for GSM850<br>Class: 4 (33dBm±2dB) for GSM900<br>Class: 1 (30dBm±2dB) for DCS1800<br>Class: 1 (30dBm±2dB) for PCS1900<br>Class: E2 (27dBm±3dB)<br>for GSM850 8-PSK<br>Class: E2 (27dBm±3dB) for GSM900 8-PSK<br>Class: E2 (26dBm±3dB) for DCS1800 8-PSK<br>Class: E2 (26dBm±3dB)<br>for PCS1900 8-PSK | 
| **LTE Features** | Supports LTE Cat M1 and LTE Cat NB1<br>Supports 1.4MHz RF bandwidth for LTE Cat M1<br>Supports 200KHz RF<br>bandwidth for LTE Cat NB1<br>Supports SISO in the DL direction<br>Cat M1: Max. 300Kbps (DL)/375Kbps (UL)<br>Cat NB1: Max. 32Kbps<br>(DL)/70Kbps (UL) | 
| **GSM Features** | **GPRS:**<br>Supports GPRS multi-slot class 33 (33 by default)<br>Coding scheme: CS-1, CS-2, CS-3, and CS-4<br>Max. 107Kbps (DL), Max. 85.6Kbps (UL)<br>EDGE:<br>Supports Edge multi-slot class 33 (33 by default)<br>Supports GMSK and 8-PSK for different MCS<br>Downlink Coding Schemes: CS 1-4 and MCS 1-9<br>Uplink Coding Schemes: CS 1-4 and MCS 1-9<br>Max. 296Kbps (DL),<br>236.8Kbps (UL) | 


## 2. nRF52840 Module

| **Parameter** | **Detail** | 
| ---- | ---- | 
| CPU | ARM® Cortex®-M4<br>32-bit processor with FPU, 64 MHz | 
| Flash | 1 MB | 
| RAM | 256 KB | 
| BLE Protocol | BLE 5.0 | 
| BLE Tx Power | 8 dBm max | 
| BLE Rx Sensitivity | 95 dBm @ 1 Mbps BLE<br>mode | 
| BLE Data Rate | 2 Mbps, 1 Mbps,<br>500 Kbps,125 Kbps | 
| Current Consumption | 4.8mA in Tx, 4.6mA in<br>Rx and 1.5uA in Sleep Mode | 


### 3. Humidity and Temperature Sensors

The Temperature and Humidity Sensor is an SHTC3 from Sensirion.

### 3.1 Temperature

| **Parameter** | **Conditions** | **Value** | **Units** | 
| ---- | ---- | ---- | ---- | 
| Accuracy | Typ. | ±2.0 | °C | 
| Tolerance | Max | See [Figure 2](/rakproducts/board-overview-rak5010-wistrio-nb-iot-tracker) | °C | 
| Repeatability |  | 0.1 | °C | 
| Resolution |  | 0.01 | °C | 
| Specified Range |  | -40 to +125 | °C | 
| Response Time | τ 63% |  | s | 
| Long-term Drift | Typ. |  | °C/y | 


### 3.2 Humidity

| **Parameter** | **Conditions** | **Value** | **Units** | 
| ---- | ---- | ---- | ---- | 
| Accuracy | Typ. | ±2.0 | %RH | 
| Tolerance | Max. | See [Figure 2](/rakproducts/board-overview-rak5010-wistrio-nb-iot-tracker) | %RH | 
| Repeatability |  | 0.1 | %RH | 
| Resolution |  | 0.01 | %RH | 
| Hysteresis |  | ±1 | %RH | 
| Specified Range | extended | 0 to 100 | %RH | 
| Response Time | τ 63% | 8 | s | 
| Long-term Drift | Typ. |  | %RH/y | 


## 4. Pressure Sensor

The Pressure Sensor is an LPS22HB from ST:

| **Symbol** | **Parameter** | **Test Condition** | **Min.** | **Typ.** | **Max.** | **Unit** | 
| ---- | ---- | ---- | ---- | ---- | ---- | ---- | 
| PTop | Operating Temperature<br>Range |  | -40 |  | +85 | °C | 
| PTfull | Full Accuracy<br>Temperature Range |  | 0 |  | +65 | °C | 
| Pop | Operating Pressure<br>Range |  | 260 |  | 1260 | hPa | 
| Pbits | Pressure Output Data |  |  | 24 |  | bitsbits | 
| Psens | Pressure Sensitivity |  |  | 4096 |  | LSB/hPa | 
| PAccRel | Relative Accuracy<br>over Pressure | P = 800 – 1100 hPa T = 25 °C |  | ±0.1 |  | hPa | 
| PAccT | Absolute Accuracy<br><br>over Temperature | **After OPC**<br>Pop = 0 to 65 °C<br><br>**No OPC**<br>Pop = 0 to 65 °C |  | ±0.1<br><br>±1 |  | hPa | 
| Pnoise | RMS Pressure Sensing<br>Noise | with embedded<br>filtering |  | 0.0075 |  | hPa<br> RMS | 
| ODRPres | Pressure Output Data<br>Rate |  |  | 1/10/25/50/75 |  | Hz | 


## 5. 3-Axis Motion Sensor

| **Symbol** | **Parameter** | **Test Condition** | **Min.** | **Typ.** | **Max.** | **Unit** | 
| ---- | ---- | ---- | ---- | ---- | ---- | ---- | 
| FS | Measurement Range | FS bit set to 00<br>FS bit set to 01<br>FS bit set to 10<br>FS bit set to 11 |  | ±2.0<br>±4.0<br>±8.0<br>±16.0 |  | g | 
| So | Sensitivity | FS bit set to 00; <br>High-resolution mode<br><br>FS bit set to 00; <br>Normal mode<br><br>FS bit set to 00; <br>Low Power mode<br><br>FS bit set to 01;<br> High-resolution mode<br><br>FS bit set to 01;<br> Normal mode<br><br>FS bit set to 01;<br> Low-power mode<br><br>FS bit set to 10;<br> High-resolution mode<br><br>FS bit set to 10;<br> Normal mode<br><br>FS bit set to 10;<br> Low-power mode<br><br>FS bit set to 11;<br> High-resolution mode<br><br>FS bit set to 11;<br> Normal mode<br><br>FS bit set to 11;<br> Low-power mode |  | 1<br><br>4<br><br>16<br><br>2<br><br>8<br><br>32<br><br>4<br><br>16<br><br>64<br><br>12<br><br>48<br><br>192 |  | mg/digit | 


## 6. Ambient Light Sensor

The Ambient Light Sensor is an OPT3001 from TI:

| **Parameter** | **Test Condition** | **Min.** | **Typ.** | **Max.** | **Unit** | 
| ---- | ---- | ---- | ---- | ---- | ---- | 
| Peak irradiance spectral responsibility |  |  | 550 |  | nm | 
| Resolution (LSB) | Lowest full-scale<br>range, RN[3:0] = 0000b |  | 0.01 |  | lux | 
| Full-scale<br>illuminance |  |  | 83865.6 |  |  | 
| Measurement output<br>result | 0.64 lux per ADC<br>code, 2620.90 lux full-scale (RN[3:0] = 0110) , 2000 lux input | 2812<br>1800 | 3125<br>2000 | 3437<br>2200 | ADC <br>lux | 
| Relative accuracy<br>between gain ranges |  |  | 0.2% |  |  | 
| Infrared response<br>(850 nm) |  |  | 0.2% |  |  | 
| Light source<br>variation (incandescent, halogen, fluorescent) | Bare device, no cover<br>glass |  | 4% |  |  | 
| Linearity | Input luminance ><br>40 lux<br>Input luminance <<br>40 lux |  | 2% |  |  | 
| Measured drift across<br>temperature | Input luminance =<br>2000 lux |  | 5% |  | %/ °C | 
| Dark condition, ADC<br>output | 0.01 lux per ADC code |  | 0<br>0 | 3<br>0.03 | lux | 
| Half-power angle | 50% of full-power<br>reading |  | 47 |  | degrees | 


