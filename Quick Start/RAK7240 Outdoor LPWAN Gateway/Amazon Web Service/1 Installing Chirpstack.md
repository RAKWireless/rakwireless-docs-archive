---
type: page
title: Installing Chirpstack
listed: true
slug: installing-chirpstack
---published


It is always a good idea to make an update and upgrade of your packages. In order to do so, run the following commands in the terminal:


$plugin[{
    "type": "code-block",
    "data": {
        "languageBlocks": [
            {
                "code": "sudo apt update",
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
                "code": "sudo apt upgrade",
                "language": "none"
            }
        ]
    }
}]$


1.After the procedure is completed, we are going to install ChirpStack and its dependencies. To do this first we need to install Git with the command:


$plugin[{
    "type": "code-block",
    "data": {
        "languageBlocks": [
            {
                "code": "sudo apt install git",
                "language": "none"
            }
        ]
    }
}]$


2.Next, we **clone** the
**RAKwireless Ubuntu** ChirpStack repository:


$plugin[{
    "type": "code-block",
    "data": {
        "languageBlocks": [
            {
                "code": "git clone https:\/\/github.com\/RAKWireless\/ChirpStack_on_Ubuntu",
                "language": "git"
            }
        ]
    }
}]$


3.After the cloning is complete open the newly created folder with the command:


$plugin[{
    "type": "code-block",
    "data": {
        "languageBlocks": [
            {
                "code": "cd ChirpStack_on_Ubuntu",
                "language": "none"
            }
        ]
    }
}]$


4.Run the installation script:


$plugin[{
    "type": "code-block",
    "data": {
        "languageBlocks": [
            {
                "code": "sudo .\/install.sh",
                "language": "none"
            }
        ]
    }
}]$


5.After the installation is completed, check if all went well by executing these commands:


$plugin[{
    "type": "code-block",
    "data": {
        "languageBlocks": [
            {
                "code": "journalctl -u chirpstack-network-server -f -n 50",
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
                "code": "journalctl -u chirpstack-application-server -f -n 50",
                "language": "none"
            }
        ]
    }
}]$


6.You should see no errors same with the image provided below. Make sure you interrupt the output of the commands above with the key combination “**Ctrl+Z**” so you can continue with the configuration process.


$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1592820882\/22533\/n9fhszh4vojnsmrnd8p6.png",
        "mode": "responsive",
        "width": 1909,
        "height": 758,
        "caption": "**Figure 1:** ChirpStack Journal Control Output (no errors)"
    }
}]$


- Below is the text form of the logs shown in **Figure 1**:


