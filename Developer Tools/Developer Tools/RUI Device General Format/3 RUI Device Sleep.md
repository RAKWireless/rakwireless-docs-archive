---
type: page
title: RUI Device Sleep
listed: true
slug: rui-device-sleep
---published

$plugin[{
    "type": "code-block",
    "data": {
        "languageBlocks": [
            {
                "code": "typedef void (*sensor_wakeup)(void);\n\ntypedef void (*sensor_sleep)(void);\n\nRUI_RETURN_STATUS rui_sensor_register_callback(sensor_wakeup callback1,sensor_sleep callback2); \n\nRUI_RETURN_STATUS rui_device_sleep(uint32_t on);",
                "language": "c"
            }
        ]
    }
}]$

| @brief | This API is used to set the device to sleep mode. | 
| ---- | ---- | 
| @return | NULL | 
| @param | uint32_t on/off: on/off<br><br>                sensor_wakeup, sensor_sleep: app callback, user can add sensor operation here to finish function and power control | 
| @module | RAK811, RAK4200, RAK8212-M, RAK5010, 4400 and RAK4600 core module | 


