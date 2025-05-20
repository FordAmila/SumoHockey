# 🤖 SumoHockey Project

**SumoHockey** is a hybrid Arduino-based robot that combines the functionalities of a **SumoBot** and a **HockeyBot**, switchable through a single SPDT mode toggle. Designed for both competitive robotics and interactive play, this project integrates multiple sensors, PWM-controlled motors, and Bluetooth-based remote control for dynamic maneuverability.

## 🔧 Features

- 🥋 **Sumo Mode**
  - IR sensors to detect the white boundary of a black doyo ring
  - Ultrasonic sensor for opponent detection and strategic attack
  - Aggressive autonomous behavior for Sumo competitions

- 🏒 **Hockey Mode**
  - Bluetooth control via custom MIT App Inventor mobile app
  - PWM-based motor speed control (0–255 range)
  - Precision control for interactive play and robot soccer

- 🛠️ **Shared Features**
  - Arduino Nano-based control
  - L298N motor driver
  - 7.4V rechargeable battery with buck converter
  - Mode selection using an SPDT switch on digital pin
  - Robust chassis and modular wiring for easy maintenance

## 🧠 Components Used

| Component              | Description                            |
|------------------------|----------------------------------------|
| Arduino Nano           | Main microcontroller                   |
| L298N Motor Driver     | Dual H-Bridge to drive DC motors       |
| Ultrasonic Sensor (HC-SR04) | Object/opponent detection        |
| IR Sensors             | Line/boundary detection                |
| SPDT Switch            | Toggle between Sumo and Hockey modes   |
| Bluetooth Module (HC-05/06) | Wireless communication           |
| 7.4V Li-ion Battery    | Power source for motors and Arduino    |
| Buck Converter         | Voltage regulation                     |
| Custom Android App     | Bluetooth controller with PWM sliders  |

## 📱 Mobile App

- Built with MIT App Inventor
- Two modes:
  - **Sumo** (autonomous)
  - **Hockey** (manual with PWM sliders)
- Connects via Bluetooth to control robot

## 🔌 Wiring Overview

- SPDT switch: Mode selection input on D2
- IR sensors: Digital pins for boundary detection
- Ultrasonic sensor: Trigger/Echo to D7/D6 (example)
- Motors: Connected through L298N to Arduino and power
- Bluetooth: RX/TX connected to Arduino Serial

## 🎮 Controls

| Mode     | Control Method        | Behavior                    |
|----------|-----------------------|-----------------------------|
| Sumo     | Autonomous (IR + Ultrasonic) | Seek and push opponent, avoid boundary |
| Hockey   | Manual (Bluetooth App) | Real-time directional control with speed tuning |


## 🚀 Getting Started

1. Upload the `sumohockey.ino` to your Arduino Nano.
2. Connect all components as shown in the wiring diagram.
3. Pair your phone with the Bluetooth module.
4. Load and run the Android app.
5. Use the SPDT switch to toggle between Sumo and Hockey modes.

## 📚 Future Improvements

- Add OLED display for debug/status info
- PID control for smoother motor response
- Add buzzer feedback and LEDs
- Multi-mode LCD interface
- Autonomous Hockey behavior

## 👥 Authors

- Clifford Clint A. Amila – Hardware Design, Arduino Programming, App Development
- Team Members: Edden Dawn Marie A. Guzman

## 📜 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

---

_Enjoy building and battling with SumoHockey!_
