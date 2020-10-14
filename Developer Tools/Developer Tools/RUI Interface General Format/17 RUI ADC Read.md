---
type: page
title: RUI ADC Read
listed: true
slug: rui-adc-read
---published

$plugin[{
    "type": "code-block",
    "data": {
        "languageBlocks": [
            {
                "code": "RUI_RETURN_STATUS rui_adc_get(RUI_GPIO_ST *rui_gpio, uint16_t* value);",
                "language": "c"
            }
        ]
    }
}]$

| @brief | This API is used to read the value of the ADC Pin | 
| ---- | ---- | 
| @return | RUI_RETURN_STATUS | 
| @param | uint8_t* value: the value which is read from ADC.RUI_GPIO_ST&nbsp;*rui_gpio<br>: GPIO struct | 
| @module | RAK811, RAK4200, RAK4400, RAK4600, RAK5010 and RAK8212-M. | 


