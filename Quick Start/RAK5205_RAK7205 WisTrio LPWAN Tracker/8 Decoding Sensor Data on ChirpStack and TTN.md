---
type: page
title: Decoding Sensor Data on ChirpStack and TTN
listed: true
slug: analyzing-the-data-from-rak5205
---published

## Analyzing Sensor Data from RAK5205

In the previous section, we have successfully sent some raw data from our RAK5205 LPWAN Tracker to The Things Network, but the problem is that you can't really see the actual sensor data from the payload. In this section , we will solve that and understand what each payload means.

Let's take this data for example:

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1570795475\/17320\/otdvg3shjsksxrm6bbl1.jpg",
        "mode": "responsive",
        "width": 1110,
        "height": 653,
        "caption": "**Figure 1:** Sample Payload"
    }
}]$

For this example, the payload is : **01 88 05 37 97 10 9D 59 00 DC 14 08 02 01 7A 07 68 58 06 73 25 6D 02 67 01 1D 04 02 14 AF 03 71 FF FF FF DD FC 2E**

Now let's analyze each data , which is in Hexadecimal Format. We will be using the data mentioned above as an example. We will convert the Hexadecimal Data into Decimal Data using this [converter](https://www.rapidtables.com/convert/number/hex-to-decimal.html?x=FF) in order to be able to understand it.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1570801620\/17320\/lwg2elvxz58fwgheftzw.jpg",
        "mode": "responsive",
        "width": 360,
        "height": 278,
        "caption": "**Figure 2:** Hexadecimal to Decimal converter"
    }
}]$

### 1. GPS Data

Example Data: **01 88 05 37 97 10 9D 59 00 DC 14**

| **Parameter** | **Hex Data** | **Decimal Equivalent** | **Multiplier** | **True Value** | 
| ---- | ---- | ---- | ---- | ---- | 
| **Data Flag** | 01 88 |  |  |  | 
| **Latitude** | 05 37 97 | 341911 | 0.0001 ° Signed MSB | 34.1911° | 
| **Longitude** | 10 9D 59 | 1088857 | 0.0001 ° Signed MSB | 108.8857° | 
| **Altitude** | 00 DC 14 | 56340 | 0.01 m Signed MSB | 563.4 m | 


### 2. Battery Voltage

Example Data: **08 02 01 7A**

| **Parameter** | **Hex Data** | **Decimal Equivalent** | **Multiplier** | **True Value** | 
| ---- | ---- | ---- | ---- | ---- | 
| **Data Flag** | 08 02 |  |  |  | 
| **Battery Voltage** | 01 7A | 378 | 0.01 Signed | 3.78 V | 


### 3. Humidity

Example Data: **07 68 58**

| **Parameter** | **Hex Data** | **Decimal Equivalent** | **Multiplier** | **True Value** | 
| ---- | ---- | ---- | ---- | ---- | 
| **Data Flag** | 07 68 |  |  |  | 
| **Humidity** | 58 | 88 | 0.5 % Unsigned | 44.0 % RH | 


### 4. Pressure

Example Data: **06 73 25 6D**

| **Parameter** | **Hex Data** | **Decimal Equivalent** | **Multiplier** | **True Value** | 
| ---- | ---- | ---- | ---- | ---- | 
| **Data Flag** | 06 73 |  |  |  | 
| **Pressure** | 25 6D | 9581 | 0.1 hPa Unsigned MSB | 958.1 hPa | 


### 5. Temperature

Example Data: **02 67 01 1D**

| **Parameter** | **Hex Data** | **Decimal Equivalent** | **Multiplier** | **True Value** | 
| ---- | ---- | ---- | ---- | ---- | 
| **Data Flag** | 02 67 |  |  |  | 
| **Temperature** | 01 1D | 285 | 0.1 °C Signed MSB | 28.5℃ | 


### 6. Gas Resistance

Example Data: **04 02 14 AF**

| **Parameter** | **Hex Data** | **Decimal Equivalent** | **Multiplier** | **True Value** | 
| ---- | ---- | ---- | ---- | ---- | 
| **Data Flag** | 04 02 |  |  |  | 
| **Gas Resistance** | 14 AF | 5295 | 0.01 kΩ Signed | 52.95 kΩ | 


### 7. Accelerometer

Example Data: **03 71 FF FF FF DD FC 2E**

| **Parameter** | **Hex Data** | **Decimal Equivalent** | **Multiplier** | **True Value** | 
| ---- | ---- | ---- | ---- | ---- | 
| **Data Flag** | 03 71 |  |  |  | 
| **Acceleration X** | FF FF | -1 | 0.001 g Signed MSB | -0.001g | 
| **Acceleration Y** | FF DD | -35 | 0.001 g Signed MSB | -0.035g | 
| **Acceleration Z** | FC 2E | -978 | 0.001 g Signed MSB | -0.978g | 


