# Hi, I'm Bau Doan

**Electronics & Telecommunications Engineering Student | Embedded Systems | IoT | Backend Integration**

I'm a fourth-year student at Hanoi University of Science and Technology (HUST), building practical systems at the intersection of **Embedded Firmware, Industrial IoT, and Backend Engineering**.

My focus is understanding how a system works as a whole — from sensor acquisition and firmware execution to communication protocols, backend processing, and data storage.

I care about building systems that are:

- Structured and understandable
- Reliable under imperfect conditions
- Testable before deployment
- Documented for future development
- Practical within real hardware constraints
  
[Tiếng Việt](README.vi.md)

---

## Current Focus

I'm currently developing my skills in:

- **Embedded Firmware:** C/C++, ESP32, STM32, non-blocking execution, state machines.
- **Industrial IoT:** MQTT, sensor acquisition, telemetry, device connectivity.
- **Backend Integration:** Java, Spring Boot, REST APIs.
- **Database Engineering:** PostgreSQL, SQL, data modeling.
- **System Design:** Data flow, fault detection, protocol design, and system documentation.

My long-term technical direction is Embedded Systems and Industrial IoT, with an interest in Edge AI as a future extension.

---

## Featured Projects

### 1. IoT Telemetry System

<sub>ESP32-S3 | C/C++ | PlatformIO | MQTT | Spring Boot | PostgreSQL</sub>

A small IoT monitoring system connecting sensor acquisition, embedded firmware, MQTT communication, and backend data processing.

**My role:** Team Leader (3 members), responsible for ESP32 firmware and communication protocol design.

Key implementations:

- Developed non-blocking firmware using a state-machine approach and System Tick Timer.
- Separated sensor acquisition, digital filtering, and data transmission into independent periodic tasks.
- Configured separate PlatformIO environments for physical hardware and Wokwi simulation.
- Implemented MQ2 and DHT11 sensor sampling with digital filtering.
- Designed a 16-byte binary communication protocol with CRC for data integrity checking.
- Configured MQTT Last Will and Testament (LWT) to detect unexpected node disconnections.
- Developed a Spring Boot and PostgreSQL backend to decode packets, store telemetry, and expose REST APIs.

**Repositories:**
- [IoT Telemetry Firmware](https://github.com/XuanBau011205/IoT-Telemetry)
- [IoT Telemetry Backend](https://github.com/XuanBau011205/IoT-TelemetryBackend)

### 2. Battery-Powered Single-Lead ECG & On-Device HRV Monitor (P05)

<sub>STM32F103C8T6 | AD8232 | INA219 | Altium Designer | C (Q15 DSP) | Python</sub>

A battery-powered single-lead ECG acquisition and real-time HRV analysis device built around an ARM Cortex-M3 MCU and AD8232 analog front-end.

**My role:** Team Leader (3 members), responsible for mixed-signal hardware design (schematic + 2-layer PCB), firmware architecture, and Python virtual hardware simulation.

Key highlights:

- Completed schematic and 2-layer `80 × 55 mm` mixed-signal PCB in Altium Designer (`ERC = 0`, `DRC = 0`, fabrication-ready Gerber/BOM).
- Designed an ultra-low-power supply tree (`32.1 µA` Stop Mode target) with `INA219` current monitoring and MOSFET power-gating for microSD & battery sensing.
- Built a zero-heap CMake firmware structure (`Q15` DSP + R-peak/HRV pipeline) and a Python ARM Cortex-M3 virtual board twin (`Unicorn` + STM32F103 MMIO).

**Links:**
- [Project Repository (P05 ECG)](https://github.com/XuanBau011205/stm32-single-lead-ecg-hrv)
- [Full Visual Portfolio](https://github.com/XuanBau011205/bau-portfolio)

---

## Technical Skills

### Embedded Systems & Hardware
- C / C++
- ESP32, STM32F103
- UART, SPI, I2C, ADC/DMA, Interrupts
- Sensor acquisition and fixed-point digital filtering (`Q15`)
- Firmware state machines and low-power modes
- Schematic capture, 2-layer mixed-signal PCB layout (Altium Designer), Gerber/BOM & hardware debugging

### IoT & Communication
- MQTT
- HTTP / REST concepts
- Binary communication protocols
- CRC and data integrity
- Device connectivity and telemetry

### Backend & Database
- Java
- Spring Boot
- PostgreSQL
- SQL
- REST API development
- Backend integration with IoT devices

### Tools & Development
- PlatformIO
- Arduino IDE
- Altium Designer
- Logic Analyzer
- Oscilloscope
- Git / GitHub
- Linux basics
- Docker

### Documentation & Design
- Markdown
- Mermaid
- ERD
- State machine diagrams
- Technical design documentation

---

## Engineering Approach

I approach engineering problems from the system level before focusing on individual implementation details.

My typical workflow:

1. **Understand:** Identify requirements, constraints, and expected behavior.
2. **Model:** Define data structures, states, interfaces, and system boundaries.
3. **Design:** Break the system into manageable modules.
4. **Implement:** Develop firmware and backend components.
5. **Validate:** Test normal operation, edge cases, and fault conditions.
6. **Document:** Record decisions, limitations, and possible improvements.

I value clear interfaces and well-defined responsibilities between hardware, firmware, communication layers, and backend services.

---

## Future Learning Direction

I'm gradually building toward deeper expertise in:

- Embedded Linux and Industrial IoT
- Reliable firmware architecture
- Edge computing and Edge AI
- Distributed sensor systems
- Fault-tolerant system design

I'm also learning German as part of my longer-term goal of developing an engineering career in Germany.

---

## Working Principle

> Good engineering is not about adding complexity. It is about understanding constraints, defining responsibilities, and making each part work together reliably.

I prefer small, testable implementations over oversized architectures that are difficult to validate.

---

**Currently building:** Embedded Firmware + Industrial IoT + Backend Integration.

