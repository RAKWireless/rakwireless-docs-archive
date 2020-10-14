---
type: page
title: Setting up the External MQTT Broker
listed: true
slug: setting-up-the-external-mqtt-broker
---published

This section provides the procedure in setting the external MQTT Broker for your Application Setup. 

## Preparing the Raspberry Pi

We are going to use going to use a Raspberry Pi 3B+ for this tutorial, as the device that is going to be hosting Mosquitto (a popular MQTT broker). 

**1**.First download the latest Raspbian Buster Lite image from the [link](https://www.raspberrypi.org/downloads/raspbian/). Then, flash the image to an SD card by following the [auto$](/rak2245-pi-hat-edition-lorawan-gateway-concentrator-module/device-firmware-setup) document. Keep in mind that the document is for RAK2245 Pi Hat Edition but it uses Raspberry Pi 3B+.

We recommend setting up the [Raspberry Pi headless](https://www.raspberrypi.org/documentation/configuration/wireless/headless.md). Once done plug the SD card into the slot and power it.

**2**.Use your favorite [SSH client](https://www.chiark.greenend.org.uk/~sgtatham/putty/latest.html) to connect to the Raspberry Pi with the following credentials:

- **Username**: pi
- **Password**: raspberry

Now as we have a platform to work with we can begin.

**3**.First execute the following command and note the IP address of the interface you will be using to connect to the network. You will need this, as it will be the address for your MQTT Broker when configuring the Gateway: 

$plugin[{
    "type": "code-block",
    "data": {
        "languageBlocks": [
            {
                "code": "ifconfig",
                "language": "none"
            }
        ]
    }
}]$

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1580972353\/23155\/zcd2yvspvxiphkvmkifj.jpg",
        "mode": "responsive",
        "width": 870,
        "height": 552,
        "caption": "**Figure 1**: Raspberry Pi interfaces"
    }
}]$

## Installing Mosquitto

**1**.Install the MQTT Broker (Mosquitto) via the command:

$plugin[{
    "type": "code-block",
    "data": {
        "languageBlocks": [
            {
                "code": "sudo apt install mosquitto mosquitto-clients",
                "language": "none"
            }
        ]
    }
}]$

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1580973008\/23155\/ixbl2ek8ayybbhe52xap.jpg",
        "mode": "responsive",
        "width": 869,
        "height": 527,
        "caption": "**Figure 2**: Mosquitto installation"
    }
}]$

**2**.Mosquitto clients help us easily test MQTT through a command line utility. We will use two command windows; one to subscribe to a topic and one to publish a message to it. Those will be explained in detail further in the tutorial.

$plugin[{
    "type": "callout",
    "data": {
        "text": "This command is not mandatory, however it is recommended as it creates a mosquitto service that will run the broker on startup.",
        "type": "info",
        "title": "Note:"
    }
}]$

$plugin[{
    "type": "code-block",
    "data": {
        "languageBlocks": [
            {
                "code": "sudo systemctl enable mosquitto.service",
                "language": "none"
            }
        ]
    }
}]$

## Configuring the Gateway to publish to the MQTT Broker

We will now then configure the Gateway to connect to our external MQTT broker. For the purpose of this example, we are going to use the built-in LoRa® Server. 

**1**.First go to the Packet Forwarder Tab and choose Built-in LoRa® Server as your Protocol:

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1580973267\/23155\/lc0cfzutfozzjnrw9m7j.jpg",
        "mode": "responsive",
        "width": 869,
        "height": 421,
        "caption": "**Figure 3**: Protocol selection"
    }
}]$

**2**.Make sure you have the LoRa® Network Server **Enabled** in the General tab:

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1580973355\/23155\/nc3w6wzrwdu8lhk6vywa.jpg",
        "mode": "responsive",
        "width": 868,
        "height": 453,
        "caption": "**Figure 4**: Built-in LoRa\u00ae Server activation"
    }
}]$

