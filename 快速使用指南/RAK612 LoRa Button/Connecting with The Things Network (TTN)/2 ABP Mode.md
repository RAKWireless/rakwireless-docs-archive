---
type: page
title: ABP Mode
listed: true
slug: abp-mode
---published

Follow these steps, if you want to join with The Things Network in **Activation By Personalisation** (ABP) Mode.

- Click the "**Settings**" button:

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1561823170\/17092\/kgl3xu8lh44k19mikxmm.png",
        "mode": "responsive",
        "width": 1788,
        "height": 879,
        "caption": "**Figure 1:** Settings Tab in TTN (Devices)"
    }
}]$

- And in your Settings, Go to the Activation Method section and click "ABP" then press "Save"

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1561823318\/17092\/nbfnijzlhlxgg1d2oh2g.png",
        "mode": "responsive",
        "width": 1793,
        "height": 815,
        "caption": "**Figure 2:** Activation Mode - ABP"
    }
}]$

You will now then see in the Device Overview that the Activation Method for your Device is now in ABP. 

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1561823709\/17092\/q0rlwn18mwbpicai57yv.png",
        "mode": "responsive",
        "width": 1803,
        "height": 926,
        "caption": "**Figure 3:** Activation Method in ABP in the Device Overview"
    }
}]$

Now let's configure your LoRa Button to use the ABP Activation Method.

- First, **set the join mode to ABP** using the following AT Command:
`at+set_config=join_mode:0`

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1561825586\/17092\/ihb50utynvtrryapoxs6.jpg",
        "mode": "responsive",
        "width": 551,
        "height": 703,
        "caption": "**Figure 4:** Set the Join Mode to ABP"
    }
}]$

. There are 3 things that you should take note of:

1. **Device Address** - this is the unique address of your device
2. **Network Session Key**- is used for interaction between the Node and the Network Server.
3. **App Session Key** - is used for encryption and decryption of the payload.

We need all of these to configure our LoRa button and they can be found here:

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1561827369\/17092\/wb0kwjs67kqqgyh4rjoo.png",
        "mode": "responsive",
        "width": 1803,
        "height": 926,
        "caption": "**Figure 5:** Device Address, Network Session Key and App Session Key"
    }
}]$

- In your RAK Serial Port tool, use the following AT Command to **set the Device Address**: `at+set"_config=dev_addr:"YOUR_DEVICE_ADDRESS"`

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1561827050\/17092\/cthsonh0tscezqbuhnit.jpg",
        "mode": "responsive",
        "width": 552,
        "height": 704,
        "caption": "**Figure 6:** Set the Device Address"
    }
}]$

- **Set the Network Session Key** using the following AT Command: `at+set_config=nwks_key:YOUR_NETWORK_SESSION_KEY`

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1561827573\/17092\/lp2zzfetutgyygm21s7w.jpg",
        "mode": "responsive",
        "width": 552,
        "height": 707,
        "caption": "**Figure 7:** Set the Network Session Key"
    }
}]$

- **Set the Application Session Key** using the AT Command:
`at+set_config=apps_key:"YOUR_APP_KEY"`

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1561827685\/17092\/pfloys5mpfbbhvyodkee.jpg",
        "mode": "responsive",
        "width": 554,
        "height": 707,
        "caption": "**Figure 8:** Set the Application Session Key"
    }
}]$

- Lastly, we need to use the command to **join in ABP Mode**:
`at+join=abp`

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1561827807\/17092\/esuyzxi5azxra28hzhfg.jpg",
        "mode": "responsive",
        "width": 551,
        "height": 701,
        "caption": "**Figure 9:** Join mode in ABP"
    }
}]$

- Press Key 1 on your RAK612 LoRa Button and you should the following data in your Serial Port Tool

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1561828081\/17092\/ovcromdn2hyyymbwnkwm.jpg",
        "mode": "responsive",
        "width": 550,
        "height": 705,
        "caption": "**Figure 10:** Data shown in the Serial Port"
    }
}]$

- Now, let's check the data in TTN. Go to the Data Tab in the Device Section and view data data:

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1561828128\/17092\/fl8myjceqlbjfuj1khxk.jpg",
        "mode": "responsive",
        "width": 1792,
        "height": 567,
        "caption": "**Figure 11:** Data Shown in the TTN"
    }
}]$

