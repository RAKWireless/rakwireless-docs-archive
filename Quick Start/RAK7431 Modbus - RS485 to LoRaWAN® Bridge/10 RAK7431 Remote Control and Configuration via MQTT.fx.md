---
type: page
title: RAK7431 Remote Control and Configuration via MQTT.fx
listed: true
slug: rak7431-remote-control-and-configuration
---published

To remotely control the RAK7431 you need to publish messages to the **Gateway’s Network Server MQTT “TX” topic**.

### Add a Scheduled Polling Task List

**Downlink instruction message format**:

$plugin[{
    "type": "custom-html",
    "data": {
        "contents": "<table style=\"text-align: center\", width = \"100%\">\n<caption style=\"text-align: center\"><b>Table 1<\/b>: Downlink instruction message format<\/caption>\n<thead>\n  <tr>\n    <th>DTU_CMD<\/th>\n    <th>MSER<\/th>\n    <th>MDATA_LEN<\/th>\n    <th colspan=\"2\">MDATA<\/th>\n  <\/tr>\n<\/thead>\n<tbody>\n        <tr>\n            <td rowspan=2>0x03<\/td>\n            <td rowspan=2>2Byte<\/td>\n            <td rowspan=2>2Byte<\/td>\n            <td>TASK_ID<\/td>\n            <td>DATA<\/td>\n        <\/tr>\n        <tr>\n            <td>1Byte<\/td>\n            <td>nByte<\/td>\n        <\/tr>\n<\/tbody>\n<\/table>"
    }
}]$

$plugin[{
    "type": "callout",
    "data": {
        "text": "The message length does not contain the header",
        "type": "info",
        "title": "Note:"
    }
}]$

**Example**: We will add a polling
instruction.

**Publish topic**:

$plugin[{
    "type": "code-block",
    "data": {
        "languageBlocks": [
            {
                "code": "application\/1\/device\/60c5a8fffe75404b\/tx",
                "language": "none"
            }
        ]
    }
}]$

$plugin[{
    "type": "callout",
    "data": {
        "text": "Application ID and Device EUI should be consistent with the\nsettings within the gateway.",
        "type": "info",
        "title": "Note:"
    }
}]$

- To successfully complete this, the JSON data format must be followed.

**Content of the uplink**:

$plugin[{
    "type": "code-block",
    "data": {
        "languageBlocks": [
            {
                "code": "{\n\"confirmed\":true, \n\"fPort\":129,\n\"data\":\"030001000901010300000002C40B\"\n}",
                "language": "none"
            }
        ]
    }
}]$

| **Parameter** | **Description** | 
| ---- | ---- | 
| **"confirmed":true** | This indicates that the downlink to the RAK7431 will be confirmed for successful receiving. | 
| **"fPort":129** | Defines the port that we want to send the command. (For more information on the fPort see the AT Command Manual for RAK7431) | 
| **"data":"030001000901010300000002C40B"** | The data of the task in hexadecimal format. | 


**The content of the data that we will send is**:

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1597214466\/45909\/chxrpgerssmrkvgj5aip.jpg",
        "mode": "responsive",
        "width": 421,
        "height": 114,
        "caption": null
    }
}]$

1. DTU command word 
2. The message number
3. Message length (excluding header)
4. The task ID
5. The content of the task

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1597214666\/45909\/nmbnb7b2xmgzvkso71a9.jpg",
        "mode": "responsive",
        "width": 1380,
        "height": 649,
        "caption": "**Figure 1**: Publishing data to RX topic"
    }
}]$

- After publishing the data, we can see the downlink instruction and uplink answer from the RAK Serial Tool:

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1597214712\/45909\/nhkuhlp7qnld1dqoft6s.jpg",
        "mode": "600",
        "width": 663,
        "height": 848,
        "caption": "**Figure 2**: Received data and sent an answer"
    }
}]$

**Message format when execution is successful**:

