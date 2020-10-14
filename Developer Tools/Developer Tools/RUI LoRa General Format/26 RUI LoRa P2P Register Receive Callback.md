---
type: page
title: RUI LoRa P2P Register Receive Callback
listed: true
slug: rui-lora-p2p-register-receive-callback
---published

$plugin[{
    "type": "code-block",
    "data": {
        "languageBlocks": [
            {
                "code": "typedef void (*lorap2p_receive)(RUI_LORAP2P_RECEIVE_T *data);\nRUI_RETURN_STATUS rui_lorap2p_register_recv_callback(lorap2p_receive callback);",
                "language": "c"
            }
        ]
    }
}]$

| @brief | This API is used to register a callback function<br>for LoRaP2P, so that application&nbsp;can receive the LoRap2p data automatically | 
| ---- | ---- | 
| @return | RUI_RETURN_STATUS | 
| @param | lora_receive callback:  the callback<br>function for receiving LoRaP2P data. | 
| @module | RAK811, RAK4200, and RAK4600 core module. | 


