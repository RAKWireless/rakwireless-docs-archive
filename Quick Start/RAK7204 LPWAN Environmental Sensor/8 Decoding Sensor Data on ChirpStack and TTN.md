---
type: page
title: Decoding Sensor Data on ChirpStack and TTN
listed: true
slug: analyzing-the-data-from-rak7204
---published

## Analyzing Sensor Data from RAK7204

In the previous section, we have successfully sent some raw data from our RAK7204 LPWAN Tracker to The Things Network, but the problem is that you can't really see the actual sensor data from the payload. In this section , we will solve that and understand what each payload means.

Let's take this data for example:

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1571386386\/18994\/ezfqysepeiwg0ufmxneo.jpg",
        "mode": "responsive",
        "width": 998,
        "height": 328,
        "caption": "**Figure 1:** Received Raw Data in TTN"
    }
}]$

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1571386399\/18994\/w4zrtlqhhmqewdwntd3d.jpg",
        "mode": "responsive",
        "width": 1447,
        "height": 251,
        "caption": "**Figure 2:** Actual Data sent to Cayenne"
    }
}]$

For this example, the payload is : **08 02 01 63 07 68 4B 06 73 25 9E 02 67 01 15 04 02 22 72 04 02 22 72**

Now lets analyze each data , which is in Hexadecimal Format. We will be using the data mentioned above as an example. We will convert the Hexadecimal Data into Decimal Data using this [converter](https://www.rapidtables.com/convert/number/hex-to-decimal.html?x=FF) in order to be able to understand it.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1571386509\/18994\/rxvyqkcqn6tqayqijhyi.jpg",
        "mode": "300",
        "width": 360,
        "height": 278,
        "caption": "**Figure 3:** Hexadecimal to Decimal converter"
    }
}]$

### 1. Battery Voltage

Example Data: **08 02 01 67**

| **Parameter** | **Hex Data** | **Decimal Equivalent** | **Multiplier** | **True Value** | 
| ---- | ---- | ---- | ---- | ---- | 
| **Data flag** | 08 02 |  |  |  | 
| **Battery Voltage** | 01 67 | 355 | 0.01 Signed | 3.55 V | 


### 2. Humidity Data

Example Data: **07 68 4B**

| **Parameter** | **Hex Data** | **Decimal Equivalent** | **Multiplier** | **True Value** | 
| ---- | ---- | ---- | ---- | ---- | 
| **Data flag** | 07 68 |  |  |  | 
| **Humidity** | 4B | 75 | 0.5 % Unsigned | 37.5 % RH | 


### 3. Pressure Data

Example Data: **06 73 25 9E**

| **Parameter** | **Hex Data** | **Decimal Equivalent** | **Multiplier** | **True Value** | 
| ---- | ---- | ---- | ---- | ---- | 
| **Data flag** | 06 73 |  |  |  | 
| **Pressure** | 25 9E | 9630 | 0.1 hPa Unsigned MSB | 963.0 hPa | 


### 4. Temperature Data

Example Data:  **02 67 01 15**

| **Parameter** | **Hex Data** | **Decimal Equivalent** | **Multiplier** | **True Value** | 
| ---- | ---- | ---- | ---- | ---- | 
| **Data flag** | 02 67 |  |  |  | 
| **Temperature** | 01 15 | 277 | 0.1 °C Signed MSB | 27.7℃ | 


### 5. Gas Resistance Data

Example Data: **04 02 22 72**

| **Parameter** | **Hex Data** | **Decimal Equivalent** | **Multiplier** | **True Value** | 
| ---- | ---- | ---- | ---- | ---- | 
| **Data flag** | 04 02 |  |  |  | 
| **Gas Resistance** | 22 72 | 8818 | 0.01 kΩ Signed | 88.18 kΩ | 


For further details about the LPP format, you can take a look at this**[ link.](https://developers.mydevices.com/cayenne/docs/lora/#lora-cayenne-low-power-payload-overview)**

## Decoding Sensor Data in TTN

### Input Decoding Function in TTN

**1.** To start with, download the decoding function through this **[link](https://github.com/RAKWireless/RUI_LoRa_node_payload_decoder/blob/master/RUISensorDataDecoder_for_TTN.js)**.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1579793818\/18994\/mj2ln3bm2so2fkpzntxt.png",
        "mode": "responsive",
        "width": 1934,
        "height": 943,
        "caption": "**Figure 4:** Github Page for the Decoding Function"
    }
}]$

**2**. From your TTN console, go to application page and click the "**Payload Formats**" tab as shown in the image below.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1575473066\/18994\/qmpbcubp9g1hiqncdsnx.jpg",
        "mode": "responsive",
        "width": 1102,
        "height": 139,
        "caption": "**Figure 5**: Payload Format at TTN Application Page"
    }
}]$

**3**. Next, select "**Payload Format**" as "**Custom**". Then, from the decoder tab, copy and paste the decoder function from **step 1**.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1575473095\/18994\/gk4wflbvc74a8bam946s.jpg",
        "mode": "responsive",
        "width": 771,
        "height": 608,
        "caption": "**Figure 6:** Decoder Function"
    }
}]$

### Testing the Validity of Decoding Sensor Data in TTN

**1. Input** the data below in the "**Payload**" box as shown in the image below.

**08 02 01 63 07 68 4B 06 73 25 9E 02 67 01 15 04 02 22 72 04 02 22 72**

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1575473257\/18994\/yqoerimlyt5zz2qkbbv8.jpg",
        "mode": "responsive",
        "width": 900,
        "height": 882,
        "caption": "**Figure 7**: Testing Payload Data"
    }
}]$

**2.** Then, click "**Test**" and it will generate a code with the decoded data as shown in the image above.

### Testing in Real System in TTN

After gateway and node go online, click the uplink data record from the application data tab to check the decode status. From the image below, we can see the data decoded successfully in TTN.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1575473292\/18994\/ao96e3gsctjbrzxvue3a.jpg",
        "mode": "responsive",
        "width": 1151,
        "height": 876,
        "caption": "**Figure 8**: Uplink Decoded Data"
    }
}]$

## Decoding Sensor Data in ChirpStack

### Input Decoding Function in ChirpStack

**1.** To start with, download the decoding function through this **[link](https://github.com/RAKWireless/RUI_LoRa_node_payload_decoder/blob/master/RUISensorDataDecoder_for_ChirpStack.js)**.

**2.** From to your ChirpStack, go to application page and click the "**APPLICATION CONFIGURATION**" tab as shown in the image below.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1575473472\/18994\/klrcxtorpusmjb9who1t.jpg",
        "mode": "responsive",
        "width": 749,
        "height": 152,
        "caption": "**Figure 9**: Application Configuration Tab"
    }
}]$

**3**. Next, select "**Payload codec**" as "**Custom JavaScript codec functions**". Then, from the decoder tab, copy and paste the decoder function from **step 1**.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1575473487\/18994\/iea9w4hz2mdgzmzadjnd.jpg",
        "mode": "responsive",
        "width": 902,
        "height": 772,
        "caption": "**Figure 10**: Decoded Function in Chirpstack"
    }
}]$

**4.** Then, click ‘**UPDATE APPLICATION**’ button to save decoding function.

### Testing in Real System in ChirpStack

After gateway and node go online, click the uplink data record from the application data at "**LIVE DEVICE DATA**" tab to check the decode status. From the image below, we can see the data decoded successfully in ChirpStack.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1575473527\/18994\/vva4otkahxoguyktqljd.jpg",
        "mode": "responsive",
        "width": 1018,
        "height": 851,
        "caption": "**Figure 11**: Decode Status in ChirpStack"
    }
}]$