$plugin[{
    "type": "custom-html",
    "data": {
        "contents": "<table style=\"text-align: center\", width = \"100%\">\n<caption style=\"text-align: center\"><b>Table 2<\/b>: Message format when execution is successful<\/caption>\n<thead>\n  <tr>\n    <th>DTU_CMD<\/th>\n    <th>MSER<\/th>\n    <th>MDATA_LEN<\/th>\n    <th>MDATA<\/th>\n  <\/tr>\n<\/thead>\n<tbody>\n        <tr>\n            <td rowspan=2>0x83<\/td>\n            <td rowspan=2>2Byte<\/td>\n            <td rowspan=2>2Byte<\/td>\n            <td>TASK_ID<\/td>\n        <\/tr>\n        <tr>\n            <td>1Byte<\/td>\n        <\/tr>\n<\/tbody>\n<\/table>"
    }
}]$

- The MQTT subscription bar can see the upstream message "**83000100010101**" for successful execution.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1597215012\/45909\/hi8xsyjzclwlxfbuek6u.jpg",
        "mode": "responsive",
        "width": 1382,
        "height": 1224,
        "caption": "**Figure 3**: Received confirmation of the task"
    }
}]$

### Remove the Scheduled Polling Task List

**Downlink instruction message format**:

$plugin[{
    "type": "custom-html",
    "data": {
        "contents": "<table style=\"text-align: center\", width = \"100%\">\n<caption style=\"text-align: center\"><b>Table 3<\/b>: Downlink instruction message format<\/caption>\n<thead>\n  <tr>\n    <th>DTU_CMD<\/th>\n    <th>MSER<\/th>\n    <th>MDATA_LEN<\/th>\n    <th>MDATA<\/th>\n  <\/tr>\n<\/thead>\n<tbody>\n        <tr>\n            <td rowspan=2>0x04<\/td>\n            <td rowspan=2>2Byte<\/td>\n            <td rowspan=2>2Byte<\/td>\n            <td>TASK_ID<\/td>\n        <\/tr>\n        <tr>\n            <td>1Byte<\/td>\n        <\/tr>\n<\/tbody>\n<\/table>"
    }
}]$

**Example**: Removal of timed polling temperature and humidity sensor task order on a node:

**Publish the topic**:

$plugin[{
    "type": "code-block",
    "data": {
        "languageBlocks": [
            {
                "code": "Application\/1\/device\/60c5a8fffe75404b\/tx",
                "language": "none"
            }
        ]
    }
}]$

**Content**:

$plugin[{
    "type": "code-block",
    "data": {
        "languageBlocks": [
            {
                "code": "{\n\"confirmed\":true,\n \"fPort\":129,\n\"data\":\"040001000101\"\n}",
                "language": "none"
            }
        ]
    }
}]$

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1597216465\/45909\/ey57bxcsvgknuh8d5tnm.jpg",
        "mode": "responsive",
        "width": 1380,
        "height": 650,
        "caption": "**Figure 4**: Remove poll downlink message"
    }
}]$

**Message format when execution is successful**:

$plugin[{
    "type": "custom-html",
    "data": {
        "contents": "<table style=\"text-align: center\", width = \"100%\">\n<caption style=\"text-align: center\"><b>Table 4<\/b>: Message format when execution is successful<\/caption>\n<thead>\n  <tr>\n    <th>DTU_CMD<\/th>\n    <th>MSER<\/th>\n    <th>MDATA_LEN<\/th>\n    <th>MDATA<\/th>\n  <\/tr>\n<\/thead>\n<tbody>\n        <tr>\n            <td rowspan=2>0x84<\/td>\n            <td rowspan=2>2Byte<\/td>\n            <td rowspan=2>2Byte<\/td>\n            <td>TASK_ID<\/td>\n        <\/tr>\n        <tr>\n            <td>1Byte<\/td>\n        <\/tr>\n<\/tbody>\n<\/table>"
    }
}]$

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1597216588\/45909\/ek2grom0h6hmsmmqtaog.jpg",
        "mode": "responsive",
        "width": 1382,
        "height": 1224,
        "caption": "**Figure 5**: Poll removed successfully message"
    }
}]$

- The MQTT subscription bar sees the upstream message "**84000100010101**", which means the task was successfully removed.

### Read the Scheduled Polling Task List

**Downlink instruction message format**:

