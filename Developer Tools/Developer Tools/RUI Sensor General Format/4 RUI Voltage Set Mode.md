---
type: page
title: RUI Voltage Set Mode
listed: false
slug: rui-voltage-set-mode
---published

$plugin[{
    "type": "code-block",
    "data": {
        "languageBlocks": [
            {
                "code": "RUI_RETURN_STATUS rui_voltage_set_mode(DRIVER_MODE mode)",
                "language": "c"
            }
        ]
    }
}]$

| @brief&nbsp;&nbsp; | This API is used to set<br>whether to collect the voltage data of the battery. | 
| ---- | ---- | 
| @return | RUI_RETURN_STATUS | 
| @param | DRIVER_MODE mode:    only two modes are valid for this parameter:<br><br>1. RUI_POWER_ON_MODE means it will collect voltage data.<br><br>2. RUI_POWER_OFF_MODE means it won’t collect voltage data. | 
| @module | RAK811,&nbsp; RAK4200,&nbsp; RAK4400 and&nbsp; RAK5010 | 


