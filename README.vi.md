# Xin chào, tôi là Đoàn Xuân Báu

**Sinh viên Kỹ thuật Điện tử - Viễn thông | Embedded Systems | IoT | Backend Integration**

Tôi là sinh viên năm 4 tại **Đại học Bách khoa Hà Nội (HUST)**, đang phát triển năng lực tại giao điểm giữa **Embedded Firmware, Industrial IoT và Backend Engineering**.

Tôi quan tâm đến cách một hệ thống vận hành tổng thể — từ thu thập dữ liệu cảm biến, thực thi firmware, giao thức truyền thông đến xử lý dữ liệu tại backend và lưu trữ trong cơ sở dữ liệu.

Tôi hướng đến việc xây dựng các hệ thống:
- Có cấu trúc rõ ràng và dễ hiểu.
- Có thể kiểm thử và đánh giá.
- Hoạt động ổn định trong điều kiện thực tế.
- Dễ bảo trì và mở rộng.
- Phù hợp với giới hạn phần cứng và tài nguyên.

[English](README.md)

---

## Định hướng hiện tại

- **Embedded Firmware:** C/C++, ESP32, STM32, non-blocking execution, state machine.
- **Industrial IoT:** MQTT, thu thập dữ liệu cảm biến, telemetry và kết nối thiết bị.
- **Backend Integration:** Java, Spring Boot, REST API.
- **Database Engineering:** PostgreSQL, SQL và thiết kế dữ liệu.
- **System Design:** Luồng dữ liệu, phát hiện lỗi, thiết kế giao thức và tài liệu kỹ thuật.

Định hướng chuyên môn dài hạn của tôi là **Embedded Systems và Industrial IoT**, với sự quan tâm đến Edge AI như một hướng phát triển trong tương lai.

---

## Các dự án tiêu biểu

### 1. Hệ thống giám sát và thu thập dữ liệu IoT (IoT Telemetry System)

`ESP32-S3` `C/C++` `PlatformIO` `MQTT` `Spring Boot` `PostgreSQL`

Hệ thống giám sát IoT quy mô nhỏ, kết nối quá trình thu thập dữ liệu cảm biến, firmware nhúng, truyền thông MQTT và xử lý dữ liệu tại backend.

**Vai trò:** Trưởng nhóm (3 thành viên), phụ trách firmware ESP32 và thiết kế giao thức truyền dữ liệu.

Các nội dung đã triển khai:

- Phát triển firmware non-blocking, sử dụng state machine và System Tick Timer.
- Tách các tác vụ đọc cảm biến, lọc số và truyền dữ liệu thành các tác vụ định kỳ độc lập.
- Thiết lập hai môi trường PlatformIO cho phần cứng thực tế và mô phỏng Wokwi.
- Triển khai lấy mẫu cảm biến MQ2 và DHT11, kết hợp bộ lọc số để giảm nhiễu.
- Thiết kế giao thức truyền dữ liệu nhị phân 16 byte kèm CRC để kiểm tra tính toàn vẹn dữ liệu.
- Cấu hình MQTT Last Will and Testament (LWT) để phát hiện node mất kết nối bất thường.
- Xây dựng backend bằng Spring Boot và PostgreSQL để giải mã gói tin, lưu trữ telemetry và cung cấp REST API.