$plugin[{
    "type": "custom-html",
    "data": {
        "contents": "<table style=\"text-align: center\", width = \"100%\">\n<caption style=\"text-align: center\"><b>Table 5<\/b>: Downlink instruction message format<\/caption>\n<thead>\n  <tr>\n    <th>DTU_CMD<\/th>\n    <th>MSER<\/th>\n    <th>MDATA_LEN<\/th>\n    <th>MDATA<\/th>\n  <\/tr>\n<\/thead>\n<tbody>\n        <tr>\n            <td rowspan=2>0x05<\/td>\n            <td rowspan=2>2Byte<\/td>\n            <td rowspan=2>2Byte<\/td>\n            <td>TASK_ID<\/td>\n        <\/tr>\n        <tr>\n            <td>1Byte<\/td>\n        <\/tr>\n<\/tbody>\n<\/table>"
    }
}]$

**Publish topic**:

$plugin[{
    "type": "code-block",
    "data": {
        "languageBlocks": [
            {
                "code": "application\/1\/device\/60c5a8fffe75404b\/tx",
                "language": "none"
            }
        ]
    }
}]$

**Content**:

$plugin[{
    "type": "code-block",
    "data": {
        "languageBlocks": [
            {
                "code": "{\n\"confirmed\":true, \n\"fPort\":129, \n\"data\":\"050001000101\"\n}",
                "language": "none"
            }
        ]
    }
}]$

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1597218441\/45909\/ebbysd5rx02k1q0v2q6t.jpg",
        "mode": "responsive",
        "width": 1380,
        "height": 649,
        "caption": "**Figure 6**: Publishing the read poll task message"
    }
}]$

**Perform successful upstream message format**:

$plugin[{
    "type": "custom-html",
    "data": {
        "contents": "<table style=\"text-align: center\", width = \"100%\">\n<caption style=\"text-align: center\"><b>Table 6<\/b>: Perform successful upstream message format<\/caption>\n<thead>\n  <tr>\n    <th>DTU_CMD<\/th>\n    <th>MSER<\/th>\n    <th>MDATA_LEN<\/th>\n    <th colspan=\"2\">MDATA<\/th>\n  <\/tr>\n<\/thead>\n<tbody>\n        <tr>\n            <td rowspan=2>0x85<\/td>\n            <td rowspan=2>2Byte<\/td>\n            <td rowspan=2>2Byte<\/td>\n            <td>TASK_ID<\/td>\n            <td>DATA<\/td>\n        <\/tr>\n        <tr>\n            <td>1Byte<\/td>\n            <td>nByte<\/td>\n        <\/tr>\n<\/tbody>\n<\/table>"
    }
}]$

- Open the MQTT subscription column that is to see to the performance of the above line: "**8500010009010103000000002C40B**" is the query to the task, the order ID is 1, the task order content is 010300000002C40B (example registers).

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1597218554\/45909\/vmtzafm9zuxsluqdxule.jpg",
        "mode": "responsive",
        "width": 1382,
        "height": 1224,
        "caption": "**Figure 7**: Received message from the node"
    }
}]$

### Read the LoRa Configuration

**Downlink instruction message format**:

$plugin[{
    "type": "custom-html",
    "data": {
        "contents": "<table style=\"text-align: center\", width = \"100%\">\n<caption style=\"text-align: center\"><b>Table 7<\/b>: Downlink instruction message format<\/caption>\n<thead>\n  <tr>\n    <th>DTU_CMD<\/th>\n    <th>MSER<\/th>\n    <th>MDATA_LEN<\/th>\n    <th>MDATA<\/th>\n  <\/tr>\n<\/thead>\n<tbody>\n        <tr>\n            <td>0x06<\/td>\n            <td>2Byte<\/td>\n            <td>2Byte<\/td>\n            <td>0Byte<\/td>\n        <\/tr>\n<\/tbody>\n<\/table>"
    }
}]$

**Publish topic**:

$plugin[{
    "type": "code-block",
    "data": {
        "languageBlocks": [
            {
                "code": "Application\/1\/device\/60c5a8fffe75404b\/tx",
                "language": "none"
            }
        ]
    }
}]$

**Content**: 

