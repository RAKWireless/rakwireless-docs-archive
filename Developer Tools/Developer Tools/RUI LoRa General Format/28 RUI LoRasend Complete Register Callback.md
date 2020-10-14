---
type: page
title: RUI LoRasend Complete Register Callback
listed: true
slug: rui-lorasend-complete-register-callback
---published

$plugin[{
    "type": "code-block",
    "data": {
        "languageBlocks": [
            {
                "code": "typedef void (*lorasend)(RUI_MCPS_T type);\nRUI_RETURN_STATUS rui_lorasend_complete_register_callback(lorasend callback);",
                "language": "c"
            }
        ]
    }
}]$

| @brief | This API is used to register a callback function for LoRaWAN send complete,&nbsp;so that application can<br>start LoRaWAN function. | 
| ---- | ---- | 
| @return | RUI_RETURN_STATUS | 
| @param | lorasend callback:        the callback function. | 
|  | RUI_MCPS_T&nbsp;type:      the packet type | 
| @module | RAK811, RAK4200, and RAK4600 core module. | 


