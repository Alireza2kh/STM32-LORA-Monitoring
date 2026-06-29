# STM32 LoRa Temperature & Humidity Monitoring System

## Overview

This project implements a wireless temperature and humidity monitoring system using two STM32 microcontrollers and SX1278 LoRa modules.

The sensor node reads analog sensor values and transmits the data wirelessly using LoRa. The gateway node receives the packets and forwards the received data to a PC via UART.

The project was implemented and tested on real hardware.

---

## Hardware

### Sensor Node
- STM32F103C8T6
- SX1278 LoRa Module
- LM35 Temperature Sensor
- Analog Humidity Sensor (likely HR202L)

### Gateway Node
- STM32F030F4P6
- SX1278 LoRa Module
- USB-to-TTL Converter
- PC Terminal

---

## Features

- LoRa wireless communication
- Temperature monitoring
- Humidity monitoring
- UART data forwarding
- Real hardware implementation
- STM32 HAL based firmware

---

## System Architecture

```text
+----------------------+
| STM32F103C8T6        |
| Sensor Node          |
+----------------------+
           |
           | LoRa SX1278
           |
           v
+----------------------+
| STM32F030F4P6        |
| Gateway Node         |
+----------------------+
           |
           | UART
           |
           v
+----------------------+
| PC Terminal          |
+----------------------+
```

---

## Project Structure

```text
STM32-LoRa-Temperature-Monitoring
│
├──loramaster
│
├── loraslave
│   
│
├── README.md
├── LICENSE
└── .gitignore
```

---

## Development Environment

- Keil MDK
- STM32CubeMX
- STM32 HAL Drivers
- Embedded C

---

## Communication Flow

1. Read analog sensors.
2. Convert sensor values.
3. Send data via LoRa.
4. Receive data on gateway node.
5. Forward data to PC through UART.

---

## Future Improvements

- CRC protected packets
- Packet acknowledgement
- Configuration interface
- Data logging
- Low power optimization

---

## License

This project is released under the MIT License.
