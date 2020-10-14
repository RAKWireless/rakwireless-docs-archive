---
type: page
title: RUI Sensor General Format
listed: true
slug: rui-sensor-general-format
---published

## General Format

### GGAData

$plugin[{
    "type": "code-block",
    "data": {
        "languageBlocks": [
            {
                "code": "typedef struct GGAData\n{\n\tuint8_t UTC[4];\n\tuint8_t Date[3];\n\tbool LatitudeNS;      \t\t\/\/0:N1:S\n\tuint8_t LatitudeDegree;\n\tuint32_t LatitudeMinute;\n\tdouble Latitude;\n\tbool LongitudaEW;\t\t\t\/\/0:E1:W\n\tuint8_t LongitudaDegree;\n\tdouble Longitude;\n\tuint32_t LongitudaMinute;\n\tint Quality;\n\tint NumSatellities;\n\tint16_t HDOP;\n\tint16_t Altitude;\n\tint16_t GeoidHeight;\n}RUI_GGA_Data;",
                "language": "c"
            }
        ]
    }
}]$

