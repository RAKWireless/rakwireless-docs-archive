---
type: page
title: RUI LoRa Set Send Interval
listed: true
slug: rui-lora-set-send-interval
---published

$plugin[{
    "type": "code-block",
    "data": {
        "languageBlocks": [
            {
                "code": "RUI_RETURN_STATUS rui_lora_set_send_interval(RUI_LORA_AUTO_SEND_MODE mode,uint16_t interval_time);",
                "language": "c"
            }
        ]
    }
}]$

| @brief | This API is used to set the interval time of sending data.&nbsp; | 
| ---- | ---- | 
| &nbsp;@return&nbsp; | RUI_RETURN_STATUS | 
| @param&nbsp; | RUI_LORA_AUTO_SEND_MODE<br>mode: lora auto send mode, refer to RUI. | 
|  | uint16_t app_interval:  the interval time of sending data.(unit:s) | 
| @module | RAK811, RAK4200, and RAK4600 core module. | 


