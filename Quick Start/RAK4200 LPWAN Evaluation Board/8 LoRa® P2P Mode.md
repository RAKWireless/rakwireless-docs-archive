---
type: page
title: LoRa® P2P Mode
listed: true
slug: lora-p2p-mode
---published

In this section, we will discuss on how we can use P2P on our RAK4200. We will be using EU868 as our frequency, although it is applicable also to other standard bands.

1. First, find two RAK4200 LPWAN Evaluation Board which can work on EU868 frequency and make sure their firmware version isn’t less than V3.0.0.1.
2. Next, connect these two RAK4200 LPWAN Evaluation Board with PC through UART, and open two serial port tool on PC.
3. Now, configure them to both work in LoRaP2P mode as follow:

$plugin[{
    "type": "code-block",
    "data": {
        "languageBlocks": [
            {
                "code": "at+set_config=lora:work_mode:1",
                "language": "none"
            }
        ]
    }
}]$

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1579529990\/24044\/nerylgv02xmr8hstfksm.jpg",
        "mode": "responsive",
        "width": 505,
        "height": 643,
        "caption": "**Figure 1**: P2P Initialization"
    }
}]$

**4.** Then configure LoRaP2P parameters for both of them as follow for example:

$plugin[{
    "type": "code-block",
    "data": {
        "languageBlocks": [
            {
                "code": "at+set_config=lorap2p:XXX:Y:Z:A:B: C",
                "language": "none"
            }
        ]
    }
}]$

Please refer to the [auto$](/rak4200-lora-evaluation-board/configuring-the-rak4200-evaluation-board) section to learn about the definition of the parameters used.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1579529996\/24044\/cgjnyy9zykhbdemr2rvs.jpg",
        "mode": "responsive",
        "width": 973,
        "height": 599,
        "caption": "**Figure 2**: Configuring P2P in both RAK4200 Nodes"
    }
}]$

**5.** OK! Try to send a message from the first RAK4200 LPWAN Evaluation Board  to the second RAK4200 LPWAN Evaluation board.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1579530003\/24044\/csib8zhcwfkevehq7fby.jpg",
        "mode": "responsive",
        "width": 924,
        "height": 595,
        "caption": "**Figure 3**: Message sent and received status in the two Nodes"
    }
}]$

**6.** Successfully! Now, send more messages.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1579530033\/24044\/gbvh6jy5olovvt0fjyib.jpg",
        "mode": "responsive",
        "width": 935,
        "height": 600,
        "caption": "**Figure 4**: Succeeding Messages sent to the other Node"
    }
}]$

You have successfully finished your RAK4200 LPWAN Evaluation Board Set Up. You are now ready to develop the coolest project that could potentially change the world.

