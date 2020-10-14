---
type: page
title: RUI AT Response
listed: true
slug: rui-at-response
---published

$plugin[{
    "type": "code-block",
    "data": {
        "languageBlocks": [
            {
                "code": "void  rui_at_response(bool is_success, uint8_t *p_msg, uint16_t ret_code);",
                "language": "c"
            }
        ]
    }
}]$

| @brief | This API is used to return info for user defined AT, so that application can use their AT. | 
| ---- | ---- | 
| @return | void | 
| @param | bool is_success: true or false<br><br>                    uint8_t *p_msg: user message<br><br>                    uint16_t ret_code:user error code | 
| @module | RAK811, RAK4200, RAK4400, RAK4600, RAK5010 and RAK8212-M. | 


