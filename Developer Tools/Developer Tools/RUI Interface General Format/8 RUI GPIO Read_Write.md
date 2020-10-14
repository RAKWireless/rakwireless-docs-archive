---
type: page
title: RUI GPIO Read/Write
listed: true
slug: rui-gpio-read-write
---published

$plugin[{
    "type": "code-block",
    "data": {
        "languageBlocks": [
            {
                "code": "RUI_RETURN_STATUS rui_gpio_rw(RUI_IF_READ_WRITE rw_status,RUI_GPIO_ST *rui_gpio,uint8_t* status);",
                "language": "c"
            }
        ]
    }
}]$

| @brief | This API is used to read or set a certain GPIO's Status. | 
| ---- | ---- | 
| @return | RUI_RETURN_STATUS | 
| @param | RUI_IF_READ_WRITE rw:&nbsp; &nbsp; read or set.RUI_GPIO_ST&nbsp;*rui_gpio:&nbsp; &nbsp; &nbsp;the pin number of the GPIO which you want to read or set.uint8_t* status: the pointer of GPIO Value. &nbsp;0 : low level, 1: high Level. | 
| @module | RAK811, RAK4200, RAK4400, RAK4600, RAK5010 and RAK8212-M. | 


