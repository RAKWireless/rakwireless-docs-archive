---
type: page
title: RUI UART Initialize
listed: true
slug: rui-uart-initialize
---published

$plugin[{
    "type": "code-block",
    "data": {
        "languageBlocks": [
            {
                "code": "RUI_RETURN_STATUS rui_uart_init(RUI_UART_DEF uart_def,RUI_UART_BAUDRATE baudrate);",
                "language": "c"
            }
        ]
    }
}]$

| @brief | This API is used to<br>configure the parameters for UART. | 
| ---- | ---- | 
| @return | RUI_RETURN_STATUS | 
| @param | RUI_UART_DEF uart_def:the instance of UART.<br><br>                RUI_UART_BAUDRATE baudrate: UART baudrate value | 
| @module | RAK811, RAK4200, RAK4400, RAK4600, and RAK5010. | 


