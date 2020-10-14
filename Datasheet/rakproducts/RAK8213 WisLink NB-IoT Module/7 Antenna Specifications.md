---
type: page
title: Antenna Specifications
listed: true
slug: antenna-specifications-rak8213
---published

### Interfaces

| **Interface Name** | **Reference** | **I/O** | **Description** | **Comment** | 
| ---- | ---- | ---- | ---- | ---- | 
| ANT_MAIN | J1 | IO | Cellular antenna interface | 50Ω characteristic impedance | 
| ANT_GNSS | J2 | AI | GNSS antenna connector | 50Ω characteristic impedance | 


### Antenna Requirements

| **Antenna Type** | **Requirements** | 
| ---- | ---- | 
| GNSS _(1)_ | - **Frequency range**: 1559MHz ~1609MHz<br>- **Polarization**: RHCP or linear<br>- **VSWR**: < 2 (Typical)<br>- **Passive antenna gain**: > 0dBi<br>- **Active antenna noise figure**: < 1.5dB<br>- **Active antenna gain**: > 0dBi<br>- **Active antenna embedded LNA gain**: < 17dB | 
| LTE/GSM | - **VSWR**: ≤ 2<br>- **Efficiency**: > 30% <br>- **Max Input Power**: 50 W<br>- **Input Impedance**: 50Ω<br>- **Cable Insertion Loss**: < 1dB (LTE B5/B8/B12/B13/B18/B19/B20/B26/B28, GSM850/EGSM900)<br>- **Cable Insertion Loss**: < 1.5dB (LTE B1/B2/B3/B4/B25/B39, DCS1800/PCS1900) | 


$plugin[{
    "type": "callout",
    "data": {
        "text": "_(1)_ It is recommended to use a passive GNSS antenna when LTE B13 or B14 is     used as the use of active antenna may generate harmonics which will affect the     GNSS performance.",
        "type": "info",
        "title": "Note"
    }
}]$

