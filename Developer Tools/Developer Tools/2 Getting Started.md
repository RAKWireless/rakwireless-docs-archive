---
type: page
title: Getting Started
listed: true
slug: getting-started
---published

Welcome to the Official Rakwireless Unified Interface (RUI) API. Our API for easy platform integration for your business. You can easily build an IoT Software for your custom hardware IoT blocks in just few minutes!

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1566310796\/18765\/piopsq3luadbo6ysug2v.jpg",
        "mode": "600",
        "width": 3901,
        "height": 3751,
        "caption": null
    }
}]$

### Document Guide

In each API, there are 4 sections under it namely: 

1. **@brief** - Description on what is the function of that specific API.
2. **@return** - Expected Return Value.
3. **@param** - Accepted Parameters of that API.
4. **@support** - Supported Hardware.

## Global Definition

### RUI_RETURN_STATUS

$plugin[{
    "type": "code-block",
    "data": {
        "languageBlocks": [
            {
                "code": "\/* RUI API return value*\/\n\ntypedef enum{\n\tRUI_STATUS_OK=0,\n \tRUI_STATUS_PARAMETER_INVALID,\n \tRUI_STATUS_RW_FLASH_ERROR\n \tRUI_STATUS_GPIO_IRQ_DISABLE,\n \tRUI_STATUS_BUS_INIT_FAIL,\n\tRUI_STATUS_TIMER_FAIL,\n\tRUI_STATUS_IIC_RW_ERROR,\n \tRUI_STATUS_UART_SEND_ERROR,\n \tRUI_SENSOR_STATUS_OK=20,\n \tRUI_BLE_STATUS_OK=40,\n \tRUI_BLE_ERROR_INVALID_STATE=41,\n\tRUI_CELLULAR_STATUS_OK=60,\n \tRUI_LORA_STATUS_BUSY=80,\n \tRUI_LORA_STATUS_SERVICE_UNKNOWN,\n \tRUI_LORA_STATUS_PARAMETER_INVALID,\n \tRUI_LORA_STATUS_FREQUENCY_INVALID,\n \tRUI_LORA_STATUS_DATARATE_INVALID,\n \tRUI_LORA_STATUS_FREQ_AND_DR_INVALID,\n \tRUI_LORA_STATUS_NO_NETWORK_JOINED,\n \tRUI_LORA_STATUS_LENGTH_ERROR,\n \tRUI_LORA_STATUS_DEVICE_OFF,\n \tRUI_LORA_STATUS_REGION_NOT_SUPPORTED,\n \tRUI_LORA_STATUS_DUTYCYCLE_RESTRICTED,\n \tRUI_LORA_STATUS_NO_CHANNEL_FOUND,\n \tRUI_LORA_STATUS_NO_FREE_CHANNEL_FOUND\n}RUI_RETURN_STATUS;",
                "language": "c"
            }
        ]
    }
}]$

### DRIVER_MODE

$plugin[{
    "type": "code-block",
    "data": {
        "languageBlocks": [
            {
                "code": "typedef enum DRIVER_MODE {\n\tRUI_NORMAL_MODE = 0,\n\tRUI_POWER_ON_MODE,\n\tRUI_POWER_OFF_MODE,\n\tRUI_SLEEP_MODE,\n\tRUI_STANDBY_MODE\n}DRIVER_MODE;",
                "language": "c"
            }
        ]
    }
}]$