$plugin[{
    "type": "code-block",
    "data": {
        "languageBlocks": [
            {
                "code": "{\n\"confirmed\":true, \n\"fPort\":129,\n \"data\":\"0600010000\"\n}",
                "language": "none"
            }
        ]
    }
}]$

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1597219259\/45909\/bqzwuczsggmfrxdacalr.jpg",
        "mode": "responsive",
        "width": 1379,
        "height": 645,
        "caption": "**Figure 8**: Publish LoRa configuration read message"
    }
}]$

**Perform successful upstream message format**:

$plugin[{
    "type": "custom-html",
    "data": {
        "contents": "<table style=\"text-align: center\", width = \"100%\">\n<caption style=\"text-align: center\"><b>Table 8<\/b>: Perform successful upstream message format<\/caption>\n<thead>\n  <tr>\n    <th>DTU_CMD<\/th>\n    <th>MSER<\/th>\n    <th>MDATA_LEN<\/th>\n    <th colspan=6>MDATA<\/th>\n  <\/tr>\n<\/thead>\n<tbody>\n        <tr>\n            <td rowspan=2>0x86<\/td>\n            <td rowspan=2>2Byte<\/td>\n            <td rowspan=2>2Byte<\/td>\n            <td>DATA RATE<\/td>\n            <td>TXPWR<\/td>\n            <td>CONFIRM<\/td>\n            <td>RETRY<\/td>\n            <td>ADR<\/td>\n            <td>DUTY CYCLE<\/td>\n        <\/tr>        \n        <tr>\n            <td>1Byte<\/td>\n            <td>1Byte<\/td>\n            <td>1Byte<\/td>\n            <td>1Byte<\/td>\n            <td>1Byte<\/td>\n            <td>1Byte<\/td>\n        <\/tr>\n<\/tbody>\n<\/table>"
    }
}]$

- **DATARATE**: Speed rate (0 – 5) 
- **TXPOWER**: The transmit power level (0 – 20) 
- **CONFIRM**: Whether to turn on ACK 0 – off, 1 – on 
- **RETRY**: Maximum re-transmission times when ACK is on (0 ~ 15) 
- **ADR**: Whether to turn on the dynamic rate adjustment 0 – off, 1 - on 
- **DUTY CYCLE**: Whether to turn on duty cycle limit 0 – off, 1 – on

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1597219665\/45909\/cocv5gkeofez1rkejio2.jpg",
        "mode": "responsive",
        "width": 875,
        "height": 531,
        "caption": "**Figure 9**: Received message with LoRa configuration"
    }
}]$

- Open the MQTT subscription bar to see the upstream message "**860001000006000010301000000**" to read the LoRa configuration based on the upstream message format for the successful execution above.

### Change the LoRa Configuration

**Downlink instruction message format**:

$plugin[{
    "type": "custom-html",
    "data": {
        "contents": "<table style=\"text-align: center\", width = \"100%\">\n<caption style=\"text-align: center\"><b>Table 9<\/b>: Downlink instruction message format<\/caption>\n<thead>\n  <tr>\n    <th>DTU_CMD<\/th>\n    <th>MSER<\/th>\n    <th>MDATA_LEN<\/th>\n    <th colspan=6>MDATA<\/th>\n  <\/tr>\n<\/thead>\n<tbody>\n        <tr>\n            <td rowspan=2>0x07<\/td>\n            <td rowspan=2>2Byte<\/td>\n            <td rowspan=2>2Byte<\/td>\n            <td>DATA RATE<\/td>\n            <td>TXPWR<\/td>\n            <td>CONFIRM<\/td>\n            <td>RETRY<\/td>\n            <td>ADR<\/td>\n            <td>DUTY CYCLE<\/td>\n        <\/tr>        \n        <tr>\n            <td>1Byte<\/td>\n            <td>1Byte<\/td>\n            <td>1Byte<\/td>\n            <td>1Byte<\/td>\n            <td>1Byte<\/td>\n            <td>1Byte<\/td>\n        <\/tr>\n<\/tbody>\n<\/table>"
    }
}]$

**Publish topic**:

$plugin[{
    "type": "code-block",
    "data": {
        "languageBlocks": [
            {
                "code": "Application\/1\/device\/60c5a8fffe75404b\/tx",
                "language": "none"
            }
        ]
    }
}]$

**Content**: 