**3**.Add Your Gateway in the Gateway tab if you haven’t done so already. You can also add multiple gateways depending on your preference.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1580973580\/23155\/lcyrxuegza65jzkpdvo8.jpg",
        "mode": "responsive",
        "width": 873,
        "height": 446,
        "caption": "**Figure 5**: LoRa\u00ae Server Gateway configuration"
    }
}]$

**4**.Finally, go to the **Global Integration** tab and enter the address where you have your Mosquitto instance running in the MQTT Broker Address field leaving the Port with the default **1883** value.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1580974748\/23155\/ni4gyww0ovpmkbcp5bbz.jpg",
        "mode": "responsive",
        "width": 868,
        "height": 445,
        "caption": "**Figure 6**: Setting up the Global Integration"
    }
}]$

Now that the Gateway parameters are set, we will now register your application in order to be able to send and receive data. We are going to use the **RAK811 LoRa Evaluation Board** as an example in the next sub-section.

## Registering the Application

**1**.Open the RAK Serial Port Tool and connect to the RAK811 LoRa Evaluation Board by opening the corresponding COM Port. You can check the [auto$](/rak811-lora-evaluation-board/interfacing-with-rak811-lora-evaluation-board) to check the corresponding COM Port used by the RAK811 LoRa Evaluation Board. Reboot it so you can see the device parameters as in the image below:

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1580974907\/23155\/luru6sorbgc9ag61uqxr.jpg",
        "mode": "responsive",
        "width": 881,
        "height": 555,
        "caption": "**Figure 7**: RAK811 parameters"
    }
}]$

- In case your device is already configured to work in OTAA, it will attempt connecting to the gateway and getting authenticated. As it is not yet registered this will not be successful. We need to do some configuring first.

**2**.Execute the command to change the working region/band (EU868 in this example):

$plugin[{
    "type": "code-block",
    "data": {
        "languageBlocks": [
            {
                "code": "at+set_config=lora:region:EU868",
                "language": "none"
            }
        ]
    }
}]$

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1580974971\/23155\/rowrorg38jaudrruyr2r.jpg",
        "mode": "responsive",
        "width": 886,
        "height": 567,
        "caption": "**Figure 8**: Setting the region\/band"
    }
}]$

**3**.Set the authentication mode to OTAA:

$plugin[{
    "type": "code-block",
    "data": {
        "languageBlocks": [
            {
                "code": "at+set_config=lora:join_mode:0",
                "language": "none"
            }
        ]
    }
}]$

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1580975123\/23155\/tddzpuqrsakup4kej5hx.jpg",
        "mode": "responsive",
        "width": 889,
        "height": 591,
        "caption": "**Figure 9**: OTAA mode"
    }
}]$

- Now that your RAK811 is working in the correct region and mode you need to fill in the application parameters in your Gateway. This will register the specific device and allow you to exchange data.

**4**.Go to the **Application tab**. Enter a name for your application and press the Add button:

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1580975614\/23155\/ppnus0mbx1zi6cneyg1u.jpg",
        "mode": "responsive",
        "width": 890,
        "height": 444,
        "caption": "**Figure 10**: Application registration"
    }
}]$

**5**.Now go back to your RAK Serial Port Tool and copy the **Application EUI** and **Application Key** same with the image below:

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1580975661\/23155\/j3bhdnftqf5lno9xqmyn.jpg",
        "mode": "responsive",
        "width": 898,
        "height": 555,
        "caption": "**Figure 11**: Application EUI and Key"
    }
}]$

**6**.Input those into the corresponding fields in the **Application Configuration** screen in the Gateway. Afterwhich, **Save & Apply** (Make sure the **Auto Add Device Slider** is in the **off position**).

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1580975902\/23155\/enw4rnajjt4rayc92alu.jpg",
        "mode": "responsive",
        "width": 899,
        "height": 470,
        "caption": "**Figure 12**: Application parameters"
    }
}]$

**7**.Now you should have an **Application** created. Press the **Edit button**:

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1580976571\/23155\/slyf05knfnsh6drnqnjw.jpg",
        "mode": "responsive",
        "width": 902,
        "height": 471,
        "caption": "**Figure 13**: Editing the Application"
    }
}]$

