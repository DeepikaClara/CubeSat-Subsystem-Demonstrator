# CubeSat-Subsystem-Demonstrator

## Overview

This project demonstrates the conceptual design and implementation of a CubeSat-inspired satellite subsystem architecture using prototyping hardware and open-source tools.

The primary objective of this project is to understand how different satellite subsystems interact and to simulate their functionality using embedded systems, IoT communication protocols, and mechanical design tools.

This project does **not represent a flight-ready satellite**. Instead, it serves as an educational and engineering demonstrator that replicates the functional architecture of a small satellite.

---

# Project Objectives

- Design a CubeSat-inspired satellite architecture.
- Develop a conceptual PicoSat structure using Fusion 360.
- Implement a payload subsystem for environmental data acquisition.
- Simulate onboard data handling using SD card storage.
- Simulate satellite telemetry using MQTT.
- Develop a ground station dashboard for monitoring telemetry.
- Understand how real satellite subsystems communicate and operate.

---

# System Architecture

```text
                 Ground Station
                     (Blynk)
                        ^
                        |
                     MQTT
                        |
                        |
       +----------------+----------------+
       | Communication Subsystem         |
       | WiFi + MQTT Telemetry           |
       +----------------+----------------+
                        |
                        |
       +----------------v----------------+
       |      OBC (On Board Computer)    |
       |           ESP8266               |
       +-----------+---------+-----------+
                   |         |
                   |         |
                   v         v

       +-----------+--+   +--+-----------+
       | Payload      |   | ADCS         |
       | DHT Sensor   |   | Conceptual   |
       | SD Card      |   | Subsystem    |
       +--------------+   +--------------+
```

---

# Subsystem Mapping

| Real Satellite | Demonstrator |
|---------------|-------------|
| On Board Computer | ESP8266 |
| Payload | DHT Sensor |
| Onboard Memory | SD Card |
| Communication System | MQTT + WiFi |
| Ground Station | Blynk Dashboard |
| Satellite Structure | Fusion 360 Model |
| ADCS | Conceptual Design (Future MPU6050 Integration) |

---

# Subsystems

---

## 1. Structure Subsystem

### Objective

Design a PicoSat-inspired satellite enclosure and subsystem layout.

### Tool

- Fusion 360

### Features

- CubeSat-inspired mechanical structure
- Internal subsystem segregation
- Payload compartment
- OBC compartment
- Communication compartment

### Skills Demonstrated

- CAD Design
- Fusion 360
- Mechanical Packaging
- Systems Integration

---

## 2. On Board Computer (OBC)

### Description

The ESP8266 acts as the central processing unit of the satellite.

### Responsibilities

- Sensor data acquisition
- Data processing
- Data logging
- Telemetry transmission
- System control

### Skills Demonstrated

- Embedded Systems
- Arduino IDE
- Firmware Development
- ESP8266 Programming

---

## 3. Payload Subsystem

### Description

The payload is responsible for collecting mission-related data.

### Payload Components

- DHT11 / DHT22 Sensor

### Collected Parameters

- Temperature
- Humidity

### Real Satellite Equivalent

Similar to weather monitoring and environmental sensing payloads used in small satellites.

### Skills Demonstrated

- Sensor Interfacing
- Data Acquisition
- Embedded Programming
- Payload Integration

---

## 4. On Board Data Handling (OBDH)

### Description

Real satellites store mission data before transmitting it to a ground station.

This functionality is simulated using an SD card module.

### Example Data

```csv
Timestamp,Temperature,Humidity

10:00,29,75
10:05,30,74
```

### Skills Demonstrated

- SPI Communication
- Data Logging
- File Handling
- Storage Systems

---

## 5. Communication Subsystem

### Description

The communication subsystem simulates telemetry flow between the satellite and a ground station.

### Technology Used

- WiFi
- MQTT

### Telemetry Example

```json
{
  "temperature": 29,
  "humidity": 75,
  "status": "Nominal"
}
```

### Important Note

Real satellites typically use dedicated RF communication systems and protocols such as:

- CCSDS
- AX.25
- CubeSat Space Protocol (CSP)

MQTT is used in this project solely to simulate telemetry concepts and subsystem communication.

### Skills Demonstrated

- MQTT
- IoT Communication
- Telemetry Concepts
- Wireless Networking

---

## 6. Ground Station

### Description

A Blynk Dashboard acts as a simplified ground station.

### Dashboard Functions

- Temperature Monitoring
- Humidity Monitoring
- Telemetry Visualization
- System Health Monitoring

### Skills Demonstrated

- Data Visualization
- Dashboard Development
- Telemetry Monitoring

---

## 7. ADCS (Conceptual)

### Description

The Attitude Determination and Control System (ADCS) is currently represented as a conceptual subsystem.

Future versions may integrate:

- MPU6050
- Accelerometer
- Gyroscope

### Future Functions

- Roll Measurement
- Pitch Measurement
- Yaw Measurement
- Orientation Monitoring

### Skills Demonstrated

- Satellite Attitude Control Concepts
- IMU Integration
- Aerospace Fundamentals

---

# Development Phases

## Phase 1

✅ Mission Definition

✅ System Architecture

✅ Subsystem Mapping

---

## Phase 2

✅ Fusion 360 Structure Design

---

## Phase 3

✅ Payload Implementation

- DHT Sensor

---

## Phase 4

✅ Data Logging

- SD Card Storage

---

## Phase 5

✅ Telemetry Transmission

- MQTT Communication

---

## Phase 6

✅ Ground Station Dashboard

- Blynk Visualization

---

## Phase 7

🔄 ADCS Integration (Future Work)

- MPU6050
- Attitude Estimation

---

# Technologies Used

## Hardware

- ESP8266
- DHT11/DHT22
- SD Card Module
- Breadboard
- Jumper Wires

## Software

- Arduino IDE
- Fusion 360
- MQTT
- Blynk
- GitHub

---

# Key Learning Outcomes

- Satellite Subsystem Architecture
- CubeSat Design Concepts
- Systems Engineering
- Embedded Systems Development
- Sensor Integration
- Telemetry Concepts
- Data Handling
- Ground Station Monitoring
- CAD Design Using Fusion 360

---

# Future Improvements

- ADCS Integration using MPU6050
- Solar Power Simulation
- Battery Management System
- LoRa Based Telemetry
- PCB Design using KiCad
- Custom Satellite Bus Design
- CubeSat Space Protocol (CSP) Simulation

---

# Author

This project was developed as a hands-on exploration of CubeSat and PicoSat engineering concepts, integrating embedded systems, telemetry, payload development, and conceptual spacecraft design into a single educational demonstrator.
