# IoT-Based Vehicle Overspeed Detection System

A real-time vehicle speed monitoring system built using ultrasonic sensors and ESP32 that detects overspeeding and automatically sends notifications with captured image evidence.

## Overview

This project uses two ultrasonic sensors placed a known distance apart on a road segment to calculate a vehicle's speed in real time. If the speed exceeds a set threshold, the system automatically captures an image of the vehicle and sends an email alert — enabling automated, low-cost speed enforcement without manual monitoring.

## Features

- **Real-time speed monitoring** using ultrasonic sensors
- **Time-based speed calculation model** for accurate detection based on distance/time between two sensor trigger points
- **Automated notification system** — sends email alerts with captured image when overspeeding is detected
- **Network-based device communication** with dynamic IP handling, allowing the system to stay connected and reachable on changing networks

## Tech Stack / Hardware

- **Microcontroller:** ESP32
- **Sensors:** Ultrasonic sensors (e.g., HC-SR04) x2
- **Camera module** (for image capture on detection)
- **Connectivity:** Wi-Fi (ESP32), dynamic IP handling
- **Notification:** Email/SMTP integration
- **Firmware:** Arduino IDE / C++

## How It Works

1. Two ultrasonic sensors are placed at a fixed, known distance apart along the road.
2. When a vehicle passes the first sensor, a timer starts; when it passes the second sensor, the timer stops.
3. Speed is calculated using `speed = distance / time`.
4. If the calculated speed exceeds the configured speed limit, the ESP32 triggers the camera to capture an image of the vehicle.
5. The system sends an automated email alert containing the captured image and speed details.
6. Dynamic IP handling ensures the device stays connected and reachable even as network conditions change.

## Getting Started

> Fill in with your actual setup instructions.

```bash
# Clone the repository
git clone https://github.com/Deeksha2508/IoT-Vehicle-Overspeed-Detection.git
cd IoT-Vehicle-Overspeed-Detection

# Flash the firmware to ESP32 via Arduino IDE
# Configure: speed threshold, sensor pin numbers, Wi-Fi credentials, email SMTP settings
```

### Hardware Setup

- Sensor placement distance (add exact measurement used)
- Wiring/circuit diagram (add an image here)
- Camera module connection details

## Results

- Add measured accuracy, tested speed range, and detection reliability here.

## Future Improvements

- Add license plate recognition (OCR) alongside image capture
- Log data to a cloud dashboard for historical analysis
- Support multiple lanes with synchronized sensor arrays

