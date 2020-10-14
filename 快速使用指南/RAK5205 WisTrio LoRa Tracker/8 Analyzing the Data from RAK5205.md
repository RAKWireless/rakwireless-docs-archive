---
type: page
title: Analyzing the Data from RAK5205
listed: true
slug: analyzing-the-data-from-rak5205
---published

In the previous section, we have successfully sent some raw data from our RAK5205 LoRa Tracker to The Things Network, but the problem is that you can't really see the actual sensor data from the payload. In this section , we will solve that and understand what each payload means.

Let's take this data for example:

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1562337024\/17320\/mdqeafe9ttu8jz4iksap.jpg",
        "mode": "responsive",
        "width": 1177,
        "height": 425,
        "caption": "**Figure 1:** Received Data in TTN"
    }
}]$

- There are 4 columns in the Application Data Section : time, counter, port and the actual payload.

Each port number tells the kind of data sent from your RAK5205 (Figure 1)

1. **GPS** - Port Number: 2
2. **Battery Voltage** - Port Number: 3
3. **LIS3DH Sensor** - Port Number : 4
4. **BME680 Sensor** - Port Number: 5

Now lets analyze each data frame, which is in Hexadecimal Format. We will be using the data in Figure 1 as an example.

We will convert the Hexadecimal Data into Decimal Data using this [converter](https://www.binaryhexconverter.com/hex-to-decimal-converter) in order to be able to understand it.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1562339635\/17320\/xe0ubgrechzzckjbd8xl.png",
        "mode": "responsive",
        "width": 1014,
        "height": 388,
        "caption": "**Figure 2:** Hex to Dec converter"
    }
}]$

### 1. GPS Data

Example Data: 01 88 05 37 A9 10 9D 5B 00 C0 F8 00 16

- "01 88" - **data flag**
- "05 37 A9" - is the **latitude** and it value is 34.1929. 
- "10 9D 5B" - is the **longitude**, and its value is 108.8859
- "00 C0 F8" - is the **altitude** in meters, and its value is 494m.
- "00 16" - is the **NMEA Speed**, and its value is 0.22km/h.

### 2. Battery Voltage

Example Data: 07 02 01 9F

- "07 02" - **data flag**
- "01 9F" - **actual battery voltage** in volts, in this example it is 4.15V.

### 3. LIS3DH Sensor

Example Data: 03 71 FF 00 FF F0 00 50

- "03 71" -  **data flag**
- "FF 00" - **Acceleration X**, the value is -256mg
- "FF F0" - **Acceleration Y**, the value is -16mg
- "00 50" - **Acceleration Z**, the value is 80mg

### 4. BME680 Sensor

Example Data: 02 67 01 30 05 68 21 06 73 25 B4

- "02 67" - **Data flag**
- "01 30" - **Temperature** in Celsius, the value if 30.4°C
- "21" - **Humidity** , the value is 33%
- "06 73" - **Pressure Flag**
- "25 B4" - **Pressure** in hPa, the value is 965.2hPa

