---
title: "Baby’s sleeping monitoring"
description: Designed and implemented an embedded IoT to monitor baby sleep, trigger audio soothing, and send real-time parental alerts via Telegram.
date: 2026-08-30T11:23:57Z
image: BSM.jpg
math: 
license: 
comments: true
draft: false
build:
    list: always    # Change to "never" to hide the page from the list
---

[![Bee Tracking Demo](https://img.youtube.com/vi/7zeq_d3Gcyo/maxresdefault.jpg)](https://www.youtube.com/shorts/7zeq_d3Gcyo)

## 👶 Baby Sleep Monitoring System

Designed and implemented an **embedded IoT system for baby sleep monitoring** that combines motion sensing, automated audio soothing, and real-time parental notifications.

### 🔧 Key Features

* **Sleep movement monitoring:** Used the **MPU6050 accelerometer and gyroscope** to detect and analyze the baby's movements during sleep.
* **Automatic soothing:** Integrated a **DFPlayer Mini and mini speaker** to automatically play soothing audio when significant movement or restlessness was detected.
* **Real-time parental alerts:** Connected the system to **Telegram** to send notifications to parents when predefined movement conditions were detected.
* **Embedded control:** Developed the system logic in **C++** on a **ESP32**, integrating sensor input, audio playback, and communication into a single monitoring workflow.
* **Event-based monitoring:** Designed the system to continuously monitor sensor data and trigger appropriate actions based on detected movement patterns.

### ⚙️ System Workflow

**MPU6050 → ESP32 → Movement Analysis →**

↳ **Normal sleep** → Continue monitoring
↳ **Detected movement** → Play soothing audio
↳ **Significant/abnormal movement** → Send Telegram alert

### 🛠️ Technologies & Hardware

**Programming:** C++
**Platform:** ESP32
**Sensor:** MPU6050 (Accelerometer + Gyroscope)
**Audio:** DFPlayer Mini + Mini Speaker
**Communication:** Telegram Bot API
**Domain:** Embedded Systems · IoT · Sensor Processing · Automation
