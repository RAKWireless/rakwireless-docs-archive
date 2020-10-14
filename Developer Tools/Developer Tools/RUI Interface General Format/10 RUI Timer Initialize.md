---
type: page
title: RUI Timer Initialize
listed: true
slug: rui-timer-init
---published

$plugin[{
    "type": "code-block",
    "data": {
        "languageBlocks": [
            {
                "code": "RUI_RETURN_STATUS rui_timer_init(void *obj, void ( *callback )( void ));",
                "language": "c"
            }
        ]
    }
}]$

| @brief&nbsp; &nbsp; &nbsp;&nbsp; | This API is used to create/initialize a timer. | 
| ---- | ---- | 
| @return | RUI_RETURN_STATUS | 
| @param | void *obj : timer instancevoid (*callback)(void): timer event callback function | 
| @module | RAK811, RAK4200, RAK4400, RAK4600, RAK5010 and RAK8212-M. | 


