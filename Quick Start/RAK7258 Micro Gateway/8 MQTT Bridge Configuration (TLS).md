---
type: page
title: MQTT Bridge Configuration (TLS)
listed: false
slug: mqtt-bridge-configuration--tls-
---published

MQTT is an instant messaging protocol developed by **[IBM](https://www.ibm.com/ph-en)**. MQTT is a connection protocol for M2M and Internet of Things, which adopts lightweight publishing and subscribing message transmission mechanism. Mosquitto is an open source message broker software that implements **MQTT v3.1 protocol**. It provides a lightweight, publish/subscribe message push mode, which makes short message communication between devices simple and easy to use. Please visit the corresponding sites for more information provided below.

$plugin[{
    "type": "custom-html",
    "data": {
        "contents": "<div class=\"row\">\n\n\t<div class=\"col px-0 text-left\">\n\n\t\t<p><strong> Learn More <\/strong><\/p>\n\n                <ul>\n\n                      <li><a href = \"https:\/\/mosquitto.org\/\" >Mosquitto<\/a><\/li>\n\n                      <li><a href =\"http:\/\/mqtt.org\/\" >MQTT <\/a><\/li>              \n               <\/ul>  \n\n\t<\/div>\n\n\t<div class=\"col px-0 text-left\" >\n\n\t\t<p><strong> Resources <\/strong><\/p>\n\n                    <ul> \n\n <li><a href = \"https:\/\/downloads.rakwireless.com\/cn\/LoRa\/LoRa-Server-OS\/image\/RAK-LoRa-Server-OS-Ubuntu-Image.rar\">LoRaServer Image<\/a><\/li>\n\n<li><a href = \"https:\/\/downloads.rakwireless.com\/cn\/LoRa\/LoRa-Server-OS\/Guide\/%E5%BF%AB%E9%80%9F%E5%BB%BA%E7%AB%8B%E4%B8%80%E4%B8%AA%E7%8B%AC%E7%AB%8B%E7%9A%84LoRaServer%E6%8C%87%E5%AF%BC%E6%89%8B%E5%86%8C.pdf\">LoRaServer User Manual <\/a><\/li>\n                \n <li><a href = \"https:\/\/downloads.rakwireless.com\/en\/LoRa\/Indoor-Gateway-RAK7258\/Firmware\/generate_CA.zip\">generate_CA.zip File <\/a> <\/li>\n\n<\/div>\n\n<\/div>"
    }
}]$

Make sure to first install the Ubuntu image that comes with LoRa® Server pre-installed. To do this use the Image and Manual from the **Resources t**ab above.

## Certificate Generation

To generate the certificates, you need the following files, which you can download directly from the Generate_CA Zip File resources provided above. After which, follow the steps provided below:

1.Login to the Ubuntu and plugin the default username and password, **rakwireless**. Switch to root user, and into the user root directory, copy **generate_CA.sh** to the current directory.

$plugin[{
    "type": "code-block",
    "data": {
        "languageBlocks": [
            {
                "code": "su root\ncd ~\nchmod +x generate_CA.sh",
                "language": "none"
            }
        ]
    }
}]$

2.Generate CA certificates and Mosquito Server certificates.

$plugin[{
    "type": "code-block",
    "data": {
        "languageBlocks": [
            {
                "code": ".\/generate_CA server",
                "language": "none"
            }
        ]
    }
}]$

3.Generate TLS certificates and keys for the LoRa® Network Server (NS).

$plugin[{
    "type": "code-block",
    "data": {
        "languageBlocks": [
            {
                "code": ".\/generate_CA.sh client loraserver",
                "language": "none"
            }
        ]
    }
}]$

4.Generate the TLS Certificate and Key for the LoRa® Application Server (AS)

$plugin[{
    "type": "code-block",
    "data": {
        "languageBlocks": [
            {
                "code": ".\/generate_CA.sh client loraappserver",
                "language": "none"
            }
        ]
    }
}]$

5.Generate the TLS certificate and key for the Client (Gateway).

$plugin[{
    "type": "code-block",
    "data": {
        "languageBlocks": [
            {
                "code": ".\/generate_CA.sh client eui_xxx",
                "language": "none"
            }
        ]
    }
}]$

$plugin[{
    "type": "callout",
    "data": {
        "text": "Raplace **xxx** with the EUI of your Gateway.",
        "type": "info",
        "title": "Info"
    }
}]$

6.**Export** all certificates

## Configure Mosquitto

1.Copy the CA Certificate and the Server certificate and Key to the directory
_/etc/mosquitto/certs_

$plugin[{
    "type": "code-block",
    "data": {
        "languageBlocks": [
            {
                "code": "sudo cp ~\/ca.* server.* \/etc\/mosquitto\/certs",
                "language": "none"
            }
        ]
    }
}]$

2.Edit _/etc/mosquitto/mosquitto.conf_ adding the code below.
You can use the **Linux system VIM editor** to modify the lines. Kindly click [**here**](https://www.linux.com/LEARN/VIM-101-BEGINNERS-GUIDE-VIM) for a tutorial on how to use VIM.

$plugin[{
    "type": "code-block",
    "data": {
        "languageBlocks": [
            {
                "code": "port 8883\n\ncafile \/etc\/mosquitto\/certs\/ca.crt\n\ncertfile \/etc\/mosquitto\/certs\/server.crt\n\nkeyfile \/etc\/mosquitto\/certs\/server.key\n\nrequire_certificate true\n\ntls_version tlsv1",
                "language": "none"
            }
        ]
    }
}]$

3.Restart the mosquitto service

$plugin[{
    "type": "code-block",
    "data": {
        "languageBlocks": [
            {
                "code": "systemctl restart mosquitto",
                "language": "none"
            }
        ]
    }
}]$

## Configure LoRa® Server

1.Copy the **CA certificate** and **Key** for the loraserver to _/etc/loraserver_

$plugin[{
    "type": "code-block",
    "data": {
        "languageBlocks": [
            {
                "code": "cp ~\/loraserver.* \/etc\/loraserver\n\ncp ~\/ca.crt \/etc\/loraserver",
                "language": "none"
            }
        ]
    }
}]$

2.Edit the file _network_server.gateway.backend_ located in _/etc/loraserver/loraserver.toml_

$plugin[{
    "type": "code-block",
    "data": {
        "languageBlocks": [
            {
                "code": "# absolutely needed.\n# Use \"{{ .MAC }}\" as an substitution for the LoRa gateway MAC.\n\nuplink_topic_template=\"gateway\/+\/rx\"\ndownlink_topic_template=\"gateway\/{{ .MAC }}\/tx\"\nstats_topic_template=\"gateway\/+\/stats\"\nack_topic_template=\"gateway\/+\/ack\"\nconfig_topic_template=\"gateway\/{{ .MAC }}\/config\"\n\n# MQTT server (e.g. scheme:\/\/host:port where scheme is tcp, ssl or ws)\nserver=\"ssl:\/\/127.0.0.1:8883\"\n\n# Connect with the given username (optional)\nusername=\"\"\n\n# but the certificate used by the server is not trusted by any CA certificate\n# on the server (e.g. when self generated)\nca_cert=\"\/etc\/loraserver\/ca.crt\"\n\n#TLS certificate file (optional)\ntls_cert=\"\/etc\/loraserver\/loraserver.crt\"\n\n#TLS key file (optional)\ntls_cert=\"\/etc\/loraserver\/loraserver.key\"\n\n\n# on the server (e.g. when self generated).\nca_cert=\"\/etc\/LoRaserver\/ca.crt\"\n\n# TLS certificate file (optional)\ntls_cert=\"\/etc\/LoRaserver\/LoRaserver.crt\"\n\n# TLS key file (optional)\ntls_key=\"\/etc\/LoRaserver\/LoRaserver.key\"",
                "language": "none"
            }
        ]
    }
}]$

3.Restart the loraserver service

$plugin[{
    "type": "code-block",
    "data": {
        "languageBlocks": [
            {
                "code": "systemctl restart LoRaserver",
                "language": "none"
            }
        ]
    }
}]$

## Configure the LoRaWAN® Gateway

1.Configure the **LoRa**® **Packet Forwarder Protocol** to work as a **LoRaWAN**® **Gateway MQTT Bridge**. This can be done in the **LoRaWAN**® **Gateway** Tab in the Gateway Web UI:

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1565577319\/16627\/i4g2wrurbccxvgwyq2dv.jpg",
        "mode": "responsive",
        "width": 1920,
        "height": 969,
        "caption": "**Figure 1**: LoRa Packet Forwarder Configuration"
    }
}]$

