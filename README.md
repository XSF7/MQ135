# MQ135 Sensor with ESP32

<div align="center">
  <img src="http://esp32.net/images/_resources/ESP32NET_Masthead.svg" width="500"/>
</div>

## Project Overview
This project integrates the MQ135 gas sensor with an ESP32 microcontroller, enabling real-time air quality monitoring via a web dashboard. The system includes advanced features such as automatic sensor calibration, Wi-Fi auto-reconnection, and an MDNS responder for easy access to the web server.

### Key Features
- **Web Dashboard:** Real-time visualization of sensor data.
- **MDNS Responder:** Access the server with a friendly URL (e.g., `http://esp32.local`).
- **Auto Sensor Calibration:** Ensures sensor accuracy over time.
- **SPIFFS Volume:** Store files and web assets directly on the ESP32.
- **LED Indication:** Visual status of system states and sensor readings.
- **Auto Wi-Fi Reconnection:** Maintains connection stability.

## Getting Started

### Hardware Requirements
- ESP32 Development Board
- MQ135 Gas Sensor
- LED (optional for status indication)
- Jumper Wires and Breadboard

### Pin Configuration
- **MQ135 Sensor Analog Pin:** Connect to ESP32 GPIO 34 (adjustable in the code)

### Software Requirements
- Arduino IDE or PlatformIO
- ESP32 Board Package
- Required Libraries:
  - `WiFi.h`
  - `WebServer.h`
  - `ESPmDNS.h`
  - `SPIFFS.h`

### Setup Instructions
1. **Install Dependencies:** Make sure all libraries are installed in your development environment.
2. **Configure SPIFFS:** Load the SPIFFS file system onto the ESP32.
3. **Upload Code:** Flash the ESP32 with the code located in the `MQ135` folder.
4. **Connect Hardware:** Wire the sensor and components as shown in the `Pictures` folder.
5. **Power On:** The ESP32 will connect to Wi-Fi and host the web server.

### Accessing the Web Dashboard
- Open a browser and go to `http://esp32.local` or the ESP32’s IP address.
- The dashboard will display real-time air quality data.

## Web Server Details
- **Port:** 80
- **Authentication:** Not required (consider adding security if needed)

## Calibration and Usage
- Allow the sensor to warm up for a few minutes.
- The system performs automatic calibration to enhance measurement accuracy.

## Troubleshooting
- **Wi-Fi Connection Issues:** Ensure the Wi-Fi credentials are correct.
- **Web Server Not Accessible:** Check the serial monitor for error messages.
- **Incorrect Sensor Readings:** Recalibrate the sensor or check the analog pin connection.

## Possible Enhancements
- Add authentication to the web server.
- Implement data logging to SPIFFS or an external server.
- Integrate with cloud services (e.g., ThingSpeak, MQTT).

## Acknowledgments
Special thanks to the open-source community and contributors who provided libraries and support for this project.

---
Feel free to reach out for support or contribute to the project by submitting pull requests or issues!

