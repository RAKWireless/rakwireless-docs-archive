---
type: page
title: Installing the Gateway Bridge
listed: true
slug: installing-the-gateway-bridge
---published


We are going to provide an outline on how to perform the installation. For detailed information you can visit [Chirpstack.io](https://www.chirpstack.io/).

1.Run the following commands provided below to update the Ubuntu Repositories.


$plugin[{
    "type": "code-block",
    "data": {
        "languageBlocks": [
            {
                "code": "sudo apt-key adv --keyserver keyserver.ubuntu.com --recv-keys 1CE2AFD36DBCCA00",
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
                "code": "sudo echo \"deb https:\/\/artifacts.loraserver.io\/packages\/3.x\/deb stable main\" | sudo tee \/etc\/apt\/sources.list.d\/loraserver.list",
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
                "code": "sudo apt-get update",
                "language": "none"
            }
        ]
    }
}]$


- This will update the Ubuntu Repositories.

2.Proceed with installing the Bridge itself:


$plugin[{
    "type": "code-block",
    "data": {
        "languageBlocks": [
            {
                "code": "sudo apt-get install lora-gateway-bridge",
                "language": "none"
            }
        ]
    }
}]$


3.Start the Bridge service:


$plugin[{
    "type": "code-block",
    "data": {
        "languageBlocks": [
            {
                "code": "sudo systemctl start lora-gateway-bridge",
                "language": "none"
            }
        ]
    }
}]$


4.Check if it is working as it should using the command as shown same with the snippet below:


$plugin[{
    "type": "code-block",
    "data": {
        "languageBlocks": [
            {
                "code": "journalctl -u chirpstack-gateway-bridge -f -n 50",
                "language": "none"
            }
        ]
    }
}]$



$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1592821690\/22534\/hi4q0zlhm4hlf2nx19mt.png",
        "mode": "responsive",
        "width": 1911,
        "height": 157,
        "caption": "**Figure 1:** Gateway Bridge Journal Control Output (no errors)"
    }
}]$


- Below is the text form of the logs shown in **Figure 1**:


$plugin[{
    "type": "code-block",
    "data": {
        "languageBlocks": [
            {
                "code": "ubuntu@ip-172-31-33-125:~$ journalctl -u chirpstack-gateway-bridge -f -n 50\n-- Logs begin at Wed 2020-06-17 11:59:21 UTC. --\nJun 18 10:20:29 ip-172-31-33-125 systemd[1]: Started ChirpStack Gateway Bridge.\nJun 18 10:20:29 ip-172-31-33-125 chirpstack-gateway-bridge[5596]: time=\"2020-06-18T10:20:29Z\" level=info msg=\"starting ChirpStack Gateway Bridge\" docs=\"https:\/\/www.chirpstack.io\/gateway-bridge\/\" version=3.8.0\nJun 18 10:20:29 ip-172-31-33-125 chirpstack-gateway-bridge[5596]: time=\"2020-06-18T10:20:29Z\" level=info msg=\"backend\/semtechudp: starting gateway udp listener\" addr=\"0.0.0.0:1700\"\nJun 18 10:20:29 ip-172-31-33-125 chirpstack-gateway-bridge[5596]: time=\"2020-06-18T10:20:29Z\" level=info msg=\"integration\/mqtt: connected to mqtt broker\"",
                "language": "none"
            }
        ]
    }
}]$