2.Configure the LoRaWAN® Gateway MQTT Bridge

- Configure the **MQTT Broker Address/Port (port 8883 is default), Enable Authentication** (via the slider).
- Choose the **TLS Version (TLSv1)** and enter the **Username/Password** (leave blank if you have not entered any in the loraserver.toml file - default).
- Select self-signed server & client certificate for the **SSL/TLS Mode**.
- Do the following steps in order:

1. Copy the content of _~/ca.crt_
in server to CA Certificate
2. Copy content of ~/eui_xxx.crt to TLS Certificate
3. Copy content of ~/eui_ xxx.key to TLS Key

$plugin[{
    "type": "callout",
    "data": {
        "text": "The **xxx** in the above stands for the EUI of your gateway so make sure you insert the correct values.",
        "type": "info",
        "title": "Info"
    }
}]$

- Save & Apply

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1561823762\/16627\/rgwnkuploadk4mvbvz1e.jpg",
        "mode": "responsive",
        "width": 1126,
        "height": 568,
        "caption": "**Figure 2**: LoRaWAN\u00ae Gateway MQTT Bridge Configuration"
    }
}]$

3.Setup the **MQTT Topics**, and note that the format should be consistent with that in **loraserver.toml**.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1561823816\/16627\/e49sumkqlp87rcvl6ofd.jpg",
        "mode": "responsive",
        "width": 1238,
        "height": 474,
        "caption": "**Figure 3**: MQTT Topic Template Setup"
    }
}]$

