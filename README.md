# -Low-Cost-IoT-Smart-Helmet-for-Accident-Detection-Rider-Safety-
ESP32-based smart helmet prototype for sensor-based crash detection and Bluetooth alerts.

# Smart Helmet — Intelligent Crash Detection & Emergency Alert System

An ESP32-based smart helmet prototype designed to detect potential motorcycle crashes using an MPU6050 accelerometer and gyroscope, analyse motion patterns, and initiate emergency communication through Bluetooth Low Energy (BLE).

## Overview

Road accidents may go unnoticed when a rider is unconscious or unable to call for help. This project explores a low-cost embedded system that monitors helmet motion and identifies potential crash events.

The prototype uses sensor data and a multi-stage detection approach to help distinguish potential crashes from ordinary movement. When a crash event is confirmed by the implemented logic, the system can communicate with a connected mobile application.

**Project status:** MVP / Prototype under development

## Key Features

- **Motion sensing:** Collects acceleration and angular velocity data using the MPU6050 IMU.
- **Crash detection:** Analyses motion data using threshold-based conditions.
- **False-positive reduction:** Designed to distinguish potential crashes from ordinary movements and sudden impacts.
- **ESP32 processing:** Processes sensor data and controls the detection workflow.
- **BLE communication:** Supports communication between the ESP32 and a connected mobile application.
- **Alert cancellation/reset:** Provides a mechanism to cancel or reset the alert workflow.
- **Expandable architecture:** Can be extended with GSM-based alerts, improved helmet-worn verification, and power-management features.

## Hardware Components

| Component | Purpose |
|---|---|
| ESP32 development board | Main controller and BLE communication |
| MPU6050 | Measures acceleration and angular velocity |
| Push button | User input for cancellation/reset |
| Breadboard and jumper wires | Prototype connections |
| Power supply | Powers the prototype |
| Mobile phone | BLE communication and application testing |

*Include only components that are actually used in your current prototype.*

## Software and Technologies

- **Programming language:** C/C++
- **Development environment:** Arduino IDE
- **Microcontroller platform:** ESP32
- **Sensor interface:** I²C
- **Wireless communication:** Bluetooth Low Energy (BLE)
- **Sensor:** MPU6050 accelerometer and gyroscope

## System Architecture

1. The MPU6050 measures the helmet's acceleration and angular velocity.
2. The ESP32 reads the sensor data.
3. The crash-detection logic checks for motion patterns that may indicate a potential crash.
4. The system evaluates the relevant confirmation conditions implemented in the firmware.
5. When the event satisfies the implemented logic, the system initiates the alert workflow.
6. The ESP32 communicates with the connected mobile application over BLE.
7. The user can use the supported cancellation/reset mechanism.

## Crash Detection Algorithm

The prototype follows a rule-based approach to potential crash detection.

- **Step 1 — Sensor acquisition:** Read accelerometer and gyroscope measurements.
- **Step 2 — Impact detection:** Check whether acceleration crosses the configured threshold.
- **Step 3 — Event validation:** Evaluate the additional motion or confirmation conditions implemented in the firmware.
- **Step 4 — Alert handling:** Initiate the alert workflow when the required conditions are satisfied.
- **Step 5 — Reset/cancellation:** Allow the supported reset or cancellation action.

The thresholds and confirmation rules should be documented alongside the actual firmware. They must be validated experimentally before making claims about detection accuracy.

## Hardware Connections

| MPU6050 | ESP32 |
|---|---|
| SDA | GPIO 21 |
| SCL | GPIO 22 |
| VCC | According to the module's supported voltage |
| GND | GND |

**Additional inputs:** The push button is configured on GPIO 25 in the current wiring plan. Verify the final firmware and physical connections before using this table as a definitive wiring guide.

## Getting Started

### Prerequisites

- Arduino IDE
- ESP32 board support package
- ESP32 development board
- MPU6050 module
- USB data cable
- Required sensor libraries used by the firmware

### Setup

1. Clone or download this repository.
2. Open the Arduino sketch (`.ino`) in Arduino IDE.
3. Install the required libraries if they are not already installed.
4. Select the appropriate ESP32 board and COM port.
5. Connect the MPU6050 according to the wiring diagram.
6. Upload the firmware to the ESP32.
7. Open the Serial Monitor to inspect sensor readings and debug messages.
8. Connect the mobile application over BLE and test the supported communication and reset functions.

*The exact library names, sketch filename, and upload settings should be added after verifying the source code.*

## Testing

The prototype should be tested under controlled conditions using scenarios such as:

- Normal helmet movement
- Sudden but non-crash movements
- Simulated impact events
- Helmet movement when not worn, if wear detection is implemented
- BLE connection and disconnection
- Alert cancellation/reset

Do not perform dangerous crash simulations on a person. Use safe, controlled bench tests and document the results.

## Limitations

- The prototype is not a certified road-safety device.
- Crash detection depends on sensor placement, threshold selection, and validation logic.
- BLE-based communication depends on a compatible connected phone and the application's implementation.
- Automatic SMS/cellular communication requires a working cellular module or another supported communication gateway.
- Real-world reliability, false-positive rate, and detection accuracy require further testing.

## Future Improvements

- Integrate and validate GSM-based emergency notifications.
- Improve helmet-worn detection.
- Add crash-severity classification using validated sensor data.
- Implement low-power operation and battery monitoring.
- Add communication retry and fallback mechanisms.
- Conduct systematic testing and evaluate false-positive and false-negative rates.
- Develop a compact PCB and a secure helmet-compatible enclosure.

## Project Team

**Team:** Phantom_Loaded  
**Project:** Smart Helmet — Intelligent Crash Detection & Emergency Alert System

## Disclaimer

This is an educational engineering prototype intended for research and development. It must not be relied upon as the sole means of accident detection or emergency response.

## License

[Choose a suitable open-source license, such as MIT, if you want others to reuse and modify the code.]
