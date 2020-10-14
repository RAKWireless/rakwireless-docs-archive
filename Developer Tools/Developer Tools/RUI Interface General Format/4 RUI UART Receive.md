---
type: page
title: RUI UART Receive
listed: true
slug: rui-uart-receive
---published

$plugin[{
    "type": "code-block",
    "data": {
        "languageBlocks": [
            {
                "code": "void rui_uart_recv(RUI_UART_DEF uart_def, uint8_t *pdata, uint16_t len)",
                "language": "c"
            }
        ]
    }
}]$

| @brief | This API is used to receive data from UART. | 
| ---- | ---- | 
| @return | NULL | 
| @param | RUI_UART_DEF&nbsp;uart_def&nbsp; : the instance of UART.uint8_t *pdata : the pointer of data.uint16_t len : the length of data. This value is always 1. | 
| @module | RAK811, RAK4200, RAK4400, RAK4600, and RAK5010. | 


