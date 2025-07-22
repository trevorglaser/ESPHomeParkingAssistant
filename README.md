# ESPHome Parking Assistant

My translation of https://github.com/Resinchem/ESP-Parking-Assistant for ESPHome.

# Smart Garage Parking Assistant (ESPHome + Ultrasonic Sensor + SK6812 LEDs)

A smart garage parking assistant using an **ESP32**, **HC-SR04 ultrasonic distance sensor**, and an **SK6812 addressable LED strip**, powered by **ESPHome** and fully integrated with **Home Assistant**.

This project visually guides drivers while parking using LED animations that adapt to distance, preventing false triggers from movement (like people walking in front of the sensor), and offers full configuration through Home Assistant.

---

## Features

- **Accurate distance-based LED feedback** using an HC-SR04 sensor.
- **LED animations** for approach, stop, and backup zones.
- **False trigger prevention** for people walking in front of the sensor.
- Fully **configurable distance zones and effects** via Home Assistant UI:
  - Approach Zone
  - Stop Zone
  - Backup Zone
  - LED Timeout
  - Animation style (`Out-In` or `In-Out`)

---

## 🔌 Wiring

| Device         | ESP32 Pin | Notes          |
|----------------|-----------|----------------|
| HC-SR04 Trig   | GPIO25    | TRIG pin       |
| HC-SR04 Echo   | GPIO26    | ECHO pin       |
| SK6812 Data    | GPIO4     | LED Data input |
| LED Power      | 5V / GND  | External supply recommended |

---

## ⚙️ Configuration

In Home Assistant, adjust:

- **Distance 1: Approach Zone** – Distance where animation starts
- **Distance 2: Stop Zone** – Target distance to stop
- **Distance 3: Backup Zone** – Too close and need to backup
- **Lights Timer** – How long the LEDs stay on after last change
- **Approach Effect** – Choose `"Out-In"` or `"In-Out"`

All parameters are adjustable live via the Home Assistant dashboard.

