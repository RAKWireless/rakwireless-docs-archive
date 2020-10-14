---
type: page
title: RUI LoRa Get Status
listed: true
slug: rui-lora-get-status
---published

$plugin[{
    "type": "code-block",
    "data": {
        "languageBlocks": [
            {
                "code": "RUI_RETURN_STATUS rui_lora_get_status(bool IsPrint,RUI_LORA_STATUS_T *status);",
                "language": "c"
            }
        ]
    }
}]$

| &nbsp;@brief | This API is used to get all status about LoRa. | 
| ---- | ---- | 
| @return&nbsp; | RUI_RETURN_STATUS&nbsp; | 
| @param&nbsp; | bool IsPrint:whether print<br>parameters through serial | 
| @param | RUI_LORA_STATUS_T *status:           the status about LoRa | 
| @module | RAK811, RAK4200, and RAK4600 core module. | 