**8**.Now, you need to add a **Device**. Copy the Device EUI from the RAK Serial Port Tool:

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1580978343\/23155\/mwpoid3ijidvaozf0ey3.jpg",
        "mode": "responsive",
        "width": 888,
        "height": 559,
        "caption": "**Figure 14**: Device EUI"
    }
}]$

**9**.Enter the **Device EUI** in the corresponding field and press the Add button same with the image shown below:

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1580978374\/23155\/wcf8vl4qjraxnuqcoiv7.jpg",
        "mode": "responsive",
        "width": 890,
        "height": 471,
        "caption": "**Figure 15**: Adding a Device"
    }
}]$

**10**.Enter a **Device name**, make sure you are in **Class A, OTAA** mode. Leave the rest of the parameters with their default settings. **Save & Apply**.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1580978415\/23155\/iajwnzh6pnrczpnss73g.jpg",
        "mode": "responsive",
        "width": 894,
        "height": 473,
        "caption": "**Figure 16**: Device parameters"
    }
}]$

**11**.You should now have your **Device** registered and if you click on the **Device EUI** you will open the corresponding Device window. Go to the **Live Device Data** tab. Here you can monitor data that the application is exchanging in real time.

$plugin[{
    "type": "callout",
    "data": {
        "text": "Leave the **Live Data** tab open as we want to monitor traffic.",
        "type": "info",
        "title": "Note:"
    }
}]$

**12**.Go the RAK **Serial Port Tool** and reboot the RAK811 LoRa Evaluation Bord with the onboard button.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1580978479\/23155\/gm99ffzbg2p2o5y54sbw.jpg",
        "mode": "responsive",
        "width": 895,
        "height": 475,
        "caption": "**Figure 17**: Successful Joining of the RAK811"
    }
}]$

- You should get same logswith the image above if everything went well. You should see the **Join request** in the **Live Data** tab and the **Join Succeeded!** message in the **Serial Tool**.

## Testing and Monitoring the Traffic

### UPLINK

Now your node is authenticated with the built-in LoRa® Server. As it is connected to the external MQTT Broker via the Global Integration, you can monitor traffic in both the Live Data tab and on the Raspberry Pi where the Mosquitto resides. Let us test this by sending an uplink frame via the RAK811 LoRa Evaluation Board.

**1**.In the command line window of the Raspberry, we need to subscribe to the Application/Device we are going to monitor the traffic of. This is done via the following command:

$plugin[{
    "type": "callout",
    "data": {
        "text": "{{**application_ID**}} \u2013 is the application ID from the Application tab in the Gateway.{{**device_EUI**}} \u2013 is the Device EUI of the RAK811 LoRa Evaluation Board",
        "type": "info",
        "title": "Note:"
    }
}]$

$plugin[{
    "type": "code-block",
    "data": {
        "languageBlocks": [
            {
                "code": "mosquitto_sub -t application\/{{application_ID}}\/device\/{{device_EUI}}\/rx -v",
                "language": "none"
            }
        ]
    }
}]$

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1580978509\/23155\/ibnajqc8jmafgf5nv302.jpg",
        "mode": "600",
        "width": 894,
        "height": 477,
        "caption": "**Figure 18**: Application ID"
    }
}]$

**2**.After executing the command, you need to send some data via the RAK Serial Port Tool. Use the command below to send an uplink frame on Frame port 1, with the Payload 1110:

$plugin[{
    "type": "code-block",
    "data": {
        "languageBlocks": [
            {
                "code": "at+send=lora:1:1110",
                "language": "none"
            }
        ]
    }
}]$

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1580978531\/23155\/lhd1flnflbhoc5pmyvo7.jpg",
        "mode": "responsive",
        "width": 895,
        "height": 469,
        "caption": "**Figure 19**: Test Uplink (Application)"
    }
}]$

