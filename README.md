# Smart_Home_Monitoring
1. Project Overview

This Smart Home Monitoring System is designed to enhance home security by integrating motion detection and video surveillance. It uses a PIR sensor to detect motion and an ESP32-CAM module to capture and stream real-time video. The system is suitable for entryways, living rooms, or outdoor areas to alert homeowners of activity.

2. Components Used

A. ESP32-CAM

Description:
The ESP32-CAM is a low-cost microcontroller with WiFi and Bluetooth capabilities. It includes a built-in camera module (usually OV2640) and can be programmed to act as a video streaming server.

Key Features:

Built-in OV2640 2MP camera

MicroSD card support for local image or video storage

WiFi 802.11 b/g/n support

Bluetooth 4.2

UART, SPI, I2C, PWM interfaces (limited GPIOs)

Can host a web server to stream video in real-time

Operates at 3.3V, with 5V input support via onboard regulator

Role in the Project:

Serves as the core controller of the system

Hosts a web server to display the live camera feed

Interacts with the PIR sensor to detect motion

Captures photos or starts streaming when motion is detected

B. FTDI232 USB to Serial Adapter

Description:
The FTDI232 is a USB to UART adapter used to upload code to boards like ESP32-CAM that do not have a built-in USB port.

Key Features:

Converts USB signals to serial (UART) logic

Supports 3.3V and 5V logic levels (configurable)

Has TX, RX, VCC, GND, and DTR pins

Commonly used to program ESP32, ESP8266, Arduino Pro Mini

Role in the Project:

Used to upload code to the ESP32-CAM using Arduino IDE or similar tools

Establishes serial communication between the computer and the ESP32 board

Required only during initial code uploading or reprogramming

Wiring with ESP32-CAM:

FTDI TX to ESP32 RX (U0R)

FTDI RX to ESP32 TX (U0T)

GND to GND

VCC to 5V

IO0 to GND (to enable programming mode)

C. PIR Motion Sensor

Description:
The PIR sensor (Passive Infrared) detects infrared radiation emitted by humans or animals. It is a common choice for motion detection in security systems.

Key Features:

Detection range typically 3 to 7 meters

Adjustable delay time and sensitivity

Outputs a digital HIGH signal when motion is detected

Operates on 5V

Role in the Project:

Continuously monitors for motion

Sends a HIGH signal to the ESP32-CAM when movement is detected

The ESP32-CAM responds by taking an action, such as capturing an image, starting the video stream, or sending an alert

3. Working Principle

The PIR sensor constantly checks for motion.

When motion is detected, the PIR sensor outputs a digital HIGH signal.

The ESP32-CAM reads this signal from one of its GPIO pins.

Upon detection, the ESP32-CAM either:

Captures and stores an image on an SD card

Sends the image or alert to a cloud server

Activates a live video stream accessible via web browser on the same network

The live stream is hosted by the ESP32-CAM’s internal web server.

4. Applications

Home entrance surveillance

Office or warehouse monitoring

Baby monitor or elderly care

Remote animal monitoring

Smart doorbell systems

5. Advantages

Low cost and compact

Wireless access over WiFi

Real-time monitoring

Customizable alerts and image capture

Easy to program using Arduino IDE or ESP-IDF

6. Future Enhancements

Integrate cloud services like Firebase or AWS for remote access

Add email or push notifications on motion detection

Night vision using IR LEDs

Use rechargeable battery and solar power for outdoor deployment
