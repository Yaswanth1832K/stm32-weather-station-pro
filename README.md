# 🌦 STM32 Weather Station Pro

A real-time embedded weather monitoring system built on the **STM32F4 microcontroller** that measures environmental conditions and provides live display and alert notifications.

---

## 📌 Overview

STM32 Weather Station Pro is an embedded firmware project designed to monitor environmental parameters using multiple sensors and display the results in real time.
The system periodically collects data from connected sensors, processes it on the microcontroller, and outputs the readings to an LCD display and serial interface.

The project demonstrates low-level microcontroller programming, peripheral interfacing, interrupt handling, and real-time sensor monitoring without using high-level hardware abstraction libraries.

---

## ❓ Problem Statement

Environmental monitoring systems must continuously collect accurate sensor data and react immediately to changing conditions (like rain).
A typical implementation using polling can be inefficient and slow.

This project solves the problem by using:

* hardware timers
* interrupts
* direct register-level programming

to ensure efficient and responsive operation.

---

## ✨ Features

* Real-time temperature and humidity monitoring
* Rain detection with alerts
* Light intensity measurement
* LCD live display
* UART serial logging
* Buzzer and LED warning system
* Periodic sensor sampling using interrupts
* Efficient low-level firmware (no HAL)

---

## 🧠 System Working

1. Sensors collect environmental data.
2. STM32 reads sensors at fixed intervals using SysTick timer interrupts.
3. Data is processed and converted to readable values.
4. Readings are displayed on a 16x2 LCD (I2C interface).
5. Data is transmitted over UART to external devices.
6. Rain detection triggers buzzer and LED alerts.

---

## 🔌 Hardware Components

| Component               | Purpose                        |
| ----------------------- | ------------------------------ |
| STM32F4 Microcontroller | Main controller                |
| DHT22                   | Temperature & Humidity sensing |
| LDR                     | Light intensity measurement    |
| Rain Sensor             | Rain detection                 |
| 16x2 LCD (I2C PCF8574)  | Data display                   |
| Buzzer                  | Alert notification             |
| LED                     | Rain warning indicator         |

---

## ⚙️ Key Embedded Concepts Used

### GPIO Interfacing

Reading digital and analog inputs from sensors and controlling LED/buzzer outputs.

### Interrupts (SysTick Timer)

Periodic sensor readings without blocking CPU execution.

### I2C Communication

Used to communicate with the LCD display via PCF8574 I/O expander.

### UART Communication

Transmits sensor data to serial monitor or external logging device.

### Register-Level Programming

Direct manipulation of STM32 registers instead of HAL libraries for higher performance and learning hardware control.

---

## 🛠 Tech Stack

**Language**

* Embedded C

**Platform**

* STM32F4 Microcontroller

**Peripherals Used**

* GPIO
* UART
* I2C
* Timers / SysTick Interrupt

---

## 📂 Project Structure

```
stm32-weather-station-pro/
│
├── stm32_weather_station_pro.c
├── README.md
└── Documentation (report file)
```

---

## 🚀 How to Run

1. Connect STM32 board via ST-Link programmer
2. Open project in STM32CubeIDE / Keil
3. Compile firmware
4. Flash code into microcontroller
5. Connect sensors and power the board

---

## ▶️ Usage

After powering the system:

* LCD displays temperature, humidity, light level, and rain status
* UART sends data to serial monitor
* Buzzer and LED activate during rain detection

---

## 📊 Example Output

LCD Screen:

```
Temp: 28°C
Humidity: 65%
Light: Medium
Rain: Detected
```

---

## 🎯 Learning Outcomes

This project demonstrates practical understanding of:

* Microcontroller architecture
* Interrupt-driven programming
* Peripheral interfacing
* Embedded system design
* Real-time data monitoring

---

## 🔮 Future Improvements

* SD card data logging
* Wireless (WiFi/Bluetooth) transmission
* Mobile app monitoring
* Cloud IoT integration

---

## 👨‍💻 Author

**Yaswanth Jallipalli**

---

## 📜 License

This project is for educational and learning purposes.
