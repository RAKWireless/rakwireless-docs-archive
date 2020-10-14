---
type: page
title: RUI Cellular Response
listed: true
slug: rui-cellular-response
---published

$plugin[{
    "type": "code-block",
    "data": {
        "languageBlocks": [
            {
                "code": "RUI_RETURN_STATUS rui_cellular_response(uint8_t *response, uint32_t len, uint32_t timeout)",
                "language": "c"
            }
        ]
    }
}]$

| @brief | This API is used to wait for a correct response from cellular module. | 
| ---- | ---- | 
| @return&nbsp; | RUI_RETURN_STATUS | 
| @param | uint8_t *response:&nbsp;the response of server string | 
|  | uint32_t len: response data length&nbsp; | 
|  | uint32_ t timeout: the time to wait for response until timeout | 
| @module | RAK8212-M and RAK5010 core module. | 


