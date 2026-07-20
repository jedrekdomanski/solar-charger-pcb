# ☀️ Solar-Powered 3.3V Power Management PCB

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![KiCad Version](https://img.shields.io/badge/KiCad-v8.0+-blue.svg)](https://www.kicad.org/)

![Solar Charger PCB Board](_OL_6112.jpg)
An open-source custom PCB designed to power microcontrollers efficiently using solar energy and Li-Ion battery management.

---

## 🎯 Motivation

When building ultra-low-power IoT nodes and microcontrollers for outdoor automation (like smart irrigation systems), reliable off-grid power is always a bottleneck. 

My motivation behind this project was to step away from breadboards and create a compact, custom-designed PCB capable of harvesting solar energy to keep a Li-Ion battery charged while delivering a stable, clean **3.3V power supply** to a microcontroller 24/7.

---

## ⚡ How It Works

1. **Energy Harvesting:** Two 5V solar panels connected in parallel capture sunlight and supply current to the charging circuit.
2. **Battery Management:** The TP4056 module safely manages the charging process of a Li-Ion battery while actively protecting it from overcharging and deep discharge.
3. **Voltage Regulation:** The low-quiescent LDO regulator steps down the variable battery voltage (3.0V – 4.2V) to a stable **3.3V** required by most modern microcontrollers (e.g., ESP32, STM32, or ATmega).
4. **Power Conditioning:** A combination of electrolytic and ceramic capacitors decouples noise and smooths out sudden voltage spikes or transient current draws (e.g., during Wi-Fi/Bluetooth bursts).

---

## 🛠️ Key Hardware Components

| Component | Function / Specification |
| :--- | :--- |
| **2x 5V Solar Panels (Parallel)** | Configured in parallel to boost current yield (mA) while maintaining a safe 5V input for the charger. |
| **TP4056 Charging Module** | Includes onboard overcharge, over-discharge, and over-current protection for safe battery cycles. |
| **18650 / Li-Ion Battery** | Energy storage medium, providing power during night time or cloudy days. |
| **MCP1700-3302E/TO92 LDO** | Low Quiescent Current LDO regulator stepping down battery voltage to a steady 3.3V output. |
| **100µF Electrolytic Capacitor** | Bulk storage capacitor providing sudden current bursts required by wireless microcontrollers. |
| **100nF Ceramic Capacitor** | High-frequency decoupling capacitor to filter high-frequency noise and voltage ripples. |

---

## 👤 Author & Journey

Designed with passion as part of my journey into hardware engineering, embedded systems, and robotics.

* **GitHub:** [@jedrekdomanski](https://github.com/jedrekdomanski)
* **Project Status:** Active / Tested Prototype

*Feel free to fork, star ⭐️, or open an issue if you have suggestions for improvement!*
