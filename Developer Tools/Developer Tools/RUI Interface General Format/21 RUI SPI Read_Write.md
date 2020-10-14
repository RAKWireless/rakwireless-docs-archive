---
type: page
title: RUI SPI Read/Write
listed: true
slug: rui-spi-read-write
---published

$plugin[{
    "type": "code-block",
    "data": {
        "languageBlocks": [
            {
                "code": "RUI_RETURN_STATUS rui_spi_rw(RUI_IF_READ_WRITE rw, uint8_t *tx, uint16_t tx_len, uint8_t *rx, uint16_t rx_len);",
                "language": "c"
            }
        ]
    }
}]$

| @brief | This API is used to<br>read/write through SPI. | 
| ---- | ---- | 
| @return | RUI_RETURN_STATUS | 
| @param | RUI_IF_READ_WRITE&nbsp;rw:      read or write through SPI.&nbsp;uint8_t *tx: write through SPI.uint16_t tx_len: TX lengthuint8_t *rx: read buffer.&nbsp;uint16_t rx_len: RX length. | 
| @module | RAK4400, RAK4600 and RAK5010. | 


