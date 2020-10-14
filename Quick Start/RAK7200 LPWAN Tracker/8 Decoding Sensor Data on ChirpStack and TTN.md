---
type: page
title: Decoding Sensor Data on ChirpStack and TTN
listed: true
slug: analyzing-the-data-from-rak7200
---published

## Analyzing the Data from RAK7200

In the previous section, we have successfully sent some raw data from our RAK7200 LPWAN Tracker to The Things Network, but the problem is that you can't really see the actual sensor data from the payload. In this section , we will solve that and understand what each payload means.

Let's take this for example: 

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1579615416\/20394\/jrd6gnoqaf6eeif4ngky.jpg",
        "mode": "responsive",
        "width": 1013,
        "height": 574,
        "caption": "**Figure 1:** Sample Payload"
    }
}]$

For this example, the payload is : **01 88 05 37 82 10 9D 6A 00 B3 42 08 02 01 66 03 71 00 06 FE 66 03 B1 05 86 FF DD 00 CC 00 04 09 02 CD BA 0A 02 F3 67 0B 02 17 CA**

Now lets analyze each data , which is in Hexadecimal Format. We will be using the data mentioned above as an example. We will convert the Hexadecimal Data into Decimal Data using this [converter ](https://www.rapidtables.com/convert/number/hex-to-decimal.html?x=FF)in order to be able to understand it.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1579615437\/20394\/hp2ugrvyfdqytyrvmi28.jpg",
        "mode": "responsive",
        "width": 374,
        "height": 292,
        "caption": "**Figure 2:** Hex to Decimal Converter"
    }
}]$

### 1. GPS Data

Example Data: **01 88 05 37 82 10 9D 6A 00 B3 42**

| **Parameter** | **Hex Data** | **Decimal Equivalent** | **Multiplier** | **True Value** | 
| ---- | ---- | ---- | ---- | ---- | 
| **Data Flag** | 01 88 |  |  |  | 
| **Latitude** | 05 37 82 | 341890 | 0.0001 ° Signed MSB | 34.189° | 
| **Longitude** | 10 9D 6A | 1088874 | 0.0001 ° Signed MSB | 108.8874° | 
| **Altitude** | 00 B3 42 | 45890 | 0.01 m Signed MSB | 458.9m | 


### 2. Battery Voltage

Example Data: : **08 02 01 66**

| **Parameter** | **Hex Data** | **Decimal Equivalent** | **Multiplier** | **True Value** | 
| ---- | ---- | ---- | ---- | ---- | 
| **Data Flag** | 08 02 |  |  |  | 
| **Battery Voltage** | 01 66 | 358 | 0.01 Signed | 3.58 V | 


### 3. Acceleration Data

Example Data: **03 71 00 06 FE 66 03 B1**

| **Parameter** | **Hex Data** | **Decimal Equivalent** | **Multiplier** | **True Value** | 
| ---- | ---- | ---- | ---- | ---- | 
| **Data Flag** | 03 71 |  |  |  | 
| **Acceleration X** | 00 06 | 6 | 0.001 g Signed MSB | 0.006g | 
| **Acceleration Y** | FE 66 | -410 | 0.001 g Signed MSB | -0.41g | 
| **Acceleration Z** | 03 B1 | 945 | 0.001 g Signed MSB | 0.945g | 


### 4. Gyroscope Data

Example Data: **05 86 FF DD 00 CC 00 04**

| **Parameter** | **Hex Data** | **Decimal Equivalent** | **Multiplier** | **True Value** | 
| ---- | ---- | ---- | ---- | ---- | 
| **Data Flag** | 05 86 |  |  |  | 
| **Gyroscope X** | FF DD | -35 | 0.01 °/s Signed MSB | - 0.35 °/s | 
| **Gyroscope Y** | 00 CC | 204 | 0.01 °/s Signed MSB | 2.04 °/s | 
| **Gyroscope Z** | 00 04 | 4 | 0.01 °/s Signed MSB | 0.04 °/s | 


