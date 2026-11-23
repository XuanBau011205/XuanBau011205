# Hi, I'm Bau Doan

Electronics & Telecommunications Engineering Student | Embedded Systems | IoT | Backend Integration

I'm a fourth-year student at Hanoi University of Science and Technology (HUST), working across embedded firmware, industrial IoT, and backend integration.

My focus is understanding how a system works end to end, from sensor acquisition and firmware execution to communication protocols, backend processing, and data storage.

I aim to build systems that are:

- Structured and understandable
- Reliable under imperfect conditions
- Testable before deployment
- Documented for future development
- Practical within real hardware constraints

[Tiếng Việt](README.vi.md)

---

## Current Focus

- Embedded Firmware: C/C++, ESP32, STM32, non-blocking execution, state machines.
- Industrial IoT: MQTT, sensor acquisition, telemetry, device connectivity.
- Backend Integration: Java, Spring Boot, REST APIs.
- Database Engineering: PostgreSQL, SQL, data modeling.
- System Design: Data flow, fault detection, protocol design, technical documentation.

My long-term direction is Embedded Systems and Industrial IoT, with Edge AI as a next area to explore.

---

## Featured Projects

### 1. IoT Telemetry System

<sub>ESP32-S3 | C/C++ | PlatformIO | MQTT | Spring Boot | PostgreSQL</sub>

A small IoT monitoring system connecting sensor acquisition, embedded firmware, MQTT messaging, and backend data storage.

Role: Team Leader (3 members), responsible for ESP32 firmware and communication protocol design.

Key work:

- Built non-blocking firmware using a state machine and System Tick Timer.
- Separated sensor reading, digital filtering, and data transmission into periodic tasks.
- Configured PlatformIO environments for physical hardware and Wokwi simulation.
- Implemented MQ2 and DHT11 sampling with digital filtering.
- Designed a 16-byte binary protocol with CRC for packet integrity.
- Configured MQTT Last Will and Testament (LWT) to detect unexpected disconnects.
- Built a Spring Boot and PostgreSQL backend to decode packets, store telemetry, and expose REST APIs.

Repositories:
- [IoT Telemetry Firmware](https://github.com/XuanBau011205/IoT-Telemetry)
- [IoT Telemetry Backend](https://github.com/XuanBau011205/IoT-TelemetryBackend)

### 2. Battery-Powered Single-Lead ECG & On-Device HRV Monitor (P05)

<sub>STM32F103C8T6 | AD8232 | INA219 | Altium Designer | C (Q15 DSP) | Python</sub>

A battery-powered single-lead ECG acquisition and real-time HRV analysis device built on STM32F103C8T6 and the AD8232 analog front-end.

Role: Team Leader (3 members), responsible for schematic and 2-layer PCB design, firmware architecture, and Python virtual board simulation.

Key work:

- Completed schematic (91 components, ERC = 0) and 2-layer 80 x 55 mm mixed-signal PCB in Altium Designer (DRC = 0), with Gerber, Drill, BOM, and Pick-and-Place files ready for fabrication.
- Designed a low-power supply path (32.1 uA Stop Mode target) with INA219 current measurement and MOSFET power gating for microSD and battery voltage sensing.
- Set up a zero-heap CMake firmware structure (Q15 DSP and R-peak/HRV pipeline) and built a Python virtual hardware twin using Unicorn (ARM Cortex-M3) and STM32F103 MMIO models.

Links:
- [Project Repository (P05 ECG)](https://github.com/XuanBau011205/stm32-single-lead-ecg-hrv)
- [Full Visual Portfolio](https://github.com/XuanBau011205/bau-portfolio)

---

## Technical Skills

### Embedded Systems & Hardware
- C / C++
- ESP32, STM32F103
- UART, SPI, I2C, ADC/DMA, Interrupts
- Sensor acquisition and fixed-point digital filtering (Q15)
- Firmware state machines and low-power modes
- Schematic capture, 2-layer mixed-signal PCB layout (Altium Designer), Gerber/BOM generation, hardware debugging

### IoT & Communication
- MQTT
- HTTP / REST
- Binary communication protocols
- CRC and data integrity
- Device connectivity and telemetry

### Backend & Database
- Java, Spring Boot
- PostgreSQL, SQL
- REST API development
- Backend integration with IoT devices

### Tools & Development
- PlatformIO, Arduino IDE, Altium Designer
- Logic Analyzer, Oscilloscope
- Git / GitHub, Linux basics, Docker

### Documentation & Design
- Markdown, Mermaid
- ERD, state machine diagrams
- Technical design documentation

---

## Engineering Approach

I start from the system level before working on individual modules:

1. Understand: Identify requirements, constraints, and expected behavior.
2. Model: Define data structures, states, interfaces, and system boundaries.
3. Design: Split the system into manageable modules.
4. Implement: Build firmware and backend components.
5. Validate: Test normal paths, edge cases, and fault conditions.
6. Document: Record decisions, limits, and next steps.

I focus on clear interfaces and responsibilities across hardware, firmware, communication, and backend layers.

---

## Future Learning Direction

- Embedded Linux and Industrial IoT
- Reliable firmware architecture
- Edge computing and Edge AI
- Distributed sensor systems
- Fault-tolerant system design

I am also learning German toward a long-term goal of working as an engineer in Germany.

---

## Working Principle

> Good engineering is not about adding complexity. It is about understanding constraints, defining responsibilities, and making each part work together reliably.

I prefer small, testable implementations over large architectures that are hard to verify.

---

Currently working on: Embedded Firmware, Industrial IoT, and Backend Integration.
