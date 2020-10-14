---
type: page
title: RUI GPIO Interrupt
listed: true
slug: rui-gpio-interrupt
---published

$plugin[{
    "type": "code-block",
    "data": {
        "languageBlocks": [
            {
                "code": "typedef void (*interrupt_callback)(void);\nRUI_RETURN_STATUS rui_gpio_interrupt(bool control, RUI_GPIO_ST st, RUI_GPIO_INTERRUPT_EDGE edge, RUI_GPIO_INTERRUPT_PRIORITY pro,calback callback);",
                "language": "c"
            }
        ]
    }
}]$

| @brief | This API is used to register external GPIO, it may lead to power current&nbsp;increase. e.g 130 µA in Nordic platform. | 
| ---- | ---- | 
| @return | RUI_RETURN_STATUS | 
| @param | bool control: true or false, use it or not.<br><br>RUI_GPIO_ST&nbsp;st: GPIO struct<br><br>                RUI_GPIO_INTERRUPT_EDGE edge: detect in raise or fall<br><br>                RUI_GPIO_INTERRUPT_PRIORITY pro: priority for interruptcalback callback: interrupt callback. | 
| @module | RAK811, RAK4200, RAK4400, RAK4600, RAK5010 and RAK8212-M. | 


