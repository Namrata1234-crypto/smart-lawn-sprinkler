
# Smart Lawn Sprinkler System

## 1. Project Overview
The Smart Lawn Sprinkler is an IoT-based irrigation system designed to automate watering using soil moisture and rain detection.

The system uses a NodeMCU ESP8266 to read sensor inputs and control a DC water pump through a relay module.

## 2. Objectives
- Reduce unnecessary water usage.
- Detect soil moisture conditions.
- Detect rainfall automatically.
- Control the water pump based on sensor conditions.
- Provide a foundation for remote monitoring using Blynk.

## 3. Components Used
- NodeMCU ESP8266
- Soil Moisture Sensor
- Rain Drop Detection Sensor
- 5V Single Channel Relay Module
- 7805 Voltage Regulator
- 9V Batteries
- DC Water Pump
- Connecting Wires and Breadboard

## 4. Pin Connections

| Component | NodeMCU Pin |
|---|---|
| Soil Moisture Sensor (AO) | A0 |
| Rain Sensor (DO) | D5 |
| Relay Input | D6 |

## 5. Working Principle

1. The soil moisture sensor measures the soil condition.
2. The rain sensor checks whether rainfall is detected.
3. NodeMCU processes both sensor inputs.
4. If the soil is dry and rain is not detected, the pump is switched ON.
5. If the soil is moist or rain is detected, the pump is switched OFF.

## 6. Software Used
- Arduino IDE
- Embedded C / Arduino Programming
- GitHub
- Blynk (planned dashboard integration)

## 7. Quality Assurance
The following issues are considered for testing:
- Soil moisture threshold calibration.
- Rain sensor output detection.
- Relay activation logic.
- Pump scheduling.
- Sensor disconnection handling.
- Wi-Fi and Blynk connectivity.

## 8. Future Scope
- Morning and evening watering schedules.
- Blynk dashboard integration.
- Improved sensor fault detection.
- Water consumption monitoring.



---

## Project Documentation

Detailed project documents are available below:

- [Quality Assurance Log](docs/QA_LOG.md)
- [Hardware Connections](docs/HARDWARE_CONNECTIONS.md)

## GitHub Project Management

GitHub Issues are used to track identified problems, while GitHub Projects is used to monitor their progress.

## Student Details

**Name:** Namrata Santosh Babar

**PRN:** 202301070101

## 9. Safety and Testing
Sensor thresholds and relay logic must be verified with the actual hardware before connecting the pump. The current starter firmware does not yet implement scheduled watering or Blynk integration.

## 10. Conclusion
The Smart Lawn Sprinkler aims to make garden irrigation more efficient through sensor-based automation and IoT technology.
