---
type: page
title: RUI LoRa P2P Config
listed: true
slug: rui-lora-p2p-config
---published

$plugin[{
    "type": "code-block",
    "data": {
        "languageBlocks": [
            {
                "code": "RUI_RETURN_STATUS rui_lorap2p_config(uint32_t Frequency,uint8_t  Spreadfact,uint8_t  Bandwidth,uint8_t  Codingrate,uint16_t  Preamlen,uint8_t  Powerdbm);",
                "language": "c"
            }
        ]
    }
}]$

| @brief | This API is used to config LoRaP2P parameters. | 
| ---- | ---- | 
| @return | RUI_RETURN_STATUS | 
| @param | Frequency:      Frequency<br>in Hz | 
|  | Spreadfact:  Spreadfactare limite to the 6-12 range | 
|  | Bandwidth:       Bandwidth<br>limite to the 0-2 range | 
|  | Codingrate:  Codingrate limite to the 1-4 range | 
|  | Preamlen:    Preamlen limite to the 2-66535 range | 
|  | Powerdbm:  Powerdbm limite to the 0-20 range. | 
| @module | RAK811, RAK4200, and RAK4600 core module. | 


