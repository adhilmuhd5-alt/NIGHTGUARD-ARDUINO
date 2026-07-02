# NIGHTGUARD-ARDUINO
It is a system to detect any presence of person in front of our door in night

NightGuard: Object Detection with Nokia Alert 🎶
Overview
NightGuard is an Arduino-based system designed for night-time object detection. It combines an HC-SR04 ultrasonic sensor and an LDR (Light Dependent Resistor) to detect nearby objects in low-light conditions. When triggered, the system plays the iconic Nokia ringtone on a passive buzzer, serving as an audible alert.

This project is ideal for learning sensor integration, conditional logic, and sound generation with Arduino.

Features
📏 Distance Measurement: Detects objects within 10 cm using the HC-SR04 ultrasonic sensor.

🌙 Light Detection: Uses an LDR to sense ambient light levels and activates only in darkness.

🎵 Nokia Ringtone Alert: Plays a nostalgic Nokia tune on a passive buzzer when conditions are met.

🖥️ Serial Monitoring: Outputs real-time distance and LDR values for debugging and calibration.

Hardware Requirements
Arduino Uno (or compatible board)

HC-SR04 Ultrasonic Sensor

LDR (Light Dependent Resistor)

Passive Buzzer

Resistors (for LDR voltage divider)

Jumper wires and breadboard

Circuit Connections
Component	Arduino Pin
HC-SR04 TRIG	D9
HC-SR04 ECHO	D10
LDR	A0
Passive Buzzer	D8


Software Details
Written in Arduino C++.

Uses tone() function for buzzer sound generation.

Adjustable light threshold (lightThreshold = 500) for different environments.

Detection logic ensures the ringtone plays once per trigger to avoid continuous retriggering.

How It Works
The ultrasonic sensor measures distance.

The LDR checks ambient light levels.

If an object is detected within 10 cm and the environment is dark:

The buzzer plays the Nokia ringtone.

A short delay prevents repeated triggers.

Getting Started
Clone this repository:

bash
git clone https://github.com/your-username/NightGuard.git
Open the code in the Arduino IDE.

Upload to your Arduino Uno.

Connect the circuit as per the diagram.

Monitor values via the Serial Monitor and adjust the light threshold if needed.

Future Improvements
🔋 Add battery power support for portability.

💡 Integrate an LED flashlight for visual alerts.

📱 Expand with Bluetooth/Wi-Fi for remote notifications.