$plugin[{
    "type": "code-block",
    "data": {
        "languageBlocks": [
            {
                "code": "ubuntu@ip-172-31-33-125:~$ journalctl -u chirpstack-network-server -f -n 50\n-- Logs begin at Wed 2020-06-17 11:59:21 UTC. --\nJun 18 10:20:29 ip-172-31-33-125 systemd[1]: Started ChirpStack Network Server.\nJun 18 10:20:29 ip-172-31-33-125 chirpstack-network-server[5588]: time=\"2020-06-18T10:20:29Z\" level=info msg=\"starting ChirpStack Network Server\" band=EU_863_870 docs=\"https:\/\/www.chirpstack.io\/\" net_id=000000 version=3.9.0\nJun 18 10:20:29 ip-172-31-33-125 chirpstack-network-server[5588]: time=\"2020-06-18T10:20:29Z\" level=info msg=\"storage: setting up storage module\"\nJun 18 10:20:29 ip-172-31-33-125 chirpstack-network-server[5588]: time=\"2020-06-18T10:20:29Z\" level=info msg=\"storage: setting up Redis client\"\nJun 18 10:20:29 ip-172-31-33-125 chirpstack-network-server[5588]: time=\"2020-06-18T10:20:29Z\" level=info msg=\"storage: connecting to PostgreSQL\"\nJun 18 10:20:29 ip-172-31-33-125 chirpstack-network-server[5588]: time=\"2020-06-18T10:20:29Z\" level=info msg=\"storage: applying PostgreSQL data migrations\"\nJun 18 10:20:29 ip-172-31-33-125 chirpstack-network-server[5588]: time=\"2020-06-18T10:20:29Z\" level=info msg=\"storage: PostgreSQL data migrations applied\" count=0\nJun 18 10:20:29 ip-172-31-33-125 chirpstack-network-server[5588]: time=\"2020-06-18T10:20:29Z\" level=info msg=\"gateway\/mqtt: connecting to mqtt broker\" server=\"tcp:\/\/localhost:1883\"\nJun 18 10:20:29 ip-172-31-33-125 chirpstack-network-server[5588]: time=\"2020-06-18T10:20:29Z\" level=info msg=\"no geolocation-server configured\"\nJun 18 10:20:29 ip-172-31-33-125 chirpstack-network-server[5588]: time=\"2020-06-18T10:20:29Z\" level=info msg=\"configuring join-server client\" ca_cert= server=\"http:\/\/localhost:8003\" tls_cert= tls_key=\nJun 18 10:20:29 ip-172-31-33-125 chirpstack-network-server[5588]: time=\"2020-06-18T10:20:29Z\" level=info msg=\"backend\/gateway: connected to mqtt server\"\nJun 18 10:20:29 ip-172-31-33-125 chirpstack-network-server[5588]: time=\"2020-06-18T10:20:29Z\" level=info msg=\"gateway\/mqtt: subscribing to gateway event topic\" qos=0 topic=gateway\/+\/event\/+\nJun 18 10:20:29 ip-172-31-33-125 chirpstack-network-server[5588]: time=\"2020-06-18T10:20:29Z\" level=info msg=\"api: starting network-server api server\" bind=\"0.0.0.0:8000\" ca-cert= tls-cert= tls-key=\nJun 18 10:20:29 ip-172-31-33-125 chirpstack-network-server[5588]: time=\"2020-06-18T10:20:29Z\" level=info msg=\"starting downlink device-queue scheduler\"\nJun 18 10:20:29 ip-172-31-33-125 chirpstack-network-server[5588]: time=\"2020-06-18T10:20:29Z\" level=info msg=\"starting multicast scheduler\"\n^Z\n[4]+  Stopped                 journalctl -u chirpstack-network-server -f -n 50\nubuntu@ip-172-31-33-125:~$ journalctl -u chirpstack-application-server -f -n 50\n-- Logs begin at Wed 2020-06-17 11:59:21 UTC. --\nJun 18 10:20:29 ip-172-31-33-125 systemd[1]: Started ChirpStack Application Server.\nJun 18 10:20:29 ip-172-31-33-125 chirpstack-application-server[5591]: time=\"2020-06-18T10:20:29Z\" level=info msg=\"starting ChirpStack Application Server\" docs=\"https:\/\/www.chirpstack.io\/\" version=3.10.0\nJun 18 10:20:29 ip-172-31-33-125 chirpstack-application-server[5591]: time=\"2020-06-18T10:20:29Z\" level=info msg=\"storage: setting up storage package\"\nJun 18 10:20:29 ip-172-31-33-125 chirpstack-application-server[5591]: time=\"2020-06-18T10:20:29Z\" level=info msg=\"storage: setup metrics\"\nJun 18 10:20:29 ip-172-31-33-125 chirpstack-application-server[5591]: time=\"2020-06-18T10:20:29Z\" level=info msg=\"storage: setting up Redis client\"\nJun 18 10:20:29 ip-172-31-33-125 chirpstack-application-server[5591]: time=\"2020-06-18T10:20:29Z\" level=info msg=\"storage: connecting to PostgreSQL database\"\nJun 18 10:20:29 ip-172-31-33-125 chirpstack-application-server[5591]: time=\"2020-06-18T10:20:29Z\" level=info msg=\"storage: applying PostgreSQL data migrations\"\nJun 18 10:20:29 ip-172-31-33-125 chirpstack-application-server[5591]: time=\"2020-06-18T10:20:29Z\" level=info msg=\"storage: PostgreSQL data migrations applied\" count=1\nJun 18 10:20:29 ip-172-31-33-125 chirpstack-application-server[5591]: time=\"2020-06-18T10:20:29Z\" level=info msg=\"integration\/mqtt: TLS config is empty\"\nJun 18 10:20:29 ip-172-31-33-125 chirpstack-application-server[5591]: time=\"2020-06-18T10:20:29Z\" level=info msg=\"integration\/mqtt: connecting to mqtt broker\" server=\"tcp:\/\/localhost:1883\"\nJun 18 10:20:29 ip-172-31-33-125 chirpstack-application-server[5591]: time=\"2020-06-18T10:20:29Z\" level=info msg=\"api\/as: starting application-server api\" bind=\"0.0.0.0:8001\" ca_cert= tls_cert= tls_key=",
                "language": "none"
            }
        ]
    }
}]$




