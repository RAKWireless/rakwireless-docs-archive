---
type: page
title: RUI BLE Event Register Callback
listed: true
slug: rui-ble-event-register-callback
---published

$plugin[{
    "type": "code-block",
    "data": {
        "languageBlocks": [
            {
                "code": "typedef void (*ble_evt_connect)(void);\ntypedef void (*ble_evt_disconnect)(void);\nuint32_t rui_ble_evt_register_callback(ble_evt_connect callback1, ble_evt_disconnect callback2);",
                "language": "c"
            }
        ]
    }
}]$

| @brief | This API is used to<br>register ble event callback functions. | 
| ---- | ---- | 
| @return | RUI_RETURN_STATUS | 
| @param | ble_evt_connect:    the callback function for ble connected<br>event. | 
|  | ble_evt_disconnect: the<br>callback function for ble disconnected event. | 
| @module | RAK5010          <br>RAK8212(M)  RAK4600         RAK4400 | 


