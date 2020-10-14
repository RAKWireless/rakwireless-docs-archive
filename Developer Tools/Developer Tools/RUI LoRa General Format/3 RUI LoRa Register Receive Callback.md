---
type: page
title: RUI LoRa Register Receive Callback
listed: true
slug: rui-lora-register-receive-callback
---published

$plugin[{
    "type": "code-block",
    "data": {
        "languageBlocks": [
            {
                "code": "typdef void (*lora_receive)(uint8_t *data);\nRUI_RETURN_STATUS rui_lora_register_recv_callback(lora_receive callback)",
                "language": "c"
            }
        ]
    }
}]$

| @brief | This API is used to register a callback function for LoRa in application, so that application can receive the LoRa data automatically. | 
| ---- | ---- | 
| @return | RUI_RETURN_STATUS | 
| @param | lora_receive callback: the callback function for receiving LoRa<br>data | 
| @module | RAK811, RAK4200, and RAK4600 core module. | 


