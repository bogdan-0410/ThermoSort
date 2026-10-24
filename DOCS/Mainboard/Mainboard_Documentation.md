# ThermoSort Main Board

## Overview

The ThermoSort Main Board is responsible for processing the data received from the Sensor Board and determining whether a detected object is a battery or another type of material. It connects the sensing hardware with the system’s control and communication functions. The board uses two microcontrollers, an RP2040 and an ESP32, each handling different tasks within the system.

## RP2040

The RP2040 is the main microcontroller responsible for processing sensor data and making the final detection decision. It receives measurements from the Sensor Board and compares them with predefined reference values and detection thresholds. By analyzing the thermal and ultrasonic measurements, it determines the detection result and sends it to the ESP32 for further use.

Keeping the main processing tasks on the RP2040 allows the system to handle sensor data independently of the web interface and Wi-Fi functions.

## ESP32

The ESP32 handles the wireless communication and user interface of the system. It provides Wi-Fi connectivity and hosts a web interface through which users can access system information and adjust settings.

It receives the detection results from the RP2040 and makes them available through the web interface. The ESP32 also manages the configuration of detection thresholds and Wi-Fi network credentials, allowing users to modify settings without having to reprogram the main microcontroller.

## Communication System

The Main Board connects to the Sensor Board through an 8-pin connector. This connection supplies power to the Sensor Board and carries the signals required for communication between the two boards.

The sensor data is transferred to the RP2040, where it is processed to determine the detection result. The RP2040 then communicates the result to the ESP32, which handles its presentation through the web interface.

Separating the sensing, processing, and user interface functions between the two boards makes the system easier to maintain and allows each microcontroller to focus on its specific tasks.