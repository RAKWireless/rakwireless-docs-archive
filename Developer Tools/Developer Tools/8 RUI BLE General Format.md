---
type: page
title: RUI BLE General Format
listed: true
slug: rui-ble-general-format
---published

## General Format

$plugin[{
    "type": "code-block",
    "data": {
        "languageBlocks": [
            {
                "code": "rui_ble_xxx()",
                "language": "c"
            }
        ]
    }
}]$

## General Definition

### BLE_CLIENT_EVT_TYPE

$plugin[{
    "type": "code-block",
    "data": {
        "languageBlocks": [
            {
                "code": "typedef enum\n{\n\tBLE_CLIENT_EVT_DISCOVERY_COMPLETE = 1,\n\tBLE_CLIENT_EVT_NOTIFICATION,\n\tBLE_CLIENT_EVT_READ\n}BLE_CLIENT_EVT_TYPE;",
                "language": "c"
            }
        ]
    }
}]$

### BLE_DATA

$plugin[{
    "type": "code-block",
    "data": {
        "languageBlocks": [
            {
                "code": "typedef struct\n{\n\tuint8_t \t*p_data;\n\tuint16_t \tlen;\n}BLE_DATA;",
                "language": "c"
            }
        ]
    }
}]$

### BLE_HANDLE

$plugin[{
    "type": "code-block",
    "data": {
        "languageBlocks": [
            {
                "code": "typedef struct\n{\n\tuint16_t write_handle;\n\tuint16_t read_notify_handle;\n\tuint16_t notify_cccd_handle;\n}BLE_HANDLE;",
                "language": "c"
            }
        ]
    }
}]$

### BLE_CLIENT_EVT

$plugin[{
    "type": "code-block",
    "data": {
        "languageBlocks": [
            {
                "code": "typedef struct\n{\n\tBLE_CLIENT_EVT_TYPE\t\tevt_type;\n\tuint16_t conn_handle;\n\tunion\n\t{\n\t\tBLE_DATA \tdata;\n\t\tBLE_HANDLE \tpeer_db;\n\t}params;\n}BLE_CLIENT_EVT;",
                "language": "c"
            }
        ]
    }
}]$

### BLE_CLIENT_EVT_HANDLER

$plugin[{
    "type": "code-block",
    "data": {
        "languageBlocks": [
            {
                "code": "typedef void (* BLE_CLIENT_EVT_HANDLER) (BLE_CLIENT * p_ble_rcs_c, BLE_CLIENT_EVT * p_evt);",
                "language": "c"
            }
        ]
    }
}]$

### BLE_CLIENT

$plugin[{
    "type": "code-block",
    "data": {
        "languageBlocks": [
            {
                "code": "\/**@brief Rak Custom Service Client structure. *\/\nstruct BLE_CLIENT\n{\n\tuint16_t \tconnect_handle;\n\tHANDLE_LIST \tpeer_list;\n\tBLE_CLIENT_EVT_HANDLER\tevt_handler;\n\tuint8_t uuid_type;\n};",
                "language": "c"
            }
        ]
    }
}]$

