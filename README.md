🔋 Smart Battery Management System (BMS) for 3S Li-Po Battery

A custom hardware design for a 3S Li-Po Battery Management System (BMS) built around the BQ76920 battery monitor and ESP32-S3-WROOM-1.

The project focuses on schematic design, power management, battery monitoring, protection circuitry, temperature sensing, MOSFET control, and complete PCB layout using KiCad.


 📌 Project Overview

The objective of this project was to design a compact and integrated BMS PCB for a 3S Li-Po battery system.

The PCB integrates battery monitoring, current sensing, temperature monitoring, charge/discharge control, power regulation, and external interfaces into a single board.

 Main Architecture

3S Li-Po Battery → BQ76920 → ESP32-S3 → Monitoring & Control

Power architecture:

12 V → 5 V Buck Converter → 3.3 V LDO

- 🔋 3S Li-Po battery interface
- 🧠 ESP32-S3-WROOM-1 MCU
- 🔍 BQ76920 battery monitor
- 📊 Individual cell-voltage monitoring
- ⚡ Current sensing using shunt resistor
- 🌡️ NTC temperature sensing
- 🛡️ Charge/discharge MOSFET control
- 🔥 Heater control circuitry
- ⚡ 12 V → 5 V buck converter
- 🔌 5 V → 3.3 V LDO
- 🖥️ OLED display interface
- 🔘 Push-button controls
- 🔌 USB-C interface
- 🔧 UART programming/debug interface
- 🛡️ Protection and filtering circuitry

 🧩 Hardware Blocks

 1. Battery Monitoring

The **BQ76920** is used as the battery monitoring IC for the 3S battery pack.

It provides interfaces for:

- Individual cell voltage monitoring
- Current measurement
- Temperature monitoring
- Battery protection signals
- I²C communication with the ESP32-S3


 2. ESP32-S3 Controller

The **ESP32-S3-WROOM-1** acts as the main controller of the BMS hardware.

Interfaces include:

- I²C communication
- OLED interface
- Push buttons
- Heater control
- USB interface
- UART programming/debugging

 3. Power Supply

The PCB uses a two-stage power supply.

 Stage 1: 12 V → 5 V

An **LM2596S-5 buck converter** generates the 5 V supply.

Stage 2: 5 V → 3.3 V

An **AMS1117-3.3 LDO** generates the regulated 3.3 V supply for the digital circuitry.

4. Protection & Control

The design includes MOSFET-based switching for charge/discharge control.

The protection section is connected to the BQ76920 monitoring system and battery power path.

 5. Temperature & Heater Control

NTC-based temperature sensing is included for monitoring system temperature.

A dedicated heater control circuit is also incorporated into the design for thermal management.


👩‍💻 Author
Harshitha S
Electronics & Communication Engineering