## Decoding Sensor Data in TTN

### Input Decoding Function in TTN

**1**. To start with, download the decoding function through this **[link](https://github.com/RAKWireless/RUI_LoRa_node_payload_decoder/blob/master/RUISensorDataDecoder_for_TTN.js)**.

**2**.  From your TTN console, go to application page and click the "**Payload Formats**" tab as shown in the image below. 

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1575468646\/17320\/i4xmo8ndpvbmx8i6q8tj.jpg",
        "mode": "responsive",
        "width": 1102,
        "height": 139,
        "caption": "**Figure 3**: Payload Format at TTN Application Page"
    }
}]$

**3**. Next, select "**Payload Format**" as "**Custom**". Then, from the decoder tab, copy and paste the decoder function from **step 1**.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1575469741\/17320\/ddpqx0x7rlma36ogiwc1.jpg",
        "mode": "responsive",
        "width": 771,
        "height": 608,
        "caption": "**Figure 4**: Inputting the Decoder Function"
    }
}]$

### Testing the Validity of Decoding Sensor Data in TTN

**Input** the data below in the "**Payload**" box as shown in the image below.

**01 88 05 37 97 10 9D 59 00 DC 14 08 02 01 7A 07 68 58 06 73 25 6D 02 67 01 1D 04 02 14 AF 03 71 FF FF FF DD FC 2E**

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1575470361\/17320\/mlgmgm8lstjnnufc5q88.jpg",
        "mode": "responsive",
        "width": 896,
        "height": 901,
        "caption": "**Figure 5**: Testing Payload Data"
    }
}]$

- Then, click "**Test**" and it will generate a code with the decoded data as shown in the image above. 

$plugin[{
    "type": "code-block",
    "data": {
        "languageBlocks": [
            {
                "code": "{\n  \"DecodeDataHex\": \"0188053797109d5900dc140802017a0768580673256d0267011d040214af0371ffffffddfc2e\",\n  \"DecodeDataObj\": {\n    \"acceleration\": {\n      \"x\": \"-0.001g\",\n      \"y\": \"-0.035g\",\n      \"z\": \"-0.978g\"\n    },\n    \"battery\": \"3.78V\",\n    \"environment\": {\n      \"gasResistance\": \"52.95k\u03a9\",\n      \"humidity\": \"44.0% RH\",\n      \"pressure\": \"958.10hPa\",\n      \"temperature\": \"28.50\u00b0C\"\n    },\n\t  \"gps\": {\n      \"altitude\": \"563.4m\",\n      \"latitude\": \"34.1911\u00b0\",\n      \"longitude\": \"108.8857\u00b0\"\n    }\n  }\n}",
                "language": "none"
            }
        ]
    }
}]$

Click "save payload functions" button to save the decoding function.

## Testing in Real System in TTN

After gateway and node go online, click the uplink data record from the application data tab to check the decode status. From the image below, we can see the data decoded successfully in TTN.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1575471624\/17320\/gncjz92kenv5h8w39bp0.jpg",
        "mode": "responsive",
        "width": 1151,
        "height": 876,
        "caption": "**Figure 6**: Uplink Decoded Data"
    }
}]$

## Decoding Sensor Data in ChirpStack

### Input Decoding Function in ChirpStack

**1.** To start with, download the decoding function through this **[link](https://github.com/RAKWireless/RUI_LoRa_node_payload_decoder/blob/master/RUISensorDataDecoder_for_ChirpStack.js)**. 

**2.** From to your ChirpStack, go to application page and click the "**APPLICATION CONFIGURATION**" tab as shown in the image below.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1575471274\/17320\/vs8mobszwtkfyqeodvze.jpg",
        "mode": "responsive",
        "width": 749,
        "height": 152,
        "caption": "**Figure 7**: Application Configuration Tab"
    }
}]$

**3**. Next, select "**Payload codec**" as "**Custom JavaScript codec functions**". Then, from the decoder tab, copy and paste the decoder function from **step 1**.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1575471776\/17320\/pvjdwnmlcykwa7g4upmr.jpg",
        "mode": "responsive",
        "width": 902,
        "height": 772,
        "caption": "**Figure 8**: Decoded Function in Chirpstack"
    }
}]$

**4.** Then, click ‘**UPDATE APPLICATION**’ button to save decoding function.

### Testing in Real System in ChirpStack

After gateway and node go online, click the uplink data record from the application data at "**LIVE DEVICE DATA**" tab to check the decode status. From the image below, we can see the data decoded successfully in ChirpStack.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1575472079\/17320\/grvuetv6kt8qdtnopyuf.jpg",
        "mode": "responsive",
        "width": 1018,
        "height": 851,
        "caption": "**Figure 9**: Decode Status in ChirpStack"
    }
}]$

