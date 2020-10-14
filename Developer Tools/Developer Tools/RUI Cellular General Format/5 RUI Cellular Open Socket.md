---
type: page
title: RUI Cellular Open Socket
listed: true
slug: rui-cellular-open-socket
---published

$plugin[{
    "type": "code-block",
    "data": {
        "languageBlocks": [
            {
                "code": "RUI_RETURN_STATUS rui_cellular_open_socket(uint8_t* data)",
                "language": "c"
            }
        ]
    }
}]$

| @brief | This API is used to open a TCP socket with a remote server. | 
| ---- | ---- | 
| @return | RUI_RETURN_STATUS | 
| @param | uint8_t* data: open TCP link cmd, for example: AT+QIOPEN=1,0,"TCP","ip",%port,0,1" | 
| @module | RAK8212-M and RAK5010 core module. | 