$plugin[{
    "type": "code-block",
    "data": {
        "languageBlocks": [
            {
                "code": "{\n\"comfirmed\":true, \n\"fPort\":129,\n\"data\":\"070001000601050103010\"\n}",
                "language": "none"
            }
        ]
    }
}]$

- The above command changes the **data rate to "1"** and the **transmit power to "5"**.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1597219975\/45909\/ibldn0uehljcdkbimabg.jpg",
        "mode": "responsive",
        "width": 1376,
        "height": 646,
        "caption": "**Figure 10**: Publish change LoRa configuration data"
    }
}]$

**Perform successful upstream message format**:

$plugin[{
    "type": "custom-html",
    "data": {
        "contents": "<table style=\"text-align: center\", width = \"100%\">\n<caption style=\"text-align: center\"><b>Table 10<\/b>: Perform successful upstream message format<\/caption>\n<thead>\n  <tr>\n    <th>DTU_CMD<\/th>\n    <th>MSER<\/th>\n    <th>MDATA_LEN<\/th>\n    <th>MDATA<\/th>\n  <\/tr>\n<\/thead>\n<tbody>\n        <tr>\n            <td>0x87<\/td>\n            <td>2Byte<\/td>\n            <td>2Byte<\/td>\n            <td>0Byte<\/td>\n        <\/tr>\n<\/tbody>\n<\/table>"
    }
}]$

- Open the MQTT subscription bar to see the upstream message for successful execution: "**8700010000**".

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1597220075\/45909\/wy7jm6rzwaceodb8aub6.jpg",
        "mode": "responsive",
        "width": 869,
        "height": 525,
        "caption": "**Figure 11**: Received confirmation message"
    }
}]$

### Reset the default LoRa Configuration

**Publish topic**: 

$plugin[{
    "type": "code-block",
    "data": {
        "languageBlocks": [
            {
                "code": "Application\/1\/device\/60c5a8fffe75404b\/tx",
                "language": "none"
            }
        ]
    }
}]$

**Content**:

$plugin[{
    "type": "code-block",
    "data": {
        "languageBlocks": [
            {
                "code": "{\n\"comfirmed\":true, \n\"fPort\":129, \n\"data\":\"1D00010000\"\n}",
                "language": "none"
            }
        ]
    }
}]$

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1597220380\/45909\/o9hgypk7n5htdghs8fnw.jpg",
        "mode": "responsive",
        "width": 1378,
        "height": 646,
        "caption": "**Figure 12**: Publish reset the default LoRa configuration"
    }
}]$

- Open the MQTT subscription bar to see the upstream message for successful execution: "**9D00010000**".

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1597220479\/45909\/moitf6u4kxhqrk2bbrcp.jpg",
        "mode": "responsive",
        "width": 874,
        "height": 531,
        "caption": "**Figure 13**: Received (missing content)"
    }
}]$

**LORA configuration default values**:

$plugin[{
    "type": "custom-html",
    "data": {
        "contents": "<table style=\"text-align: center\", width = \"100%\">\n<caption style=\"text-align: center\"><b>Table 11<\/b>: LORA configuration default values<\/caption>\n<thead>\n  <tr>\n    <th>DATARATE<\/th>\n    <th>TXPOWER<\/th>\n    <th>CONFIRM<\/th>\n    <th>RETRY<\/th>\n    <th>ADR_ENABlE<\/th>\n    <th>DUTYCYCLE_ENABLE<\/th>\n  <\/tr>\n<\/thead>\n<tbody>\n        <tr>\n            <td>0 \u2013 DR_0<\/td>\n            <td>19 -19dBm<\/td>\n            <td>1 \u2013 open<\/td>\n            <td>3 times<\/td>\n            <td>1 \u2013 open<\/td>\n            <td>0 \u2013 close<\/td>\n        <\/tr>\n<\/tbody>\n<\/table>"
    }
}]$

### Read the DTU Configuration

**Downlink instruction message format**:

