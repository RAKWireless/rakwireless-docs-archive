---
type: page
title: RUI Cellular Set Operator
listed: true
slug: rui-cellular-set-operator
---published

$plugin[{
    "type": "code-block",
    "data": {
        "languageBlocks": [
            {
                "code": "RUI_RETURN_STATUS rui_cellular_set_operator(uint8_t *APN,uint8_t *operator_long_name,uint8_t *operator_short_name,uint8_t operator_net)",
                "language": "c"
            }
        ]
    }
}]$

| @brief | &nbsp;This API is used to configure parameters of Cellular operator. | 
| ---- | ---- | 
| @return | RUI_RETURN_STATUS | 
| @param | uint8_t *APN&nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp;:&nbsp;The APN name of Cellular operatoruint8_t *operator_long_name&nbsp; &nbsp; : The operator’s long name. For example: “CHINAMOBILE”.uint8_t *operator_short_name&nbsp; : The operator's short name. For example, "CMCC"uint8_t operator_net&nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; : The cellular network type. | 
| @module | RAK8212-M and RAK5010 core module. | 


