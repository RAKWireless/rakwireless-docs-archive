---
type: page
title: RUI LoRajoin Register Callback
listed: true
slug: rui-lorajoin-register-callback
---published

$plugin[{
    "type": "code-block",
    "data": {
        "languageBlocks": [
            {
                "code": "typedef void (*lorajoin)(uint32_t status);\nRUI_RETURN_STATUS rui_lorajoin_register_callback(lorajoin callback);",
                "language": "c"
            }
        ]
    }
}]$

| @brief | This API is used to register a callback function for LoRaWAN join, so that application can start LoRaWAN function. | 
| ---- | ---- | 
| @return | RUI_RETURN_STATUS | 
| @param | lorajoin callback:          the callback function for LoRaWAN join successed. | 
|  | status:                          1<br>-&gt; join succeed, 0 -&gt; join fail. | 
| @module | RAK811, RAK4200, and RAK4600 core module. | 


