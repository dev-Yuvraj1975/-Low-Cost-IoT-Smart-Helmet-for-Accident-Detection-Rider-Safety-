# -Low-Cost-IoT-Smart-Helmet-for-Accident-Detection-Rider-Safety-
ESP32-based smart helmet prototype for sensor-based crash detection and Bluetooth alerts.

# Smart Helmet Safety System

An ESP32-based smart helmet prototype designed to explore sensor-based crash detection and Bluetooth alert communication.

## Project Overview

This project uses an ESP32 microcontroller and an MPU6050 inertial measurement unit (IMU) to monitor acceleration and orientation. The prototype explores detecting potential crash events using motion and tilt information and communicating alerts over Bluetooth Low Energy (BLE).

## Hardware Components

- ESP32 development board
- MPU6050 accelerometer and gyroscope
- Breadboard and jumper wires
- Push button for cancellation or reset functionality

## Technologies Used

- Embedded C/C++
- Arduino IDE
- ESP32
- I2C communication
- Bluetooth Low Energy (BLE)

## Key Features

- Reads motion and orientation data from the MPU6050
- Uses motion thresholds to identify potential crash events
- Supports Bluetooth Low Energy communication
- Includes a button-based cancellation/reset concept

## Current Status

Prototype under development. Features and detection thresholds require testing and validation under controlled conditions.

## Future Improvements

- Improve crash-detection reliability
- Add power-efficient operation
- Integrate GPS/GSM-based emergency notifications
- Conduct further testing to reduce false alerts

## Disclaimer

This is an educational prototype and is not a certified safety device. It should not be relied upon as a substitute for a certified protective helmet or emergency-response system.
