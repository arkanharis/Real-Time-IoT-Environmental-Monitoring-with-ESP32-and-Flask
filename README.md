# Real-Time IoT Environmental Monitoring with ESP32 and Flask

This repository contains an IoT project using ESP32 microcontroller and Flask framework for real-time environmental monitoring. The ESP32 gathers temperature, humidity, and air quality data from sensors and sends it to a Flask server via HTTP POST requests. The Flask server displays the latest data on a web page and supports long polling for real-time updates.

## Components:
- ESP32 Microcontroller: Handles data collection from sensors and sends it to the server.
- DHT22 Sensor: Measures temperature and humidity.
- MQ135 Sensor: Measures air quality.
- Flask Server: Receives data from ESP32, displays real-time data on a web page, and supports long polling for continuous updates.

##  Files:
- **SIC_PROJECT_1.ino**: Arduino sketch for ESP32 that collects sensor data and sends it to the Flask server.
- **main.py**: Python script for the Flask server that handles HTTP requests, stores data, and serves a web page with real-time updates.
- **circuit_diagram.png**: Diagram showing the circuit connections between the sensors and ESP32.

## Setup Instructions:
ESP32 Setup:
* Upload SIC_PROJECT_1.ino to your ESP32 using the Arduino IDE or similar.
* Ensure WiFi credentials (WIFI_SSID and WIFI_PASS) and sensor pin assignments (sensor_input, DHTPIN, DHTTYPE) are correctly configured.

Flask Server Setup:
*Install required Python packages: Flask.
*Run main.py on your server (e.g., Raspberry Pi, local machine) with Python.

## Accessing Data:
* Navigate to http://<server-ip>:5000/ to view real-time data.
* The web page updates automatically using long polling whenever new data is received from ESP32.

## Example Usage:
* Start the Flask server (main.py).
* Power on the ESP32 connected to sensors.
* Open a web browser and navigate to the server's IP address.
* Monitor real-time updates of temperature, humidity, and air quality displayed on the web page.

## Circuit Diagram:

!["circuit_diagram"](https://github.com/arkanharis/Real-Time-IoT-Environmental-Monitoring-with-ESP32-and-Flask/blob/92958accb6adb84517e79e287e2a3c4e7d22433f/circuit_diagram.jpg?raw=true)

Notes:
Ensure proper connections between sensors (DHT22, MQ135) and ESP32, especially regarding power supply (VIN pin).
Modify the server URL in SIC_PROJECT_1.ino if the Flask server is hosted on a different IP or port.
