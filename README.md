# AREH-PMS
AREH-PMS Ambient Charging System 
# AREH-PMS

Ambient/Renewable Energy Harvesting & Power Management System

## Mission
AREH-PMS is a modular system that harvests small amounts of energy from different ambient sources, manages and stores that energy efficiently, and provides useful power while monitoring and optimizing itself.

## Prototype 001
The first engineering objective is to build an instrumented test platform that measures and compares RF, solar, vibration, and thermal energy inputs and establishes repeatable baseline data.

## Core Architecture
Energy sources -> source-specific harvesting front ends -> power management -> energy storage -> voltage regulation -> load.

Telemetry measures voltage, current, power, temperature, storage state, and system performance. A microcontroller records the measurements and communicates with an Android monitoring and analytics application.

## Project Areas
- Hardware
- Firmware
- Android application
- Experiments and measured data
- Procurement and salvage inventory
- Engineering research journal
- Technical research
- IP and prior-art documentation

## Engineering Rule
Measured results must be distinguished from hypotheses, simulations, and design targets. Failed experiments are retained because they are part of the engineering record.
docs/
hardware/
firmware/
android/
experiments/
research/
procurement/
ip/

Initial repository baseline: 2026-09-11.
# AREH-PMS System Architecture

## Document Purpose
This document defines the baseline engineering architecture for the Ambient/Renewable Energy Harvesting & Power Management System (AREH-PMS).

## System Objective
AREH-PMS is designed as a modular multi-source energy-harvesting platform capable of collecting, conditioning, storing, measuring, and managing energy from ambient and renewable sources.

## Energy Sources

### RF Energy
Potential sources include:
- Wi-Fi
- Cellular RF
- Bluetooth
- Other legally accessible ambient RF sources

RF harvesting path:

Antenna → Impedance Matching → RF Rectifier/Rectenna → Energy-Harvesting PMIC

### Solar Energy

Photovoltaic Cell → MPPT/Energy Harvester → Power Management

### Vibration Energy

Piezoelectric or Electromagnetic Harvester → Rectification → Energy-Harvesting PMIC

Potential environments include machinery, transportation infrastructure, industrial equipment, and wind-turbine structures.

### Thermal Energy

Thermoelectric Generator → Ultra-Low-Voltage Boost Converter → Power Management

## Common Power Architecture

Energy Sources
↓
Source-Specific Harvesting Modules
↓
Power Management System
↓
Energy Storage
↓
Voltage Regulation
↓
Load

Possible storage technologies include supercapacitors and rechargeable batteries.

## Measurement and Telemetry

Sensors will measure:

- Source voltage
- Source current
- Harvested power
- Storage voltage
- Output voltage/current
- Temperature
- Environmental conditions
- Conversion efficiency

## Controller

An ESP32-class microcontroller is initially proposed for:

- Sensor acquisition
- Data logging
- Energy-source identification
- Power-management control
- Bluetooth/Wi-Fi telemetry
- Communication with the Android application

## Android System

The Android application will provide:

- Real-time telemetry
- Energy-source monitoring
- Historical graphs
- Efficiency calculations
- Experiment logging
- Device status
- Configuration and control

## Prototype 001

Prototype 001 will prioritize measurement over charging capability.

The objective is to determine experimentally how much usable energy can be harvested from each source under controlled and real-world conditions.

No energy-harvesting capability will be represented as practical device charging until supported by repeatable measured data.

## Engineering Research Policy

Successful and unsuccessful experiments will both be documented.

Each experiment should record:

- Date
- Prototype revision
- Hardware configuration
- Components
- Environmental conditions
- Test procedure
- Raw measurements
- Calculations
- Results
- Problems encountered
- Conclusions
- Recommended next experiment

This provides technical traceability and supports future engineering and intellectual-property documentation.
