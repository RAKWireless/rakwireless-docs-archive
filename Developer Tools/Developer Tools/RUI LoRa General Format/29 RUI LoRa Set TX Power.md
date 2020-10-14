---
type: page
title: RUI LoRa Set TX Power
listed: true
slug: rui-lora-tx-power
---published

$plugin[{
    "type": "code-block",
    "data": {
        "languageBlocks": [
            {
                "code": "RUI_RETURN_STATUS rui_lora_set_tx_power(uint8_t power_value);",
                "language": "c"
            }
        ]
    }
}]$

| @brief | This API is used to<br>set  lora sending power | 
| ---- | ---- | 
| @return | RUI_RETURN_STATUS | 
| @param | uint8_t<br>power_value.&lt;range:0~15 according thr region&gt; | 
| @module | RAK811, RAK4200, and RAK4600 core module. | 


