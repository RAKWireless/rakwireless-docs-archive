---
type: page
title: RUI BLE Send Data Write
listed: true
slug: rui-ble-send-written-data
---published

$plugin[{
    "type": "code-block",
    "data": {
        "languageBlocks": [
            {
                "code": "RUI_RETURN_STATUS rui_ble_tx_data_write(BLE_CLIENT * p_ble_rcs_c, uint8_t *pdata, uint16_t len)",
                "language": "c"
            }
        ]
    }
}]$

| @brief | This API is used to write data to another BLE device through BLE. | 
| ---- | ---- | 
| @return | RUI_RETURN_STATUS | 
| @param | BLE_CLIENT&nbsp; *p_ble_rcs_c:&nbsp;&nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; The BLE client instance.uint8_t&nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp;*pdata:&nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp;The data which will be sent.uint16_t&nbsp; &nbsp; &nbsp; &nbsp; &nbsp;len:&nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; The length of data. | 
| @module | RAK8212-M, RAK5010, and RAK4600 core module | 