**Mã nguồn:**
- [IoT Telemetry Firmware](https://github.com/XuanBau011205/IoT-Telemetry)
- [IoT Telemetry Backend](https://github.com/XuanBau011205/IoT-TelemetryBackend)

### 2. Thiết bị đo ECG một đạo trình & phân tích HRV chạy pin (P05)

`STM32F103C8T6` `AD8232` `INA219` `Altium Designer` `2-Layer PCB` `C (Q15 DSP)` `Python`

Dự án nghiên cứu – thiết kế thiết bị thu tín hiệu điện tim (ECG) một đạo trình chạy pin Li-ion, phát hiện đỉnh R và tính toán chỉ số HRV thời gian thực bằng toán học dấu phẩy tĩnh `Q15` trực tiếp trên MCU không FPU, tối ưu dòng ngủ sâu (`32.1 µA`) và kiểm thử tự động MIT-BIH Hardware-in-the-Loop (HIL).

**Vai trò:** Trưởng nhóm (3 thành viên), phụ trách thiết kế phần cứng (Schematic + PCB 2 lớp), kiến trúc firmware và khung mô phỏng bo ảo.

| Mặt Top (`80 × 55 mm`, phân 4 vùng) | Mặt Bottom (GND liền khối >90% + 125 Stitching Vias) |
| :---: | :---: |
| <img src="https://raw.githubusercontent.com/XuanBau011205/stm32-single-lead-ecg-hrv/main/docs/images/pcb_top.png" alt="P05 ECG PCB Top Layer" width="380" /> | <img src="https://raw.githubusercontent.com/XuanBau011205/stm32-single-lead-ecg-hrv/main/docs/images/pcb_bottom.png" alt="P05 ECG PCB Bottom Layer" width="380" /> |

Các nội dung đã triển khai:

- Hoàn thiện sơ đồ nguyên lý và bộ thư viện chuẩn IPC-7351 trên Altium Designer (**91 linh kiện, `ERC = 0 Errors, 0 Warnings`**).
- Thiết kế hoàn chỉnh **PCB 2 lớp kích thước `80.0 × 55.0 mm` (`DRC = 0 Violations`)**: tách biệt chặt vùng Analog AFE (`AD8232`) và vùng Digital (`STM32`, `SPI1`, `Power`), mặt GND đáy liền khối >90% kèm 125 stitching vias, đi dây vi sai ECG đối xứng (0 via) và bảo vệ thạch anh `8 MHz / 32.768 kHz`.
- Thiết kế chuỗi nguồn siêu tiết kiệm năng lượng (mục tiêu `Stop Mode = 32.1 µA`): sạc Li-ion `MCP73831`, LDO `MCP1700`, đo dòng `INA219` + header PPK2 `J_IMEAS`, ngắt nguồn thẻ microSD bằng P-MOSFET `AO3401` và ngắt cầu đo pin bằng `2N7002`.
- Tự động hóa bố trí linh kiện, đi dây vùng tín hiệu nhạy cảm và dọn lỗi silkscreen/DRC bằng Altium DelphiScript; xuất đầy đủ bộ file gia công kiểm chứng trên **JLCPCB Gerber Viewer** (Gerber RS-274X, NC Drill PTH/NPTH/Slot, BOM, Pick-and-Place).
- Xây dựng khung firmware CMake zero-heap (`Q15` vs `Soft-Float`, Pan–Tompkins + nội suy Parabol, Ping-Pong DMA) và bản thiết kế **Python Digital Twin (`P05-Sim`)** (Unicorn ARM Cortex-M3 + Fast SIL + PySide6 Virtual Lab).

**Trạng thái:** Hoàn thành Cổng Phần cứng G1 & G2 (`ERC = 0`, `DRC = 0`, sẵn sàng đặt mạch); đang chuyển sang triển khai firmware và khung mô phỏng Python.

**Mã nguồn:**
- [P05 STM32 Single-Lead ECG & HRV](https://github.com/XuanBau011205/stm32-single-lead-ecg-hrv)

---

## Kỹ năng kỹ thuật

### Embedded Systems và phần cứng
- C / C++, ESP32, STM32F103.
- UART, SPI, I2C, ADC/DMA, Interrupts.
- Thu thập dữ liệu cảm biến và lọc số fixed-point (`Q15`).
- Firmware state machine và tối ưu chế độ tiêu thụ thấp.
- Thiết kế schematic, layout PCB 2 lớp hỗn hợp Analog/Digital (Altium Designer), xuất Gerber/BOM và gỡ lỗi phần cứng.

### IoT và truyền thông
- MQTT.
- HTTP / REST concepts.
- Giao thức truyền dữ liệu nhị phân.
- CRC và kiểm tra tính toàn vẹn dữ liệu.
- Kết nối thiết bị và telemetry.

### Backend và cơ sở dữ liệu
- Java, Spring Boot.
- PostgreSQL, SQL.
- Phát triển REST API.
- Tích hợp backend với thiết bị IoT.

### Công cụ và môi trường phát triển
- PlatformIO, Arduino IDE, Altium Designer.
- Logic Analyzer, Oscilloscope.
- Git / GitHub, Linux cơ bản, Docker.

### Tài liệu hóa và thiết kế
- Markdown, Mermaid.
- ERD, State machine diagrams.
- Tài liệu thiết kế kỹ thuật.

---

## Phương pháp tiếp cận kỹ thuật

Tôi thường tiếp cận bài toán từ cấp độ hệ thống trước khi đi sâu vào từng phần triển khai.

1. **Phân tích:** Xác định yêu cầu, giới hạn và hành vi mong đợi.
2. **Mô hình hóa:** Định nghĩa cấu trúc dữ liệu, trạng thái, giao diện và ranh giới hệ thống.
3. **Thiết kế:** Chia hệ thống thành các module có trách nhiệm rõ ràng.
4. **Triển khai:** Phát triển các thành phần firmware và backend.
5. **Kiểm chứng:** Kiểm thử luồng hoạt động bình thường, trường hợp biên và trạng thái lỗi.
6. **Tài liệu hóa:** Ghi lại quyết định thiết kế, giới hạn và hướng cải tiến.

Tôi coi trọng giao diện rõ ràng và phân chia trách nhiệm hợp lý giữa phần cứng, firmware, lớp truyền thông và backend.

---

## Hướng học tập tiếp theo

Tôi đang từng bước phát triển kiến thức chuyên sâu hơn về:

- Embedded Linux và Industrial IoT.
- Kiến trúc firmware đáng tin cậy.
- Edge Computing và Edge AI.
- Hệ thống cảm biến phân tán.
- Thiết kế hệ thống có khả năng phát hiện và xử lý lỗi.

Tôi cũng đang học tiếng Đức để phục vụ mục tiêu phát triển sự nghiệp kỹ thuật tại Đức trong dài hạn.

---

## Nguyên tắc làm việc

> Kỹ thuật tốt không nằm ở việc tạo ra sự phức tạp, mà ở khả năng hiểu rõ các giới hạn, xác định trách nhiệm và khiến từng thành phần phối hợp với nhau một cách đáng tin cậy.

Tôi ưu tiên những triển khai nhỏ, có thể kiểm thử và đánh giá được hơn là những kiến trúc quá lớn nhưng khó kiểm chứng.

---

**Đang phát triển:** Embedded Firmware + Industrial IoT + Backend Integration.
