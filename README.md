# Fail Safe CAN OTA Firmware Engine

## Overview
The Fail Safe CAN OTA Firmware Engine is an embedded firmware update framework designed for safety-critical and automotive-grade systems using the CAN (Controller Area Network) protocol.

The system enables reliable Over-The-Air (OTA) firmware updates between two STM32 microcontrollers while ensuring system stability, data integrity, and rollback safety in the presence of power loss, communication errors, or corrupted firmware.

## Key Features
- CAN-based OTA firmware update mechanism
- Bootloader and application separation
- Dual-partition / rollback-safe firmware design
- CRC-based firmware integrity validation
- Power-failure and interruption recovery
- Flash memory protection and version control
- CAN error handling and retransmission logic
- Automotive and safety-critical design approach

## System Architecture
- **Controller Node**: Sends firmware over CAN
- **Target Node**: Receives firmware via bootloader
- **Bootloader**:
  - Validates firmware integrity
  - Handles rollback on failure
  - Safely jumps to application
- **Application**:
  - Normal system operation
  - Sensor data (vibration) transmission

## Technologies Used
- STM32 Microcontrollers
- CAN Protocol
- Embedded C
- Bootloader Architecture
- Flash Memory Management
- CRC / Integrity Checks
- Linker Scripts
- Git & GitHub

## Use Case
- Automotive ECUs
- Industrial controllers
- Remote firmware update systems
- Safety-critical embedded devices

## How OTA Works
1. Bootloader enters OTA mode
2. Firmware is transferred via CAN frames
3. Firmware stored in secondary flash partition
4. CRC verification performed
5. If valid → firmware activated
6. If failure → rollback to previous version

## Author
**Lovzy**
