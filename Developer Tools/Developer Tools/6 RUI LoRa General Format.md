---
type: page
title: RUI LoRa General Format
listed: true
slug: rui-lora-general-format
---published

## General Format

$plugin[{
    "type": "code-block",
    "data": {
        "languageBlocks": [
            {
                "code": "rui_lora_xxx()",
                "language": "c"
            }
        ]
    }
}]$

## General Definition

### LORA_JOIN_MODE

$plugin[{
    "type": "code-block",
    "data": {
        "languageBlocks": [
            {
                "code": "typedef enum LORA_JOIN_MODE\n{\n\tRUI_OTAA = 0,\n\tRUI_ABP\n}LORA_JOIN_MODE;",
                "language": "c"
            }
        ]
    }
}]$

### LORA_CLASS_MODE

$plugin[{
    "type": "code-block",
    "data": {
        "languageBlocks": [
            {
                "code": "typedef enum LORA_CLASS_MODE\n{\n\tCLASS_A = 0,\n\tCLASS_B,\n\tCLASS_C\n}LORA_CLASS_MODE;",
                "language": "c"
            }
        ]
    }
}]$

### LORA_WORK_MODE

$plugin[{
    "type": "code-block",
    "data": {
        "languageBlocks": [
            {
                "code": "typedef enum LORA_WORK_MODE\n{\n\tRUI_LORAWAN = 0,\n\tRUI_P2P,\n\tRUI_TESTMODE\n}LORA_WORK_MODE;",
                "language": "c"
            }
        ]
    }
}]$

### LORA_REGION

$plugin[{
    "type": "code-block",
    "data": {
        "languageBlocks": [
            {
                "code": "typedef enum LORA_REGION\n{\n\tAS923,\n\tAU915,\n\tCN470,\n\tCN779,\n\tEU433,\n\tEU868,\n\tKR920,\n\tIN865,\n\tUS915,\n\tUS915_Hybrid\n}LORA_REGION;",
                "language": "c"
            }
        ]
    }
}]$

### RUI_LORA_STATUS

$plugin[{
    "type": "code-block",
    "data": {
        "languageBlocks": [
            {
                "code": "typedef struct RUI_LORA_STATUS\n{\n\tuint32_t dev_addr;\n\tuint8_t dev_eui[8];\n\tuint8_t app_eui[8];\n\tuint8_t app_key[16];\n\tuint8_t nwks_key[16];\n\tuint8_t apps_key[16];\n    RUI_LORA_WORK_MODE work_mode;\n    RUI_LORA_CLASS_MODE class_status;\n    RUI_LORA_JOIN_MODE join_mode;\n    uint8_t lora_dr;\n    uint8_t confirm; \n    uint16_t lorasend_interval;\n    uint8_t autosend_status;\n    bool IsJoined;\n    bool AdrEnable;\n    uint8_t region[5]; \/\/region string e.g:\"EU868\"\n}RUI_LORA_STATUS_T;",
                "language": "c"
            }
        ]
    }
}]$

### RUI_LORA_AUTO_SEND_MODE

$plugin[{
    "type": "code-block",
    "data": {
        "languageBlocks": [
            {
                "code": "typedef enum RUI_LORA_AUTO_SEND_MODE\n{\n    RUI_AUTO_DISABLE=0,     \/\/ Disable lora auto send.\n    RUI_AUTO_ENABLE_SLEEP,  \/\/ Enable lora auto send, sleep when the system is idle.\n\tRUI_AUTO_ENABLE_NORMAL  \/\/ Enable lora auto send, runs normally when the system is idle.\n}RUI_LORA_AUTO_SEND_MODE;",
                "language": "c"
            }
        ]
    }
}]$