$plugin[{
    "type": "callout",
    "data": {
        "text": "The Topic templates in the Web UI and in the loraserver.toml should be identical. The {{eui}} corresponds to the {{ .MAC }} field.",
        "type": "warning",
        "title": "Note:"
    }
}]$

$plugin[{
    "type": "code-block",
    "data": {
        "languageBlocks": [
            {
                "code": "# absolutely needed.\n# Use \"{{ .MAC }}\" as an substitution for the LoRaWAN gateway MAC.\n\nuplink_topic_template=\"gateway\/+\/rx\"\ndownlink_topic_template=\"gateway\/{{ .MAC }}\/tx\"\nstats_topic_template=\"gateway\/+\/stats\"\nack_topic_template=\"gateway\/+\/ack\"\nconfig_topic_template=\"gateway\/{{ .MAC }}\/config\"\n\n# MQTT server (e.g. scheme:\/\/host:port where scheme is tcp, ssl or ws)\nserver=\"ssl:\/\/127.0.0.1:8883\"\n\n# Connect with the given username (optional)\nusername=\"\"",
                "language": "none"
            }
        ]
    }
}]$

## Subscribe to the MQTT topic of the Gateway

Use the command below to subscribe to the MQTT topic where the Gateway is publishing data.

$plugin[{
    "type": "code-block",
    "data": {
        "languageBlocks": [
            {
                "code": "mosquitto_sub -t \"gateway\/#\" -p 8883 -v --cafile ~\/ca.crt --cert ~\/eui_xxx.crt --key eui_xxx.key --tls-version tlsv1",
                "language": "none"
            }
        ]
    }
}]$

$plugin[{
    "type": "callout",
    "data": {
        "text": "The **xxx** in the above stands for the EUI of your gateway so make sure you insert the correct values.",
        "type": "info",
        "title": "Info"
    }
}]$