$plugin[{
    "type": "custom-html",
    "data": {
        "contents": "<table style=\"text-align: center\", width = \"100%\">\n<caption style=\"text-align: center\"><b>Table 12<\/b>: Downlink instruction message format<\/caption>\n<thead>\n  <tr>\n    <th>DTU_CMD<\/th>\n    <th>MSER<\/th>\n    <th>MDATA_LEN<\/th>\n    <th>MDATA<\/th>\n  <\/tr>\n<\/thead>\n<tbody>\n        <tr>\n            <td>0x08<\/td>\n            <td>2Byte<\/td>\n            <td>2Byte<\/td>\n            <td>0Byte<\/td>\n        <\/tr>\n<\/tbody>\n<\/table>"
    }
}]$

**Publish topic**:

$plugin[{
    "type": "code-block",
    "data": {
        "languageBlocks": [
            {
                "code": "Application\/1\/device\/60c5a8fffe75404b\/tx",
                "language": "none"
            }
        ]
    }
}]$

**Content**:

$plugin[{
    "type": "code-block",
    "data": {
        "languageBlocks": [
            {
                "code": "{\n\"comfirmed\":true, \n\"fPort\":129, \n\"data\":\"0800010000\"\n}",
                "language": "none"
            }
        ]
    }
}]$

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1597221074\/45909\/jnrcv3yid4q5netstfga.jpg",
        "mode": "responsive",
        "width": 1378,
        "height": 648,
        "caption": "**Figure 14**: Publish message for reading the DTU configuration"
    }
}]$

**Uplink data message format when execution successful**:

$plugin[{
    "type": "custom-html",
    "data": {
        "contents": "<table style=\"text-align: center\", width = \"100%\">\n<caption style=\"text-align: center\"><b>Table 13<\/b>: Uplink data message format when execution successful<\/caption>\n<thead>\n  <tr>\n    <th>DTU_CMD<\/th>\n    <th>MSER<\/th>\n    <th>MDATA_LEN<\/th>\n    <th colspan=5>MDATA<\/th>\n  <\/tr>\n<\/thead>\n<tbody>\n        <tr>\n            <td rowspan=2>0x88<\/td>\n            <td rowspan=2>2Byte<\/td>\n            <td rowspan=2>2Byte<\/td>\n            <td>POLL ENABLE<\/td>\n            <td>POLL PERIOD<\/td>\n            <td>BUS TIMEOUT<\/td>\n            <td>RETRY<\/td>\n            <td>RS485<\/td>\n        <\/tr>        \n        <tr>\n            <td>1Byte<\/td>\n            <td>4Byte<\/td>\n            <td>1Byte<\/td>\n            <td>1Byte<\/td>\n            <td>1Byte<\/td>\n        <\/tr>\n<\/tbody>\n<\/table>"
    }
}]$

- **POLL ENABLE**: Enables scheduled polling, 0 - off, 1 - on 
- **POLL PERIOD**: Polling period, in seconds 
- **BUS TIMEOUT**: Bus timeout. The unit is seconds 
- **RETRY**: Number of retries after bus timeout. 0 - turn off retry function 
- **RS485**: 485 bus parameters

Open the MQTT subscription bar to see the upstream message "**8800010000800000003C010050**" to read the DTU configuration according to the successful upstream message format above.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1597221331\/45909\/cficjq4nlf4ns04ub7un.jpg",
        "mode": "responsive",
        "width": 875,
        "height": 529,
        "caption": "**Figure 15**: Received message with current DTU configuration"
    }
}]$

### Change the DTU POLL configuration

**Downlink instruction message format**:

$plugin[{
    "type": "custom-html",
    "data": {
        "contents": "<table style=\"text-align: center\", width = \"100%\">\n<caption style=\"text-align: center\"><b>Table 14<\/b>: Downlink instruction message format<\/caption>\n<thead>\n  <tr>\n    <th>DTU_CMD<\/th>\n    <th>MSER<\/th>\n    <th>MDATA_LEN<\/th>\n    <th colspan=5>MDATA<\/th>\n  <\/tr>\n<\/thead>\n<tbody>\n        <tr>\n            <td rowspan=2>0x09<\/td>\n            <td rowspan=2>2Byte<\/td>\n            <td rowspan=2>2Byte<\/td>\n            <td>POLL ENABLE<\/td>\n            <td>POLL PERIOD<\/td>\n            <td>BUS TIMEOUT<\/td>\n            <td>RETRY<\/td>\n            <td>RS485<\/td>\n        <\/tr>        \n        <tr>\n            <td>1Byte<\/td>\n            <td>4Byte<\/td>\n            <td>1Byte<\/td>\n            <td>1Byte<\/td>\n            <td>1Byte<\/td>\n        <\/tr>\n<\/tbody>\n<\/table>"
    }
}]$

