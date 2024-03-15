
# Project Title: STM32 Gyro LED Control

## Introduction
This project aims to control the onboard LEDs of an STM32 board based on the roll and pitch angles obtained from gyroscopic data. The system consists of two main components: a Python script running on a Jetson Nano to process gyro data and send LED control commands, and firmware running on the STM32 board to receive commands and control the LEDs accordingly.

## Overview
The project utilizes serial communication between the Jetson Nano and the STM32 board to exchange data and commands. The Python script requests gyro data from the STM32 board, processes it to determine roll and pitch angles, and sends LED control commands back to the STM32 board. The STM32 firmware receives these commands and sets the appropriate LEDs.

### Block Diagram:
```
                    +-----------------+
                    |   Jetson Nano   |
                    | Python Script   |
                    +-----------------+
                            |
                            | Serial
                            |
                    +-----------------+
                    |   STM32 Board   |
                    |     Firmware    |
                    +-----------------+
```

## Instructions
To run the code:
1. Connect the Jetson Nano and the STM32 board via USB.
2. Upload the provided STM32 firmware to the board.
3. Run the Python script on the Jetson Nano.

## Dependencies
- [Link to STM32 firmware](github.com/your-stm32-firmware)
- Python 3
- PySerial library (install via `pip install pyserial`)

## Table of Contents
1. `python_script.py`: Python script running on the Jetson Nano to process gyro data and control LEDs.
2. `stm32_firmware.ino`: Firmware for the STM32 board to receive LED control commands and set LEDs accordingly.

## Credits
- PySerial library: [https://github.com/pyserial/pyserial](https://github.com/pyserial/pyserial)
