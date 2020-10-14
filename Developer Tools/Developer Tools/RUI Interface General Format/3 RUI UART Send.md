---
type: page
title: RUI UART Send
listed: true
slug: rui-uart-send
---published

$plugin[{
    "type": "code-block",
    "data": {
        "languageBlocks": [
            {
                "code": "RUI_RETURN_STATUS rui_uart_send(RUI_UART_DEF uart_def, uint8_t *pdata, uint16_t len)",
                "language": "c"
            }
        ]
    }
}]$

| @brief | This API is used to send data via UART. | 
| ---- | ---- | 
| @return | RUI_RETURN_STATUS | 
| @param | RUI_UART_DEF&nbsp;uart_def : the instance of UART.uint8t *pdata : the pointer of data you want to send.uint16_t len :  the length of the data. | 
| @module | RAK811, RAK4200, RAK4400, RAK4600, and RAK5010. | 


