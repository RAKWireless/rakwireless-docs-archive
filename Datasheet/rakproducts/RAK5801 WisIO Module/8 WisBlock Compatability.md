---
type: page
title: WisBlock Compatability
listed: false
slug: wisblock-compatability-rak5801
---draft

Since a WisBlock module can be combined with a variety of different functional modules, the pin functions of the MCU are multiplexed, so the interface expansion module for each specific function may need to be appropriately adapted for the WisBlock shipped according to standards. The adaptable modules of RAK5801 are as shown in the following table:

| **WisBlock Module** | **Adaptable Module** | **Description** | 
| ---- | ---- | ---- | 
| WisBase Baseboard | RAK5005/RAK5005-O | RAK5801 can be attached in the WisIO slot of RAK5005/RAK5005-O baseboard. | 
| WisCore Module | RAK4631 | RAK5801 is compatible with RAK4631. | 
|  | RAK4201 | Low Band: **RAK4201L-ADC**<br>High Band: **RAK4201H-ADC** | 
|  | RAK4202 | Refer to Note 1 for the hardware adaptions to the RAK5005 and RAK4202 shipped according to standards. | 
|  | RAK4261 | Refer to Note 2 for the hardware adaptations to the RAK5005 and RAK4262 shipped according to standards. | 


$plugin[{
    "type": "callout",
    "data": {
        "text": "Non-adaptable WisBlock module for RAK5801: **RAK4601**\n\n1. Only **analog0** channel analog data collection is supported when the RAK4202+RAK5801 module shipped according to standards is applied. **RAK5801** and **RAK5005** require adaptation as follows when the analog0 analog data channel is to be applied. The adapted RAK5005 does not support battery power collection.\n\n- For RAK5005 adaptation: Remove **R7**.\n- For RAK5801 adaptation: Change R94 to **R95.** Apply **PA0** to read the analog data of Channel **analog1**. Apply **PA2** to read the analog data of Channel **analog0**.\n\nAdaptation when applying **RAK4261+RAK5801**:\n\n2.Only **analog0** channel analog data collection is supported when the RAK4261+RAK5801 module shipped according to standards is applied. **RAK5801** and **RAK5005** require adaptation as follows when the analog1 analog data channel is to be applied. The adapted RAK5005 does not support battery power collection.\n\n- For RAK5005 adaptation: Remove **R7**.\n- For RAK5801 adaptation: Change R94 to **R95.** Apply **PA0** to read the analog data of Channel **analog1**. Apply **PA2** to read the analog data of Channel **analog0.**",
        "type": "info",
        "title": "Info"
    }
}]$

