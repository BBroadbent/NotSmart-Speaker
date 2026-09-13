# NotSmart Speaker

> **All the beats. None of the privacy risks.**

**NotSmart Speaker** is a custom, open-hardware local-first audio receiver designed to bring high-fidelity multi-room streaming to your home without the bloat, telemetry, or invasive microphones of commercial "smart" speakers. 

Powered by an ESP32 micro-controller, a PCM5100A I2S DAC, and a TPA3118 Class-D amplifier, it connects directly over Wi-Fi via the **Sendspin** protocol (integrating seamlessly with Home Assistant, Music Assistant, and local media setups).

---

## Features

- **100% Local & Cloud-Free:** No voice tracking, no external server dependency, no telemetry, and zero microphones.
- **20V USB-PD Powered:** Runs off a standard 45W+ USB-C laptop power brick using an onboard CH224K USB Power Delivery trigger IC.
- **Hi-Fi I2S Digital Path:** Uses the PCM5100A DAC to convert digital I2S audio signals straight from the ESP32.
- **Punchy Class-D Output:** Drives a single 4Ω mono speaker with up to ~40W cleanly via a TPA3118 amplifier in PBTL mode.
- **Clean Power Tree:** Dedicated buck step-down and low-noise LDO stages to protect sensitive audio lines from power noise.
- **Open Hardware:** Custom PCB layout engineered specifically for small desktop/shelf speaker enclosures.

---

## Hardware Architecture

### **Core Components**
| Component | Function |
| :--- | :--- |
| **ESP32** | Main microcontroller running local audio client firmware |
| **PCM5100A** | Dedicated I2S stereo/mono DAC |
| **TPA3118** | High-efficiency Class-D mono (PBTL) audio power amplifier |
| **CH224K** | Hardware USB-PD sink controller (Requests 20V profile) |
| **4Ω Mono Speaker** | Custom cabinet integration |

### **Power Architecture**
