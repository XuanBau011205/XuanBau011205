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

<sub>STM32F103C8T6 | AD8232 | INA219 | Altium Designer (2-Layer PCB) | C (Q15 DSP) | Python</sub>

A battery-powered single-lead biomedical ECG acquisition and real-time HRV analysis device built around an ARM Cortex-M3 MCU (no FPU) and a minimalist analog front-end (`AD8232`), designed for zero-heap Q15 fixed-point DSP, ultra-low-power Stop Mode (`32.1 µA` target), and automated MIT-BIH Hardware-in-the-Loop (HIL) validation.

**My role:** Team Leader (3 members), responsible for mixed-signal hardware design (schematic + 2-layer PCB), firmware architecture, and simulation framework.

| Top Layer (`80 × 55 mm`, 4-Zone Layout) | Bottom Layer (Solid GND Plane >90% + 125 Stitching Vias) |
| :---: | :---: |
| <img src="https://raw.githubusercontent.com/XuanBau011205/stm32-single-lead-ecg-hrv/main/docs/images/pcb_top.png" alt="P05 ECG PCB Top Layer" width="380" /> | <img src="https://raw.githubusercontent.com/XuanBau011205/stm32-single-lead-ecg-hrv/main/docs/images/pcb_bottom.png" alt="P05 ECG PCB Bottom Layer" width="380" /> |

Key implementations:

- Completed full schematic capture and IPC-7351 custom component libraries in Altium Designer (**91 components, `ERC = 0 Errors, 0 Warnings`**).
- Designed a compact **`80.0 × 55.0 mm` 2-layer mixed-signal PCB (`DRC = 0 Violations`)** with strict Analog/Digital spatial partitioning, >90% unbroken bottom GND plane, 125 stitching vias, symmetric 0-via differential ECG routing, and isolated 8 MHz HSE / 32.768 kHz LSE crystals.
- Engineered an ultra-low-power supply tree (`32.1 µA` Stop Mode target): USB-C 5V-only Li-ion charging (`MCP73831`), `MCP1700` LDO, `INA219` I2C dynamic current monitor + `J_IMEAS` PPK2 header, `AO3401` microSD power-gating, and `2N7002` switched battery divider.
- Automated zero-collision placement, critical analog/crystal pre-routing, and DRC/silkscreen cleanup via custom Altium DelphiScripts; exported factory-verified **JLCPCB Gerber RS-274X, PTH/NPTH/Slot NC Drill, BOM, and Pick-and-Place** packages.
- Architected a zero-heap CMake firmware structure (`Q15` vs. `Soft-Float` Pan–Tompkins + parabolic R-peak interpolation + Ping-Pong DMA) and a **Python Virtual Hardware Twin (`P05-Sim`)** architecture (Unicorn ARM Cortex-M3 + Fast SIL + PySide6 Virtual Lab).

**Status:** Hardware Gate G1 & G2 completed (`ERC = 0`, `DRC = 0`, fabrication files ready); moving into firmware implementation & Python Digital Twin validation.

**Repository:**
- [P05 STM32 Single-Lead ECG & HRV](https://github.com/XuanBau011205/stm32-single-lead-ecg-hrv)

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