- Now if you look at the three windows in the image above, in the RAK Serial Port Tool, Live Device Data and the CLI of the Raspberry, you will see that the message arriving is displayed.

**3**.You can also monitor the Gateway traffic itself. You can do this via the command:

$plugin[{
    "type": "callout",
    "data": {
        "text": "{{**eui**}} \u2013 is the Gateway EUI",
        "type": "info",
        "title": "Note:"
    }
}]$

$plugin[{
    "type": "code-block",
    "data": {
        "languageBlocks": [
            {
                "code": "mosquitto_sub -t gateway\/{{eui}}\/rx -v",
                "language": "none"
            }
        ]
    }
}]$

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1580996128\/23155\/mm16rkraq4hzyjygvhfw.jpg",
        "mode": "600",
        "width": 829,
        "height": 442,
        "caption": "**Figure 20**: Test uplink (Gateway)"
    }
}]$

- This is very convenient as you have three ways to monitor and you can see the metadata and payload in both the Gateway and via the MQTT Broker.

### DOWNLINK

There is a convenient tool in the Built-in LoRa® Server for sending a Downlink frame. 

**1**.You can find it in the Device tab in the LoRa® Network Server section. You can choose your Type of frame (confirmed/unconfirmed), the Frame port and the Hex Data shown in the image below:

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1580978572\/23155\/uva7wf2snbti9ed6m8bn.jpg",
        "mode": "600",
        "width": 821,
        "height": 402,
        "caption": "**Figure 21**: LoRa\u00ae Network Server Device Downlink tool"
    }
}]$

**2**.Once you schedule a message for downlink it will be displayed in the Live Device Data window. Upon sending the next uplink via the RAK Serial Port Tool you will also see it there, as it needs an uplink frame in order to send the downlink in the RX1 window shown in the image below.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1580978597\/23155\/ujzm6fzfpqkpgimxw1cz.jpg",
        "mode": "600",
        "width": 855,
        "height": 417,
        "caption": "**Figure 22**: Received Downlink Frame"
    }
}]$

**3**.If you want to test the Gateway downlink via the external MQTT Broker, you need to first create a json file which you will be sensing your data in. Below is what the file formatting structure needs to look like:

$plugin[{
    "type": "callout",
    "data": {
        "text": "\"**confirmed**\": **true** \u2013 This is the LoRa\u00ae frame type. True (confirmed), False (unconfirmed)\n\n\"**data**\": \"**TEST**\" \u2013 example data to be sent\n\n\"**fPort**\": **10** \u2013 the Frame Port Number",
        "type": "info",
        "title": "Note:"
    }
}]$

$plugin[{
    "type": "code-block",
    "data": {
        "languageBlocks": [
            {
                "code": "{\n\"confirmed\": true,\n\"fPort\": 10,\n\"data\": \"1001\"\n}",
                "language": "none"
            }
        ]
    }
}]$

$plugin[{
    "type": "callout",
    "data": {
        "text": "You need to have a Base64 encoded HEX data for the above to work!",
        "type": "info",
        "title": "Note:"
    }
}]$

**4**.Create the file, for example with the following command and copy the data in discussed above:

$plugin[{
    "type": "code-block",
    "data": {
        "languageBlocks": [
            {
                "code": "sudo nano test.json",
                "language": "none"
            }
        ]
    }
}]$

**5**.After you have created the file, you need to schedule it for downlink. This means that you have to publish it via Mosquitto with the command:

$plugin[{
    "type": "code-block",
    "data": {
        "languageBlocks": [
            {
                "code": "sudo mosquito_pub application\/{{application_ID{{\/device\/{{device_EUI}}\/ tx \u2013f test.json",
                "language": "none"
            }
        ]
    }
}]$

- The packet will be scheduled for downlink, which you can see in the Gateway Packet logger. 
- When the next uplink frame that comes for the Application/Device specified by the **application_ID** and **device_EUI** is received, the Gateway will send the data in the RX1 window to the node. You should have a response similar to the one in **Figure 22**.

