---
type: page
title: MQTT Bridge Configuration (TLS)
listed: true
slug: mqtt-bridge-configuration--tls-
---published

MQTT is an instant messaging protocol developed by **[IBM](https://www.ibm.com/ph-en)**. MQTT is a connection protocol for M2M and Internet of Things, which adopts lightweight publishing and subscribing message transmission mechanism. Mosquitto is an open source message broker software that implements **MQTT v3.1 protocol**. It provides a lightweight, publish/subscribe message push mode, which makes short message communication between devices simple and easy to use. Please visit the corresponding sites for more information provided below.

$plugin[{
    "type": "custom-html",
    "data": {
        "contents": "<div class=\"row\">\n\n\t<div class=\"col px-0 text-left\">\n\n\t\t<p><strong> Learn More <\/strong><\/p>\n\n                <ul>\n\n                      <li><a href = \"https:\/\/mosquitto.org\/\" >Mosquitto<\/a><\/li>\n\n                      <li><a href =\"http:\/\/mqtt.org\/\" >MQTT <\/a><\/li>              \n               <\/ul>  \n\n\t<\/div>\n\n\t<div class=\"col px-0 text-left\" >\n\n\t\t<p><strong> Resources <\/strong><\/p>\n\n                    <ul> \n\n <li><a href = \"https:\/\/downloads.rakwireless.com\/cn\/LoRa\/LoRa-Server-OS\/image\/RAK-LoRa-Server-OS-Ubuntu-Image.rar\">LoRaServer Image<\/a><\/li>\n\n<li><a href = \"https:\/\/downloads.rakwireless.com\/cn\/LoRa\/LoRa-Server-OS\/Guide\/%E5%BF%AB%E9%80%9F%E5%BB%BA%E7%AB%8B%E4%B8%80%E4%B8%AA%E7%8B%AC%E7%AB%8B%E7%9A%84LoRaServer%E6%8C%87%E5%AF%BC%E6%89%8B%E5%86%8C.pdf\">LoRaServer User Manual <\/a><\/li>\n                \n <li><a href = \"https:\/\/downloads.rakwireless.com\/en\/LoRa\/Indoor-Gateway-RAK7258\/Firmware\/generate_CA.zip\">Generate_CA Zip File <\/a> <\/li>\n\n<\/div>\n\n<\/div>"
    }
}]$

## Certificate Generation

To generate the certificates, you need the following files, which you can download directly from the Generate_CA Zip File resources provided above. After which, follow the steps provided below:

**Step 1**. Login to the Ubuntu and plugin the default username and password, **rakwireless**. Switch to root user, and into the user root directory, copy **generate_CA.sh** to the current directory.

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

**Step 2**. Generate CA certificates and Mosquito Server certificates

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

**Step 3**. Generate TLS certificates and keys for LoRaServer

$plugin[{
    "type": "code-block",
    "data": {
        "languageBlocks": [
            {
                "code": ".\/generate_CA client LoRaserver",
                "language": "none"
            }
        ]
    }
}]$

**Step 4**. Generate the TLS certificate and key of LoRaGateway. **eui_60c5a8fffe6f74a0** is the certificate name. You can set it up by yourself. It is recommended to distinguish according to devices eui.

$plugin[{
    "type": "code-block",
    "data": {
        "languageBlocks": [
            {
                "code": ".\/generate_CA client eui_60c5a8fffe6f74a0",
                "language": "none"
            }
        ]
    }
}]$

**Step 5**. **Export** all certificates

## Mosquitto Certificate Configuration

**Step 1.** Copy the CA certificate and server certificate and key to **'/etc/mosquitto/certs'** directory

$plugin[{
    "type": "code-block",
    "data": {
        "languageBlocks": [
            {
                "code": "cp ~\/ca.* server.* \/etc\/mosquitto\/certs",
                "language": "none"
            }
        ]
    }
}]$

**Step 2.** Add the following content to **/etc/mosquito/mosquitto.conf**. You can use the **Linux system VIM editor** to modify the lines. Kindly click [**here**](https://www.linux.com/LEARN/VIM-101-BEGINNERS-GUIDE-VIM)for tutorials and guides for the editor mentioned beforehand. 

$plugin[{
    "type": "code-block",
    "data": {
        "languageBlocks": [
            {
                "code": "port 8883\n\ncafile \/etc\/mosquitto\/certs\/ca.crt\n\ncertfile \/etc\/mosquitto\/certs\/server.crt\n\nRAK LoRaWAN Gateway Application Note 21\n\nkeyfile \/etc\/mosquitto\/certs\/server.key\n\nrequire_certificate true\n\ntls_version tlsv1",
                "language": "none"
            }
        ]
    }
}]$

**Step 3. Restart** mosquitto

## LoRaserver Certificate Configuration

**Step 1.** Copy **CA certificate** and **LoRaserver TLS** certificate and key to **/etc/LoRaserver**

$plugin[{
    "type": "code-block",
    "data": {
        "languageBlocks": [
            {
                "code": "cp ~\/LoRaserver.* \/etc\/LoRaserver\n\ncp ~\/ca.crt \/etc\/LoRaserver",
                "language": "none"
            }
        ]
    }
}]$

**Step 2.** Modify the **network_server.gateway.backend** of **/etc/LoRaserver/LoRaserver.toml** using Linux System VIM Editor. 

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

**Step 3. Restart** LoRaserver

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

## Enable & Configure MQTT Bridge

**Step 1**. Setup the LoRa Gateway MQTT Bridge as **LoRa Packet Forwarder** Protocol.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1561823623\/16627\/jrpiy1znthvtd6h6ske1.jpg",
        "mode": "responsive",
        "width": 1194,
        "height": 594,
        "caption": "**Figure 1.** LoRa Packet Forwarder Configuration"
    }
}]$

