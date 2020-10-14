---
type: page
title: RUI LoRa Get DR
listed: true
slug: rui-lora-get-dr
---published

$plugin[{
    "type": "code-block",
    "data": {
        "languageBlocks": [
            {
                "code": "RUI_RETURN_STATUS rui_lora_get_dr(uint8_t* dr, uint16_t* lengthM)",
                "language": "c"
            }
        ]
    }
}]$

| **@brief** | This API is used to get current Data rate and Payload Size | 
| ---- | ---- | 
| **@return** | [RUI_RETURN_STATUS](https://doc.rakwireless.com/developer-tools/developer-tools/getting-started#rui%3Ci%3Ereturn%3C/i%3Estatus) | 
| **@param** | **uint8_t* dr**: current DR<br>**uint16_t* lengthM**: Maximum Acceptable size | 
| **@module** | RAK811, RAK4200, and RAK4600 | 


