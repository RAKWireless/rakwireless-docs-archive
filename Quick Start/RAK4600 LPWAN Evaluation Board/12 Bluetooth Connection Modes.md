---
type: page
title: Bluetooth Connection Modes
listed: true
slug: bluetooth-connection-modes
---published

There are three BLE modes in RAK4600 from the firmware V3.0.0.6 on, the **Peripheral Mode**, the **Central Mode** and the **Beacon Scan Mode**. You can change the work mode of RAK4600’s BLE using this command provided below which is defined in this [auto$](/rak4600-lora-evaluation-board/at-commands-for-rak4600) 

$plugin[{
    "type": "code-block",
    "data": {
        "languageBlocks": [
            {
                "code": "at+set_config=ble:work_mode:X:Y",
                "language": "none"
            }
        ]
    }
}]$

**Description:** Set the work mode for BLE.

**X** - 0: BLE peripheral mode, 1: BLE central mode. 2: Beacon scan mode.

**Y** - 0: normal range, 1: BLE long range.

### BLE Peripheral Mode

For the Peripheral Mode, you can scan RAK4600’s BLE and connect with it using your mobile device.

### BLE Central Mode

For the Central Mode, RAK4600’s BLE will not broadcast so that your mobile devices will not be able to scan it.  This is very useful if you want to make the RAK4600 act as a BLE Gateway wherein BLE Sensor Nodes (up to 20 Devices) can send sensor data.

### Beacon Scan Mode

For the Beacon Scan mode, RAK4600 can scan around the Beacon signal, it is useful for Beacon use case like iBeacon.

## RAK4600 BLE Default Settings

By default, the RAK4600 LPWAN Evaluation Board will work on **Peripheral Mode.** In this mode users can configure it through BLE including DFU easily. It should be noted that after resetting the RAK4600, the user has only 60 seconds to establish a connection with your Mobile Device through BLE based on its power consumption settings. If no connection has been established within 60 seconds, the RAK4600's BLE signal will not be broadcasted and it will enter power saving mode. On the other hand, there is no limitation once you are already connected with the RAK4600's BLE.

If you set the RAK4600 to work in Central Mode, the RAK4600 will work first on Peripheral Mode for 30 seconds and if no connection is established after 30 seconds, it will automatically work in **Central Mode.** In this mode,the BLE signal of the RAK4600 will stop broadcasting and will not be visible on your mobile devices up until you change the work mode to peripheral mode or reset the RAK4600 again.

