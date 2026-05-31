---
title: "Confidential Alarm System"
subtitle: "IoT alert system for sensitive screen content protection"
tech: ["C++", "ESP32", "MQTT", "IoT", "CMake"]
sort_date: 2022
period: "2022"
---

## Overview

An IoT-based alert system designed to protect sensitive on-screen material in workplace environments. When triggered, the system instantly hides confidential content and alerts designated personnel — preventing shoulder-surfing and casual data exposure.

## Technical Details

- **ESP32 microcontroller** — WiFi-connected device with physical alert mechanism
- **MQTT messaging** — lightweight pub/sub protocol for instant trigger propagation
- **Custom desktop integration** — companion software that listens for alert signals and hides active windows
- **Physical alert** — visual/audible indicator on the ESP32 device itself for ambient awareness
- **Low-latency response** — end-to-end trigger-to-hide time measured in milliseconds

## Outcome

Deployed as a proof-of-concept in a security-conscious office environment. Demonstrated practical IoT security integration combining embedded hardware, network protocols, and desktop software into a cohesive privacy solution.
