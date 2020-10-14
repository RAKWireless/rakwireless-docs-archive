---
type: page
title: RUI Flash Read
listed: true
slug: rui-flash-read
---published

$plugin[{
    "type": "code-block",
    "data": {
        "languageBlocks": [
            {
                "code": "RUI_RETURN_STATUS rui_flash_read(RUI_FLASH_MODE mode,uint8_t *str, uint8_t len);",
                "language": "c"
            }
        ]
    }
}]$

| @brief | This API is auto send data<br>timeout callback by LoRa. | 
| ---- | ---- | 
| @return | RUI_RETURN_STATUS | 
| @param | uint8_t *str<br><br>                    uint8_t len: should less than 128 byte<br><br>                    RUI_FLASH_MODE mode: user data or origin data | 
| @module | RAK811, RAK4200, RAK4400, RAK4600, RAK5010 and RAK8212-M. | 