**Step 2.** Configure LoRa Gateway MQTT Bridge

1. Modify **MQTT Broker Address/Port**, open **Enable Authentication**, and TLS Version is consistent withmosquitto tls_version (**TLSv1**).
2. Copy the contents of **~/ca.crt** in server to **CA Certificate**, copy the contents of **~/eui_60c5a8fffe6f74a0.crt** to **TLS Certificate**, and copy the contents of **~/eui_ 60c5a8fffe6f74a0.key** to **TLS Key**.
3. **Save** & **Apply**.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1561823762\/16627\/rgwnkuploadk4mvbvz1e.jpg",
        "mode": "responsive",
        "width": 1126,
        "height": 568,
        "caption": "**Figure 2.** LoRa Gateway MQTT Bridge Configuration"
    }
}]$

**Step 3.** Setup **MQTT Topic**, and note that the format should be consistent with that in **LoRaserver.toml**.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1561823816\/16627\/e49sumkqlp87rcvl6ofd.jpg",
        "mode": "responsive",
        "width": 1238,
        "height": 474,
        "caption": "**Figure 3.** MQTT Topic Template Setup"
    }
}]$

$plugin[{
    "type": "callout",
    "data": {
        "text": "The configuration of the web page here must is consistent with the configuration of LoRaServer . The {eui} in the gateway is equivalent to {MAC} in the LoRaServer.",
        "type": "warning",
        "title": "Note:"
    }
}]$

$plugin[{
    "type": "code-block",
    "data": {
        "languageBlocks": [
            {
                "code": "# absolutely needed.\n# Use \"{{ .MAC }}\" as an substitution for the LoRa gateway MAC.\n\nuplink_topic_template=\"gateway\/+\/rx\"\ndownlink_topic_template=\"gateway\/{{ .MAC }}\/tx\"\nstats_topic_template=\"gateway\/+\/stats\"\nack_topic_template=\"gateway\/+\/ack\"\nconfig_topic_template=\"gateway\/{{ .MAC }}\/config\"\n\n# MQTT server (e.g. scheme:\/\/host:port where scheme is tcp, ssl or ws)\nserver=\"ssl:\/\/127.0.0.1:8883\"\n\n# Connect with the given username (optional)\nusername=\"\"",
                "language": "none"
            }
        ]
    }
}]$

## Mosquitto_Sub Subscribe the Gateway Messages

$plugin[{
    "type": "code-block",
    "data": {
        "languageBlocks": [
            {
                "code": "mosquitto_sub -t \"gateway\/#\" -p 8883 -v --cafile ~\/ca.crt --cert ~\/eui_60c5a8fffe6f74a0.crt --key eui_60c5a8fffe6f74a0.key --tls-version tlsv1",
                "language": "none"
            }
        ]
    }
}]$

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

## View Messages Subscribed on LoRaServer

Open the WEB page of LoRaserver, into the LIVE LoRaWAN FRAMES page of the gateway. As shown in the following figure.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1561824983\/16627\/uapdcgk85f9yt8vgqh4y.jpg",
        "mode": "responsive",
        "width": 1148,
        "height": 579,
        "caption": "**Figure 4.** Viewing Messages on LoRaServer"
    }
}]$