### 5. Magnetometer Data

Example Data: **09 02 CD BA 0A 02 F3 67 0B 02 17 CA**

| **Parameter** | **Hex Data** | **Decimal Equivalent** | **Multiplier** | **True Value** | 
| ---- | ---- | ---- | ---- | ---- | 
| **Magnetometer X LPP flag** | 09 02 |  |  |  | 
| **Magnetometer X** | CD BA | -12870 | 0.01 Signed | -128.7 μT | 
| **Magnetometer Y LPP flag** | 0A 02 |  |  |  | 
| **Magnetometer Y** | F3 67 | -3225 | 0.01 Signed | -32.25 μT | 
| **Magnetometer Z LPP flag** | 0B 02 |  |  |  | 
| **Magnetometer Z** | 17 CA | 6090 | 0.01 Signed | 60.9 μT | 


## Decoding Sensor Data in TTN

### Input Decoding Function in TTN

**1**. To start with, download the decoding function through this **[link](https://github.com/RAKWireless/RUI_LoRa_node_payload_decoder/blob/master/RUISensorDataDecoder_for_TTN.js)**.

**2**. From your TTN console, go to application page and click the "**Payload Formats**" tab as shown in the image below.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1579615461\/20394\/sldtdovigclybyfohpcb.jpg",
        "mode": "responsive",
        "width": 1116,
        "height": 153,
        "caption": "**Figure 3**: Payload Format at TTN Application Page"
    }
}]$

**3**. Next, select "**Payload Format**" as "**Custom**". Then, from the decoder tab, copy and paste the decoder function from **step 1**.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1579615473\/20394\/f4iojgdt1y7tyjhs00ir.jpg",
        "mode": "responsive",
        "width": 785,
        "height": 622,
        "caption": "**Figure 4**: Inputting the Decoder Function"
    }
}]$

### Testing in Real System in TTN

After gateway and node go online, click the uplink data record from the application data tab to check the decode status. From the image below, we can see the data decoded successfully in TTN.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1579615490\/20394\/wng5840n8huymngaeg2a.jpg",
        "mode": "responsive",
        "width": 1165,
        "height": 890,
        "caption": "**Figure 5**: Uplink Decoded Data"
    }
}]$

## Decoding Sensor Data in ChirpStack

### Input Decoding Function in ChirpStack

**1.** To start with, download the decoding function through this **[link](https://github.com/RAKWireless/RUI_LoRa_node_payload_decoder/blob/master/RUISensorDataDecoder_for_ChirpStack.js)**.

**2.** From to your ChirpStack, go to application page and click the "**APPLICATION CONFIGURATION**" tab as shown in the image below.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1579615504\/20394\/zjrvbx39f2hb1tzsan9a.jpg",
        "mode": "responsive",
        "width": 763,
        "height": 166,
        "caption": "**Figure 6**: Application Configuration Tab"
    }
}]$

**3**. Next, select "**Payload codec**" as "**Custom JavaScript codec functions**". Then, from the decoder tab, copy and paste the decoder function from **step 1**.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1579615522\/20394\/dxyccziqcihhez5ipyvp.jpg",
        "mode": "responsive",
        "width": 916,
        "height": 786,
        "caption": "**Figure 7**: Decoded Function in Chirpstack"
    }
}]$

**4.** Then, click ‘**UPDATE APPLICATION**’ button to save decoding function.

### Testing in Real System in ChirpStack

After gateway and node go online, click the uplink data record from the application data at "**LIVE DEVICE DATA**" tab to check the decode status. From the image below, we can see the data decoded successfully in ChirpStack.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1579615535\/20394\/f46qt62fzsphhwqnbjft.jpg",
        "mode": "responsive",
        "width": 1032,
        "height": 865,
        "caption": "**Figure 8**: Decode Status in ChirpStack"
    }
}]$