If you receive a message as in the box below than you have successfully subscribed!

$plugin[{
    "type": "code-block",
    "data": {
        "languageBlocks": [
            {
                "code": "gateway\/60c5a8fffe6f74a0\/rx\n{\"rxInfo\":{\"mac\":\"60c5a8fffe6f74a0\",\"timestamp\":2036224996,\"frequency\":905300000,\"channel\":7,\"rfChain\":1,\"crcStatus\":1,\"codeRate\":\"4\/5\",\"rssi\":-23,\"LoRaSNR\":10.5,\"size\":24,\"dataRate\":{\"modulation\":\"LoRa\",\"spreadFactor\":7,\"bandwidth\":125},\"board\":0,\"antenna\":0},\"phyPayload\":\"gC5K1gGASwIFAUrhF\/nr2MDyWNXIw9L4\"}\n\ngateway\/60c5a8fffe6f74a0\/tx\n{\"token\":35594,\"txInfo\":{\"mac\":\"60c5a8fffe6f74a0\",\"immediately\":false,\"timestamp\":2037224996,\"frequency\":927500000,\"power\":20,\"dataRate\":{\"modulation\":\"LoRa\",\"spreadFactor\":7,\"bandwidth\":500},\"codeRate\":\"4\/5\",\"iPol\":true,\"board\":0,\"antenna\":0},\"phyPayload\":\"YC5K1gGgOQI9VpIf\"}\n\ngateway\/60c5a8fffe6f74a0\/ack {\"mac\":\"60c5a8fffe6f74a0\",\"token\":35594}gateway\/60c5a8fffe6f74a0\/stat {\"mac\":\"60c5a8fffe6f74a0\",\"time\":\"2019-04-02T07:18:54Z\",\"rxPacketsReceived\":5,\"rxPacketsReceivedOK\":3,\"txPacketsReceived\":3,\"txPacketsEmitted\":3}\n\ngateway\/60c5a8fffe6f74a0\/rx\n{\"rxInfo\":{\"mac\":\"60c5a8fffe6f74a0\",\"timestamp\":2046166763,\"frequency\":904100000,\"channel\":1,\"rfChain\":0,\"crcStatus\":1,\"codeRate\":\"4\/5\",\"rssi\":-21,\"LoRaSNR\":9.8,\"size\":17,\"dataRate\":{\"modulation\":\"LoRa\",\"spreadFactor\":7,\"bandwidth\":125},\"board\":0,\"antenna\":0},\"phyPayload\":\"gC5K1gGATAID1VoTFGxWaz8=\"}\n\ngateway\/60c5a8fffe6f74a0\/tx\n{\"token\":19073,\"txInfo\":{\"mac\":\"60c5a8fffe6f74a0\",\"immediately\":false,\"timestamp\":2047166763,\"frequency\":923900000,\"power\":20,\"dataRate\":{\"modulation\":\"LoRa\",\"spreadFactor\":7,\"bandwidth\":500},\"codeRate\":\"4\/5\",\"iPol\":true,\"board\":0,\"antenna\":0},\"phyPayload\":\"YC5K1gGgOgLJfJ+g\"}\n\ngateway\/60c5a8fffe6f74a0\/ack {\"mac\":\"60c5a8fffe6f74a0\",\"token\":19073}",
                "language": "none"
            }
        ]
    }
}]$

## Viewing the RAW LoRa® Frames in the Web UI

Go to the Gateway tab of your **LoRa**® **Application Server Web UI**. Select your Gateway and go to the **LIVE LoRaWAN**® **FRAMES** tab. You should see the frames in real time.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1561824983\/16627\/uapdcgk85f9yt8vgqh4y.jpg",
        "mode": "responsive",
        "width": 1148,
        "height": 579,
        "caption": "**Figure 4**: Viewing The Raw LoRaWAN\u00ae Frames going through the Gateway"
    }
}]$

