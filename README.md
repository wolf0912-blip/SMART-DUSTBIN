# SMART-DUSTBIN
ESP32 Smart Dustbin & Waste Segregator
An IoT-powered smart waste segregation system built using an ESP32 microcontroller. The system automatically detects incoming waste using an ultrasonic sensor, analyzes its moisture content via a soil moisture sensor, and tilts a servo-driven sorting tray into either the Wet or Dry waste compartment.

It also hosts a local responsive web dashboard directly on the ESP32, allowing users to monitor live waste counts, sensor telemetry, and system states in real time over Wi-Fi.

✨ Key Features
Automated Segregation: Uses an HC-SR04 ultrasonic sensor to detect objects and an analog soil moisture sensor to distinguish between wet and dry waste.

No External Servo Libraries Required: Directly drives the servo motor using the ESP32's native LEDC hardware PWM, making it fully compatible with both Arduino ESP32 core v2.x and v3.x.

Embedded Web Dashboard: Built-in web server (WebServer.h) serving a modern, mobile-friendly HTML/CSS interface via Access Point (AP) or Home Wi-Fi mode.

Non-Volatile Storage (NVS): Persistently saves wet and dry item counts across reboots using the ESP32 Preferences library.

Non-Blocking State Machine: Uses millis-based asynchronous timing (IDLE, SETTLING, TILTED, COOLDOWN) to keep the web server responsive while handling physical sensors.
