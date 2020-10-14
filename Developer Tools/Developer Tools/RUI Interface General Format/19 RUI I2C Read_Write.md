---
type: page
title: RUI I2C Read/Write
listed: true
slug: rui-i2c-read-write
---published

$plugin[{
    "type": "code-block",
    "data": {
        "languageBlocks": [
            {
                "code": "RUI_RETURN_STATUS rui_i2c_rw(RUI_I2C_ST *rui_i2c, uint8_t devAddr, uint16_t regAddr, uint8_t* data, uint16_t len)",
                "language": "c"
            }
        ]
    }
}]$

| **@brief** | This API is used to Read/Write Through I2C. | 
| ---- | ---- | 
| **@return** | [RUI_RETURN_STATUS](https://doc.rakwireless.com/developer-tools/developer-tools/getting-started#rui_return_status) | 
| **@param** | RUI_I2C_ST *rui_i2c: init parameters struct.<br>uint8_t devAddr:  device address in HEX Format.<br>uint16_t regAddr:  the sensor's register address in HEX Format.  <br>uint8_t *data:  the data output or data to be written through I2C.<br>uint16_t len :  the data length in byte. | 
| **@module** | RAK811, RAK4200, RAK4400, RAK4600, and RAK5010. | 


