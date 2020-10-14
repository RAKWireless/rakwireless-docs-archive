---
type: page
title: RUI BLE Set Work Mode
listed: true
slug: rui-ble-set-work-mode
---published

$plugin[{
    "type": "code-block",
    "data": {
        "languageBlocks": [
            {
                "code": "RUI_RETURN_STATUS rui_ble_set_work_mode(BLE_WORK_MODE mode, bool long_range_enable);",
                "language": "c"
            }
        ]
    }
}]$

| @brief | This API is used to set the<br>work mode of BLE | 
| ---- | ---- | 
| @return | RUI_RETURN_STATUS | 
| @param | BLE_WORK_MODE mode:  BLE_MODE_PERIPHERAL, BLE_MODE_CENTRAL,<br>BLE_MODE_OBSERVER | 
|  | long_range_enable: true or<br>false | 
| @module | RAK5010          <br>RAK8212(M)  RAK4600         RAK4400 | 


