---
type: page
title: ABP Mode
listed: true
slug: abp-mode
---published

This is a mode best used for testing environments. It is not recommended for production, as it is less secure.

By default when adding a device in TTN it is in OTTA mode. This has been covered in the previous section. You need to first register one and than change the mode from OTAA to ABP. Thus we will use the previous example as base and assume there is already an OTTA mode device present.

Go to your device page and click on the _Settings_ tab:

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1562894959\/17614\/cmb0tgja4iftvkfign1r.jpg",
        "mode": "responsive",
        "width": 1892,
        "height": 764,
        "caption": "**Figure 1**: Device page"
    }
}]$

- You should end up in a screen resembling the one in Figure 2:

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1562895164\/17614\/y6uhacckvhd4shrfjz2g.jpg",
        "mode": "responsive",
        "width": 1900,
        "height": 886,
        "caption": "**Figure 2**: Device Settings page"
    }
}]$

- You can now change to ABP mode as shown in Figure 2 above. Once you do this a number of new fields will appear in the page below the _ABP button._

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1562896749\/17614\/eyxtcbfgzx232f3pnrfv.jpg",
        "mode": "responsive",
        "width": 1886,
        "height": 848,
        "caption": "**Figure 3**: ABP Settings"
    }
}]$
H2M_LI_HEADER **The Network Session Key** and the **Application Session Key** will be automatically generated. Return to the device overview page:

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1562897152\/17614\/q3mhzt8psleziv1ntcce.jpg",
        "mode": "responsive",
        "width": 1886,
        "height": 826,
        "caption": "**Figure 4**: ABP Network parameters"
    }
}]$

- Note the **Device Address**, **The Network Session Key** and the **Application Session Key**. You will need to input those in your node. In your RAK Serial Port Tool, enter the following AT Commands to update the parameters to the ones from Figure 4.

`at+dev_addr=DEV_ADD` - where DEV_ADD is your Device Address

`at+nwks_key=NWSK_KEY` - where NWSK_KEY is your Network Session Key

`at+apps_key=APPS_KEY` - where APPS_KEY is your Application Session Key

These will update the parameter. Finally enter the line to change operation mode to ABP:

`at+join_mode=abp`

Your node should now work in ABP mode.

