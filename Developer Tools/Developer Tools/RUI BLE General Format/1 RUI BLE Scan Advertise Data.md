---
type: page
title: RUI BLE Scan Advertise Data
listed: true
slug: rui-ble-scan-advertise-data
---published

$plugin[{
    "type": "code-block",
    "data": {
        "languageBlocks": [
            {
                "code": "void rui_ble_scan_adv(int8_t rssi_value, uint8_t *p_adv_data, uint16_t adv_data_len, uint8_t *p_device_mac)",
                "language": "c"
            }
        ]
    }
}]$

| @brief | This API is used to scan all around BLE devices and&nbsp;valid when the BLE works on master mode. | 
| ---- | ---- | 
| @return | NULL | 
| @param | int8_t&nbsp; rssi_value:&nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp;peripheral rssi valueuint8_t&nbsp; *p _adv_data:&nbsp;&nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; the advertise datauint16_t&nbsp; adv_data_len:&nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp;the length of advertise datauint8_t&nbsp; *p_device_mac:&nbsp; &nbsp; &nbsp; &nbsp; &nbsp; the peripheral's MAC address | 
| @module | RAK8212-M, RAK5010, and RAK4600 core module. | 


