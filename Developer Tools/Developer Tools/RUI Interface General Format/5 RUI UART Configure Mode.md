---
type: page
title: RUI UART Configure Mode
listed: true
slug: rui-uart-configure-mode
---published

$plugin[{
    "type": "code-block",
    "data": {
        "languageBlocks": [
            {
                "code": "RUI_RETURN_STATUS rui_uart_mode_config(RUI_UART_DEF uart_def,RUI_UART_MODE uart_mode);",
                "language": "c"
            }
        ]
    }
}]$

| @brief | This API is used to<br>configure uart work mode. | 
| ---- | ---- | 
| @return | RUI_RETURN_STATUS | 
| @param | RUI_UART_DEF&nbsp;&nbsp;uart_def:&nbsp;the instance of UART.RUI_UART_MODE<br>uart_mode:&nbsp;value for RUI_UART_NORMAL, RUI_UART_UNVARNISHED.&nbsp; | 
| @module | RAK811, RAK4200, RAK4400, RAK4600, and RAK5010. | 