**Publish topic**:

$plugin[{
    "type": "code-block",
    "data": {
        "languageBlocks": [
            {
                "code": "Application\/1\/device\/60c5a8fffe75404b\/tx",
                "language": "none"
            }
        ]
    }
}]$

**Content**:

$plugin[{
    "type": "code-block",
    "data": {
        "languageBlocks": [
            {
                "code": "{\n\"comfirmed\":true, \n\"fPort\":129,\n\"data\":\"09000100080100000E10010050\"\n}",
                "language": "none"
            }
        ]
    }
}]$

- The above command changes the polling period to only 1 hour.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1597221520\/45909\/ngxfbfzfxuzxwmoyty1f.jpg",
        "mode": "responsive",
        "width": 1378,
        "height": 646,
        "caption": "**Figure 16**: Publish message for change the DTU configuration"
    }
}]$

**Uplink data message format when execution successful**:

$plugin[{
    "type": "custom-html",
    "data": {
        "contents": "<table style=\"text-align: center\", width = \"100%\">\n<caption style=\"text-align: center\"><b>Table 15<\/b>: Uplink data message format when execution successful<\/caption>\n<thead>\n  <tr>\n    <th>DTU_CMD<\/th>\n    <th>MSER<\/th>\n    <th>MDATA_LEN<\/th>\n    <th>MDATA<\/th>\n  <\/tr>\n<\/thead>\n<tbody>\n        <tr>\n            <td>0x89<\/td>\n            <td>2Byte<\/td>\n            <td>2Byte<\/td>\n            <td>0Byte<\/td>\n        <\/tr>\n<\/tbody>\n<\/table>"
    }
}]$

- Open the MQTT subscription bar to see the upstream message for successful execution: "**8900010000**".

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1597222022\/45909\/dcfsrbco21gsilyrao8k.jpg",
        "mode": "responsive",
        "width": 874,
        "height": 531,
        "caption": "**Figure 17**: Received confirmation message"
    }
}]$

### Reset the default DTU Configuration

**Publish topic**:

$plugin[{
    "type": "code-block",
    "data": {
        "languageBlocks": [
            {
                "code": "Application\/1\/device\/60c5a8fffe75404b\/tx",
                "language": "none"
            }
        ]
    }
}]$

 **Content**:

$plugin[{
    "type": "code-block",
    "data": {
        "languageBlocks": [
            {
                "code": "{\n\"comfirmed\":true,\n \"fPort\":129,\n\"data\":\"1E00010000\"\n}",
                "language": "none"
            }
        ]
    }
}]$

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1597222175\/45909\/awzerhkuz8nivvvfcoqy.jpg",
        "mode": "responsive",
        "width": 1379,
        "height": 648,
        "caption": "**Figure 18**: Publish reset the default DTU configuration"
    }
}]$

- Open the MQTT subscription bar to see the upstream message for successful execution: "**9E00010000**".

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1597222193\/45909\/iorjx08yjxe5o0uzbtme.jpg",
        "mode": "responsive",
        "width": 874,
        "height": 532,
        "caption": "**Figure 19**: Received (missing content)"
    }
}]$

**DTU Configure the initial value**:

$plugin[{
    "type": "custom-html",
    "data": {
        "contents": "<table style=\"text-align: center\", width = \"100%\">\n<caption style=\"text-align: center\"><b>Table 16<\/b>: DTU Configure the initial value<\/caption>\n<thead>\n  <tr>\n    <th>POLL_ENABLE<\/th>\n    <th>POLL_PERIOD<\/th>\n    <th>BUS_TIMEOUT<\/th>\n    <th>RS485<\/th>\n  <\/tr>\n<\/thead>\n<tbody>\n        <tr>\n            <td>1 - on<\/td>\n            <td>3600 seconds<\/td>\n            <td>1 second<\/td>\n            <td>0xE0<\/td>\n        <\/tr>\n<\/tbody>\n<\/table>"
    }
}]$

