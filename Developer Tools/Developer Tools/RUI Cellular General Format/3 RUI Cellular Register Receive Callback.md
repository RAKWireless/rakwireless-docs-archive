---
type: page
title: RUI Cellular Register Receive Callback
listed: true
slug: rui-cellular-register-receive-callback
---published

$plugin[{
    "type": "code-block",
    "data": {
        "languageBlocks": [
            {
                "code": "typdef void(*cellular_receive)(uint8_t *data);\nRUI_RETURN_STATUS rui_cellular_register_recv_callback(cellular_receive callback)",
                "language": "c"
            }
        ]
    }
}]$

| @brief&nbsp; | This API is used to register a callback function for cellular in&nbsp;application so that application&nbsp;can receive cellular data automatically. | 
| ---- | ---- | 
| @return | RUI_RETURN_STATUS | 
| @param | cellular_receive callback: the callback function for receiving cellular data. | 
| @module | RAK8212-M<br>and RAK5010 core module. | 


