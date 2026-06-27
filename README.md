# 🚓 Arduino-Based Speed Detection Radar System

[![Build Status](https://img.shields.io/badge/Status-Completed-success)](#)
[![Hardware](https://img.shields.io/badge/Hardware-Arduino-blue)](#)
[![Sensors](https://img.shields.io/badge/Sensors-Infrared_(IR)-red)](#)
[![Timeline](https://img.shields.io/badge/Timeline-Jan_2024_--_Mar_2024-orange)](#)

---

## 📖 Overview
A highly responsive, embedded hardware prototype engineered to accurately measure and report the velocity of moving objects in real-time. By leveraging the physical principles of kinematics, this system utilizes precision-calibrated Infrared (IR) sensor pairings to execute Time-of-Flight (ToF) calculations. It serves as a robust proof-of-concept for automated traffic monitoring systems, speed traps, and embedded motion-tracking technologies.

## ✨ Key Features
- **⏱️ Time-of-Flight (ToF) Calculations:** Accurately computes object velocity by capturing the exact microsecond time interval an object takes to travel between two fixed points.
- **🎯 Precision IR Calibration:** Features meticulously aligned and calibrated Infrared sensor pairs, optimized to eliminate false positives and ensure high-fidelity motion detection under varying lighting conditions.
- **⚙️ Embedded C++ Processing:** Fully self-contained logic executed on an Arduino microcontroller, demonstrating efficient, low-level hardware programming and hardware interrupt management.
- **📊 Real-Time Analytics:** Instantly processes sensor triggers and translates raw timing data into readable speed metrics (e.g., cm/s, m/s, or km/h).

## 🛠️ Hardware Components
*(Note: Adjust the specific module names based on your actual physical build)*
- **Microcontroller:** Arduino Uno / Nano (Core processing unit)
- **Sensing Mechanism:** 2x Infrared (IR) Obstacle Avoidance Sensors (Transmitter/Receiver pairs)
- **Output Interface:** I2C LCD Display or Serial Monitor (For real-time speed visualization)
- **Prototyping Essentials:** Breadboard, jumper wires, and precision measuring tools for spatial calibration.

## 💻 Software & Logic Architecture
- **Development Environment:** Arduino IDE (`C/C++`).
- **Interrupt Handling:** Utilizes Arduino's hardware interrupts to capture millisecond/microsecond timestamps the exact moment an IR beam is broken, ensuring zero-latency calculations.
- **Kinematic Algorithm:** Applies the fundamental physics formula `Velocity = Distance / ∆Time`, where the distance is the rigorously measured physical gap between the two IR sensors.

## ⚙️ How it Works
1. **Initiation (Point A):** A moving object passes the first IR sensor, breaking its beam. This triggers a hardware interrupt that records the start time ($T_1$).
2. **Completion (Point B):** The object continues and breaks the beam of the second IR sensor. A second interrupt records the stop time ($T_2$).
3. **Data Processing:** The Arduino calculates the time delta ($\Delta T = T_2 - T_1$).
4. **Speed Output:** Using the pre-programmed, calibrated distance between the sensors, the microcontroller instantly calculates the speed and outputs the result to the display.

## 📅 Project Timeline
- **Development Period:** January 2024 – March 2024
